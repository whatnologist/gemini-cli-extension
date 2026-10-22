# Get Shouting

Get Shouting is a marketing platform for social posts, email newsletters, SMS, paid ads (Meta, Google, TikTok), and analytics. This extension connects four Get Shouting MCP servers:

| Server | Use it for |
|---|---|
| `get-shouting-campaigns` | Planning, building, and scheduling a cross-channel campaign (posts, emails, ads) |
| `get-shouting-social` | Writing, previewing, scheduling, and publishing social posts; paid social ads |
| `get-shouting-email` | Writing, previewing, sending, and scheduling email newsletters |
| `get-shouting-analytics` | Reading results for posts, emails, SMS, and ads; PDF reports |

## How the tools work

- Sign-in is OAuth. The first call opens a browser to sign in to Get Shouting and approve access.
- Call `get_me` first to find the user's brands; most tools need a `brandId`.
- Writing follows brief, then commit: a `*_brief` tool returns constraints and context, you write the copy, and a commit tool (`set_post_copy`, `set_email_blast_copy`, `campaign_commit_materials`) validates and saves it. The server does not generate copy.
- Anything that publishes, sends, schedules, deletes, or spends is confirm, then commit: the first call returns a preview and a `confirmToken`. Show the preview to the user and call again with the token only after they approve.
- Results include an `Open in Get Shouting` link to the record in the web app.

Docs: https://www.getshouting.app/help/ai-assistants
