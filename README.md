# daily_inspiration

Daily inspirational emails generated with Ollama and sent using GitHub Actions.

## Setup

1. Enable 2-Step Verification on your Google Account and create an
   [App Password](https://support.google.com/accounts/answer/185833) for Gmail.
   Do not use your regular account password.
2. In your repository's **Settings > Secrets and variables > Actions**, add
   these repository secrets:
   - `MAIL_USERNAME`: your full Gmail address.
   - `MAIL_PASSWORD`: the Gmail App Password.
   - `MAIL_TO`: the recipient address, or a comma-separated list of addresses.
3. Ensure GitHub Actions is enabled and the workflow is on the default branch.
   To test it, select **Actions > Daily Inspirational Quote > Run workflow**.

The workflow runs daily at 13:00 UTC (7:00 AM CST / 8:00 AM CDT). GitHub may
delay scheduled runs, and the local time changes with daylight saving time.
The first run downloads the `qwen3:4b` model; later runs can reuse the cached
model. Runtime depends on the runner, download, and model inference.
