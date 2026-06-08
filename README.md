# Distinguished-Bingus — Hermes Agent

Docker Compose deployment of the official [Nous Research Hermes Agent](https://hub.docker.com/r/nousresearch/hermes-agent)
image, intended for deployment on a Hostinger VPS.

## Services

- **hermes** (`nousresearch/hermes-agent:latest`) running `gateway run`
  - `8642` — gateway API (OpenAI-compatible)
  - `9119` — web dashboard (`HERMES_DASHBOARD=1`)
  - Data persisted in the `hermes-data` named volume (`/opt/data`)

## Model provider

No model provider key is baked into this repo. Set `ANTHROPIC_API_KEY` or
`OPENAI_API_KEY` after deploy via the dashboard or by redeploying with the
environment variable supplied out-of-band.
