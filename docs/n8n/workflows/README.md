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
