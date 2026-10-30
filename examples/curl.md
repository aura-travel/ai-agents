# Raw HTTP with curl

Every request is one JSON-RPC message in a POST, with your agent key. The server is stateless, so there is no
session to keep.

```bash
K='<your aura.travel agent key>'
U=https://ai.aura.travel/mcp
H=(-H "Authorization: Bearer $K" -H 'Content-Type: application/json' -H 'Accept: application/json, text/event-stream' -H 'MCP-Protocol-Version: 2025-11-25')

# The tools and their schemas
curl -s "${H[@]}" "$U" -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'

# Search
curl -s "${H[@]}" "$U" -d '{"jsonrpc":"2.0","id":2,"method":"tools/call","params":{"name":"search_stays","arguments":{"place":"Byron Bay","check_in":"2026-12-12","check_out":"2026-12-15","adults":2}}}'

# Price one stay (listing_id from the search)
curl -s "${H[@]}" "$U" -d '{"jsonrpc":"2.0","id":3,"method":"tools/call","params":{"name":"quote_stay","arguments":{"listing_id":12345,"check_in":"2026-12-12","check_out":"2026-12-15","adults":2}}}'
```

Without a valid key the answer is `401`.
