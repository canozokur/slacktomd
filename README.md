## slacktomd
Message parser for Slack raw messages to Github Markdown Syntax.
Based on [https://www.npmjs.com/package/slackdown](slackdown).
Basic formatting like emphasis, strikethrough, code blocks, Slack
<> tags, links and channel/user name convert are supported.

This is a standalone script, requires the channel and users lists as parameters
to convert user notifications (@user) and channel links (#channel) to meaningful
names.

## Usage
### With node.js
var slacktomd = require('slacktomd');

I have not yet published this as an npm package. Include it with a github reference
in your package.json file.

```json
{
  "dependencies": {
    "slacktomd": "canozokur/slacktomd"
  }
}
```

## Parsing
You'll need to pass three parameters to slacktomd.parse method. The first one will be
your message's raw text (not the whole message object). The second is your Slack userlist
object. The third will be the Slack channel list object.

```
var message = slacktomd.parse(slackRawMessage, UserList, ChannelList);
```

TODO:
* Doesn't support emojis
* Doesn't support multiline messages (need to check this)
* Doesn't support blockquotes
