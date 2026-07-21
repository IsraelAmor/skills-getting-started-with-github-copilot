# AGENTS instructions for this repository

## Project overview
- This repository contains a small FastAPI application for the Mergington High School activities API.
- The main application code lives in [src/app.py](src/app.py) and the frontend assets live in [src/static](src/static).
- The API stores activity data in memory, so restarting the server resets all changes.

## Working conventions
- Keep changes small and focused. Prefer updating the existing FastAPI app rather than introducing new frameworks or persistence layers.
- Preserve the existing API contract unless the task explicitly requires a change.
- The main endpoints are:
  - GET /activities
  - POST /activities/{activity_name}/signup
- Be careful when editing response shapes or validation logic because the current app is intentionally simple.

## Local development
- Install dependencies with:
  - `pip install -r requirements.txt`
- Run the app locally with:
  - `python -m uvicorn src.app:app --reload`
  - or, from the src directory, `python -m uvicorn app:app --reload`
- API docs are available at http://localhost:8000/docs when the server is running.

## Testing
- Pytest is configured via [pytest.ini](pytest.ini).
- There are no test files yet; if you add tests, place them under a `tests/` directory and keep them focused on the FastAPI behavior.

## Files to consult first
- [src/app.py](src/app.py) for the API implementation
- [src/README.md](src/README.md) for the app overview and endpoint documentation
- [pytest.ini](pytest.ini) for the test configuration
