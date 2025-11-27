# hai5016-rag

A repository for experimenting with RAG and LangChain.

## Weather Agent

Added `agent_weather.py` — a small example agent that:

- Geocodes a free-form location via Nominatim (OpenStreetMap).
- Fetches current weather from Open-Meteo (no key required).
- Uses Claude Sonnet 4.5 via LangChain's `ChatAnthropic` to produce a concise, friendly weather report.

Usage:

1. Install dependencies (example):

```
pip install langchain requests
```

2. Set your Anthropic API key in the environment (PowerShell example):

```
$env:ANTHROPIC_API_KEY = 'sk-...'

# Then run:
python agent_weather.py "Seoul, South Korea"
```

Notes:
- If `ANTHROPIC_API_KEY` is not set the script will still print raw weather data but skip Claude summarization.
- `agent_weather.py` is intentionally small and designed as an educational example.

