# Use tips33 from AI APIs

## OpenAI (Responses API)
```python
from openai import OpenAI
client = OpenAI()
r = client.responses.create(
    model="gpt-5",
    tools=[{"type": "mcp", "server_label": "tips33",
            "server_url": "https://tips33.vercel.app/mcp", "require_approval": "never"}],
    input="Trail running shoes under $200, US",
)
print(r.output_text)
```

## Anthropic (Messages API, MCP connector)
```python
import anthropic
client = anthropic.Anthropic()
r = client.beta.messages.create(
    model="claude-sonnet-4-5", max_tokens=1024,
    mcp_servers=[{"type": "url", "url": "https://tips33.vercel.app/mcp", "name": "tips33"}],
    messages=[{"role": "user", "content": "Trail running shoes under $200, US"}],
    betas=["mcp-client-2025-04-04"],
)
print(r.content)
```

## Any other model or framework
Call the HTTP API as a tool and pass the JSON to the model:
`GET https://tips33.vercel.app/api/recommend?q=<query>&country=US&deals=1`
Schema: https://tips33.vercel.app/openapi.json
