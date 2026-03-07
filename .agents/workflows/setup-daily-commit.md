---
description: how to set up and manage the daily commit automation
---

# Daily Commit Setup Workflow

This workflow helps you set up and manage the daily commit automation.

// turbo

1. **Initialize Git (if not done)**:

   ```powershell
   git init
   git add .
   git commit -m "chore: initial setup for daily committer"
   ```

2. **Connect to GitHub**:
   - Create a new repository on GitHub.
   - Run the following command (replace `<URL>` with your repo URL):

   ```powershell
   git remote add origin <URL>
   git branch -M main
   git push -u origin main
   ```

3. **Verify Permissions**:
   - Go to your GitHub repository -> **Settings** -> **Actions** -> **General**.
   - Scroll down to **Workflow permissions**.
   - Select **Read and write permissions**.
   - Click **Save**.

4. **Trigger Manually (Optional)**:
   - Go to the **Actions** tab in your GitHub repository.
   - Select the **Daily Heartbeat Commit** workflow.
   - Click **Run workflow**.

5. **Check Status**:
   - You can see the history of daily commits in the `heartbeat.txt` file on GitHub or by checking the repository's commit history.
