# HL Bot Reports

Public reporting repository for the autonomous trading strategy:

**TR-F5-Crypto-LS-1H-03**

## Files

- `latest.json` — complete snapshot of the latest bot run
- `index.json` — compact list of recent runs
- `stats.json` — cumulative dashboard statistics
- `account-history.json` — account balance history
- `reports/` — immutable individual run reports

## Data flow

1. The trading routine completes a run.
2. The routine creates a structured JSON report.
3. The latest report replaces `latest.json`.
4. A compact run entry is added to `index.json`.
5. Account values are added to `account-history.json`.
6. Aggregated statistics are updated in `stats.json`.
7. The complete report is stored permanently inside `reports/`.

## Important

This repository is for reporting and visualization only.

It must not contain:

- exchange API keys
- GitHub access tokens
- private account credentials
- Gmail credentials
- SIGNUM credentials
- executable trading controls
