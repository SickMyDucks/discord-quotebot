# QuoteBot
### A Discord selfbot to add "reply"-like quoting functionality
In action
------
![gif demonstration](https://i.neilrichter.com/wc6vu.gif)

Purpose
------
A proof-of-concept for how replying/quoting could work in Discord. This solution is obviously not optimal, but it's a cool way to see how quoting might work in the future (if ever implemented into the Discord client itself).

Using
------
Make sure you have "Developer Mode" enabled in Discord's Appearance settings. Right click the message you want to quote, and click "Copy ID."

Next, type `{quote:` where you want the quote to appear, and paste in the ID of the message. Then, add the source with `, source:` and paste the ID of the Text channel from where you are quoting. End with `}`.

Example : `{quote<messageID>, source:<sourceChannel>}`

When you send the message, it will be replaced with the quote and its source! Wow!

Features
------
* Easy, fast quoting
* No annoying error messages when you mess up. Nothing happens.

Limitations
------
* Sort of spammy (bigger guilds might not like you using this)
* Only looks for quotes in the last 50 messages (if the selfbot can't find the message, nothing happens)
* Currently only available on servers text channels, not DM channels

Setup
------
Clone/download the repo, and with a working Node installation, run `npm install`.

Rename `config.js.defaults` to `config.js`, and enter your user token (this can be found under Discord's Ctrl-Shift-I menu by Application > Storage > Local Storage and finding the key/value pair with the key `token`) between the quotes.

Now, just run the selfbot with `node index.js`, and as long as the bot is running, you can quote people freely.
