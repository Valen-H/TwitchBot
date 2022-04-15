# TwitchBot

> Twitch account chatting (and more?) automation.

**Visit Bot Host Site _[Here](https://valen-h.github.io/TwitchBot/TwitchBot.html "GitHub Pages")_**  
Learn JS RegExp _[Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp "JS RegEx MDN")_.

## Notes

> `Twitch.js` is `TMI`-based.

### Triggers

> JS code with to evaluate, return truth-y to activate rule.

Example of accessable scope values within the rule:
```javascript
{
	"_raw": "@badge-info=subscriber/15;badges=subscriber/12,glitchcon2020/1;color=#485F86;display-name=exemplative;emotes=181172:8-14;first-msg=0;flags=;id=916b68bb-b21c-4c71-ab4e-60eac715c65b;mod=0;room-id=24761645;subscriber=1;tmi-sent-ts=1650057813368;turbo=0;user-id=153885677;user-type= :exemplative!exemplative@exemplative.tmi.twitch.tv PRIVMSG #cirno_tv :masthir naroWOW",
	"timestamp": "2022-04-15T21:23:33.368Z",
	"command": "PRIVMSG",
	"event": "PRIVMSG",
	"channel": "#cirno_tv",
	"username": "exemplative",
	"isSelf": false,
	"message": "masthir naroWOW",
	"tags": {
		"badgeInfo": "subscriber/15",
		"badges": {
			"subscriber": 12,
			"glitchcon2020": "1"
		},
		"color": "#485F86",
		"displayName": "exemplative",
		"emotes": [
			{
				"id": "181172",
				"start": 8,
				"end": 14
			}
		],
		"firstMsg": "0",
		"flags": "",
		"id": "916b68bb-b21c-4c71-ab4e-60eac715c65b",
		"mod": "0",
		"roomId": "24761645",
		"subscriber": "1",
		"tmiSentTs": "1650057813368",
		"turbo": "0",
		"userId": "153885677",
		"userType": "",
		"emoteSets": [],
		"username": "exemplative",
		"isModerator": false
	}
}
```

#### Examples

* Activate if a message is sent by a user in the designated channel and carries a designated message:  
   `username == "user1" && /^starts with .+? and ends with$/.test(message)`

### Reactions

> Reactions are responses to rules activation/triggering.
> Same syntax as [Triggers](#triggers "Triggers") but bot-oriented instead of event/message-oriented.
