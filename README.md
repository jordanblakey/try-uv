# Try UV

One package manager to rule them all, supposably.

```sh
pip install uv
uv init try-uv
uv add ruff
uv run ruff check
uv lock
uv sync
uvx pycowsay 'hello world!'
uv tool install ruff # install as an tool (executable), not a module
which ruff # ./try-uv/.venv/bin/ruff
```
