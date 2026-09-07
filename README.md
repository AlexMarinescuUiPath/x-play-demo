# x-play-demo

Order feed for the XPlay Workflow self-healing demo. Same six orders, two shapes.

| File | Shape | Role in the demo |
|---|---|---|
| `orders.json` | v1 - flat `orders[]`, `customer` is a string, `amountCents` is an integer | What the workflow is generated against. Run 1 is green. |
| `orders.v2.json` | v2 - records under `data.orders[]`, `customer` is an object, `amount` is a decimal string | The upstream "broke" its payload. Run 2 fails in the parser and self-heals. |

Raw URLs:

- `https://raw.githubusercontent.com/AlexMarinescuUiPath/x-play-demo/main/orders.json`
- `https://raw.githubusercontent.com/AlexMarinescuUiPath/x-play-demo/main/orders.v2.json`

`raw.githubusercontent.com` caches for about five minutes, so the safe way to switch shapes mid-demo is to
pass the v2 URL as the job's input argument rather than rewriting `orders.json` and waiting.
