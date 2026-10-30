# Get Shouting extension for Gemini CLI

Connect [Gemini CLI](https://github.com/google-gemini/gemini-cli) to [Get Shouting](https://www.getshouting.com) to plan marketing campaigns, schedule social posts, send email newsletters, and read marketing analytics from your terminal.

## Install

```bash
gemini extensions install https://github.com/whatnologist/gemini-cli-extension
```

Start `gemini`. The first time a Get Shouting tool runs, a browser window opens: sign in to Get Shouting and approve access. No API keys are stored in this extension.

## What's included

One remote MCP server covering campaigns, social posts and paid social ads, email, SMS, and analytics.

| Server | URL |
|---|---|
| Get Shouting | `https://www.getshouting.app/api/mcp` |

## Requirements

- A Get Shouting account with an active subscription or trial.
- Social, email, and ad accounts connected in Get Shouting for the channels you use.

## Safety

Publishing, sending, scheduling, deleting, and ad spend always show a preview first and run only after you approve. Paid ads run through your own connected ads accounts; Get Shouting charges no fee on ads launched from an assistant.

## Links

- Help: https://www.getshouting.app/help/ai-assistants
- Privacy policy: https://getshouting.com/legal/privacy-policy.html
- Terms of use: https://www.getshouting.com/legal/terms-of-use.html
- Support: support@getshouting.com

## Maintainers

Canonical source lives in the SHOUTapp app repo under `integrations/gemini-cli-extension/`. After changing listing URLs or this README, copy the files here and cut a new GitHub Release — see [`SYNC.md`](SYNC.md).
