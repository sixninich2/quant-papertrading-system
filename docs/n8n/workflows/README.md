# N8N Workflows

## daily_euro_stoxx_screener.json
- Runs daily via Cron
- Fetches EU stock tickers from PostgreSQL
- Pulls fundamentals via Financial Modeling Prep API
- Applies filters:
  - ROCE > 9%
  - Operating margin > 4%
  - Positive revenue growth
  - Price-to-cash-flow < 7
  - Low leverage
- Stores qualified stocks in the database

## Notes
- API keys and credentials have been removed
- Workflow provided for demonstration and documentation purposes


## How the screening automation works

1. A daily Cron trigger in n8n runs every morning.
2. The workflow fetches a universe of European stocks from a PostgreSQL table.
3. For each ticker, fundamentals are pulled via an external financial API.
4. A screening function applies quantitative filters:
   - ROCE > 9%
   - Operating margin > 4%
   - Positive revenue growth
   - Price-to-cash-flow < 7
   - Low leverage
5. Stocks passing all criteria are stored as "qualified ideas" for paper trading.


## Notes on reproducibility

This repository focuses on documenting system design and logic.

API keys, database credentials, and environment variables have been intentionally removed.
The n8n workflows are provided for demonstration and architectural understanding rather than direct execution.


