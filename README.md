# Try UV

An extremely fast Python package and project manager, written in Rust.
A single tool to replace pip, pip-tools, pipx, poetry, pyenv, twine, virtualenv, and more.

`https://github.com/astral-sh/uv`

## Installation

```sh
pip install uv
pip install pipx && pipx install uv # isolated
brew install uv # possibly best option

# standalone install
curl -LsSf https://astral.sh/uv/install.sh | sh
# uninstall
uv cache clean
rm -r "$(uv python dir)"
rm -r "$(uv tool dir)"
rm ~/.local/bin/uv ~/.local/bin/uvx
```

### Quickstart

```sh
uv init try-uv # create project
uv add ruff # add
uv run ruff check # run a module
uv lock # writes uv.lock
uv sync # creates venv and installs uv.lock
uvx pycowsay 'hello world!' # run module in ephemeral venv
uv tool install ruff # install as an tool (executable), not a module
which ruff # ./try-uv/.venv/bin/ruff
```

### manage python versions

```
uv python install
uv python list
uv python find
uv pin
uv uninstall
```

### run standalone scripts in ephemeral python venv

```sh
uv run
uv add --script
uv add --script script_example.py colorama
uv remove --script
echo 'import requests; print(requests.get("https://astral.sh"))' > example.py

# look at script_example.py to see the uv file header that dynmically resolves deps in a standalone script at runtime
```

# projects

uv init # add remove sync lock run tree build publish

```

```
