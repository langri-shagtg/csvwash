# csvwash

Reusable ETL skeleton for the CSVs I get at work

## How to use

```bash
python pipeline.py raw.csv --config config.yaml --out clean.csv
```

## Features

- Config-driven column renames and type casts
- Writes a cleaning report next to the output
- Chunked reading for files that do not fit in memory
- Drops duplicates, trims strings, normalizes dates

## Install

```bash
pip install -r requirements.txt
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── config.yaml
├── pipeline.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## Why

Needed this for myself; figured others might too.
