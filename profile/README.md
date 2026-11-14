# GeniusRelay

One OpenAI-compatible endpoint for 599 AI models from 37 providers, including 43 uncensored and abliterated editions.

Every model page publishes input, output and cached-input prices in USD per 1M tokens. Billing is prepaid and per token; there is no subscription and no routing fee.

## Use it

```bash
curl https://api.geniusrelaygpt.com/v1/chat/completions \
  -H "Authorization: Bearer $GENIUSRELAY_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"deepseek-v4.1-flash","messages":[{"role":"user","content":"Hello"}]}'
```

The SDK shape is OpenAI:

```python
from openai import OpenAI

client = OpenAI(base_url="https://api.geniusrelaygpt.com/v1", api_key="KEY")
resp = client.chat.completions.create(
    model="deepseek-v4.1-flash",
    messages=[{"role": "user", "content": "Hello"}],
)
```

## What is in the catalogue

| Category | Models | Start here |
|---|---:|---|
| Uncensored / abliterated | 43 | https://geniusrelaygpt.com/models/uncensored |
| Reasoning (`:thinking`) | 404 | https://geniusrelaygpt.com/models/thinking |
| Vision input | 334 | https://geniusrelaygpt.com/models/vision |
| Tool calling | 430 | https://geniusrelaygpt.com/models/tools |
| 128K+ context | 384 | https://geniusrelaygpt.com/models/long-context |

Prices range from $0.0195/M input (Ling 3.0 Tiny) to $39.00/M input (Universal Summarizer). Largest context window is 2M.

## What it does not do

- No free tier — new accounts get a small trial credit, then prepaid only
- No embeddings or image generation endpoint yet
- No fine-tuning, no weight hosting
- No per-route SLA — retries and failover are client-side

## Machine-readable

- `https://geniusrelaygpt.com/llms.txt` — facts and page index
- `https://geniusrelaygpt.com/data/models.json` — full catalogue as JSON
- `https://geniusrelaygpt.com/sitemap.xml`

## Docs

- Quickstart: https://geniusrelaygpt.com/docs/quickstart
- API reference: https://geniusrelaygpt.com/docs/api
- Errors: https://geniusrelaygpt.com/docs/errors
- SillyTavern: https://geniusrelaygpt.com/docs/sillytavern
- Cursor: https://geniusrelaygpt.com/docs/cursor

## Other

- Site: https://geniusrelaygpt.com
- Pricing: https://geniusrelaygpt.com/pricing
- Console: https://console.geniusrelaygpt.com
