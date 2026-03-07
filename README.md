# Daily Committer

This repository is configured to automatically commit a "heartbeat" every 24 hours using GitHub Actions.

## Setup Instructions

1.  **Create a Repository**: Create a new repository on GitHub.
2.  **Add Remote**: Run `git remote add origin <your-repo-url>` in this directory.
3.  **Push Code**: Run `git push -u origin main`.
4.  **Enable Permissions**: Go to **Settings > Actions > General** in your GitHub repository and ensure "Workflow permissions" is set to "Read and write permissions".

## How it Works

The GitHub Action defined in `.github/workflows/daily_commit.yml` runs every day at midnight (UTC). It updates `heartbeat.txt` with the current timestamp and pushes the change back to the repository.
