---
allowed-tools: Bash, Grep, Read, Edit
description: Run Django tests and check for non-local URLs

---

## Your Task
- Before run them check if we are in the pipenv shell, if now start it.
- Run all Django tests using `pipenv run pytest apps common --cov=./ --cov-report xml --color=yes --durations=20 -n auto --timeout=780`
- Search for URLs in test files that point to non-local endpoints
- Check common test configuration files for external URLs:
  - `settings/test.py` or `settings.py`
  - Test files in `tests/` directories
  - Any `conftest.py` files
- Replace any non-local URLs (http/https external domains) with localhost equivalents and at the end of them revert to the original ones.
- Report which URLs were changed and verify tests still pass
- check if some test is failing
- Missing coverage?