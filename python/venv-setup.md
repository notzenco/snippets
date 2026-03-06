# Python Virtual Environments

Quick reference for setting up and managing virtual environments.

## venv (built-in)

```bash
# create
python3 -m venv .venv

# activate
source .venv/bin/activate    # linux/mac
.venv\Scripts\activate       # windows

# deactivate
deactivate

# freeze deps
pip freeze > requirements.txt

# install from requirements
pip install -r requirements.txt
```

## uv (fast alternative)

```bash
# install uv
curl -LsSf https://astral.sh/uv/install.sh | sh

# create venv
uv venv

# install deps
uv pip install -r requirements.txt

# add a package
uv pip install requests
```

## Tips

- Always add `.venv/` to your `.gitignore`
- Pin versions in `requirements.txt` for reproducibility (`requests==2.31.0`, not `requests`)
- Use `python -m pip` instead of bare `pip` to avoid PATH confusion
