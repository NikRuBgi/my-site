# DybeeManual – Claude Instructions

## Project Overview
MkDocs documentation project. Key files: `mkdocs.yml`, `docs/`.

## Python / Environment
- Always use a virtual environment (`.venv`) for any Python/MkDocs work.
- Activate with `.venv/Scripts/activate` (Windows) before running pip or mkdocs commands.
- Python 3.13 is installed for the regular user. Do NOT run Claude Code with admin rights — admin has a different PATH and only sees a broken Windows Store Python 3.9.
- `requirements.txt` exists in the project root with all needed packages.

## Development Workflow
- The user runs `mkdocs serve` in a separate terminal (default: http://127.0.0.1:8000). MkDocs auto-reloads on file changes, so Claude does not need to manage the server process.
