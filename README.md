# Test Case: Pip Priority Conflict - .python-version vs pyproject.toml

## Package Manager
Pip

## Python Version Detection
- **Source**: .python-version (PRIORITY #1)
- **Expected Version**: 3.8.10
- **Conflict**: pyproject.toml says >=3.11, but .python-version should win

## Files Present
- .python-version - 3.8.10 (SHOULD WIN)
- pyproject.toml - requires-python = ">=3.11" (SHOULD BE IGNORED)
- requirements.txt - Contains dependencies

## Test Purpose
Critical test: Validate highest priority file wins in conflict scenario.
