# tutor-queue

Distributed tutor queue management system for programming labs and student tutoring sessions.

## Prerequisites

- **Python**: `>= 3.12` (see [`.python-version`](.python-version))
- **[uv](https://docs.astral.sh/uv/)**: Python package and project manager

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/rosefrancis-99/tutor-queue.git
cd tutor-queue
```

### 2. Install `uv` (if not already installed)

**macOS / Linux:**

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows (PowerShell):**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 3. Set up the environment and install dependencies

Using `uv` (recommended, creates `.venv` and installs all dependencies including the `dev` group from `uv.lock`):

```bash
uv sync
```

If you prefer activating the virtual environment directly instead of prefixing commands with `uv run`:

- **macOS / Linux:**

  ```bash
  source .venv/bin/activate
  ```

- **Windows (PowerShell):**

  ```powershell
  .venv\Scripts\Activate.ps1
  ```

- **Windows (Command Prompt):**

  ```cmd
  .venv\Scripts\activate.bat
  ```

## Development

### Linting & Formatting

This project uses [Ruff](https://docs.astral.sh/ruff/) (configured in [`pyproject.toml`](pyproject.toml)):

```bash
# Check for lint issues
uv run ruff check .

# Automatically fix lint issues where possible
uv run ruff check --fix .

# Check formatting
uv run ruff format --check .

# Format code
uv run ruff format .
```

### Running Tests

Tests are run with [pytest](https://docs.pytest.org/) (with `pythonpath = ["src"]` configured in [`pyproject.toml`](pyproject.toml)):

```bash
uv run pytest
```

## Project Structure

```text
tutor-queue/
├── pyproject.toml
├── uv.lock
├── src/
│   ├── client.py
│   ├── protocol.py
│   └── server.py
└── tests/
```
