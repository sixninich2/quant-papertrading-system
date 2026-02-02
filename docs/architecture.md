# Architecture

This project is a paper trading platform for European stocks.

Main components:
- N8N: runs a daily stock screener
- Backend: stores signals and simulated trades
- Frontend: displays trades and portfolio
- Dashboard: shows performance metrics

Data flow:
N8N → API → Database → Dashboard / Frontend
