# Get Shouting

Get Shouting is a marketing platform for social posts, email, SMS, CRM journeys, paid ads (Meta, Google, TikTok), inbox, and analytics. This extension connects one remote MCP server at `https://www.getshouting.app/api/mcp` (50 pinned tools): campaigns, social, email, SMS, journeys, ads, and analytics on a single URL.

## How the tools work

- Sign-in is OAuth. The first call opens a browser to sign in to Get Shouting and approve access.
- Call `get_me` first to find the user's brands; most tools need a `brandId`. Use `choose_workflow` when the user has not named a goal.
- List and read records with `list_content` and `get_analytics` (pass `channel` for email, sms, paid or survey results); paid ads with `ads_get` and `ads_check` before `ads_publish`.
- Writing follows brief, then commit: a `*_brief` tool returns constraints and context, you write the copy, and a commit tool (`set_post_copy`, `set_email_blast`, `campaign_commit_materials`) validates and saves it. The server does not generate copy.
- Anything that publishes, sends, schedules, deletes, or spends is confirm, then commit: the first call returns a preview and a `confirmToken`. Show the preview to the user and call again with the token only after they approve.
- Results include an `Open in Get Shouting` link to the record in the web app.

Docs: https://www.getshouting.app/help/ai-assistants
