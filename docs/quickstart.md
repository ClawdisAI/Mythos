# Quickstart

## Install

```bash
pip install agentos
```

Or from source:

```bash
git clone https://github.com/ArchieHowell/AgentOS
cd AgentOS
pip install -e ".[dev]"
```

## Run your first agent

```python
import asyncio
from agentos import Runtime

async def main():
    async with Runtime() as rt:
        result = await rt.run("summarise the top 5 HN stories today and save to hn.md")
        print(result)

asyncio.run(main())
```

Or via CLI:

```bash
agentos run --goal "find all TODO comments in ./src and write a report"
```

## Configure

Copy `.env.example` to `.env` and set your API key:

```bash
cp .env.example .env
# edit .env and set ANTHROPIC_API_KEY
```

## Run tests

```bash
make test
make coverage
```





