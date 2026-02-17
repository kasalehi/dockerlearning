FROM python:3.9-slim

COPY --from=ghcr.io/astral-sh/uv:latest /uv /bin/


WORKDIR /app

COPY pyproject.toml uv.lock ./

RUN uv sync --locked 

COPY main.py ./
ENTRYPOINT ["uv", "run", "main.py"]