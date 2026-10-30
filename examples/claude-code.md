# Claude Code

Keep your agent key in an environment variable, then add the server:

```bash
export AURA_AGENT_KEY='<your aura.travel agent key>'
claude mcp add --transport http aura-travel https://ai.aura.travel/mcp \
  --header "Authorization: Bearer $AURA_AGENT_KEY"
```

Check it with `claude mcp list`. Then ask, for example: "Find a stay in Byron Bay for 2 adults, 12 to 15 December,
and price the best one."
