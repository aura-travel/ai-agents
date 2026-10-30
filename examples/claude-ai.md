# Claude (claude.ai and the Claude apps)

The aura.travel connector needs nothing set up on aura.travel's side: no account, OAuth app, API key or IP allowlist.
Claude reaches it from Anthropic's network, which aura.travel recognises.

## For admins (Team and Enterprise)

1. In **Organization settings > Connectors**, add **aura.travel** from the directory.
2. Members connect it under **Customize > Connectors**, and can turn it on or off per chat from the **+** menu >
   **Connectors**.
3. All five tools only read data. You can set them to **Always allow** so members aren't asked before each call. If
   your members only travel, you can block `list_your_property` and `integrate_with_aura`, which are for accommodation
   owners and software companies.

## For individual users

Open **Customize > Connectors**, find **aura.travel** and connect it. Then ask, for example: "Find a pet-friendly stay
in Byron Bay, NSW, Australia for 2 adults, 12 to 15 December, and price the best one."

Before the listing appears in your directory, you can add it as a custom connector: **Customize > Connectors > Add
custom connector**, URL `https://ai.aura.travel/mcp`, no sign-in.

## Data and booking

Claude sends only what a search needs, such as the place, dates, number of guests and filters; no personal details.
The connector never books or pays: each stay comes with a link to aura.travel, where the traveller books.

Questions: https://aura.travel/contact-us.html
