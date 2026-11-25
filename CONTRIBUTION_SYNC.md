# Contribution heatmap sync

The portfolio refreshes the GitHub contribution calendar in GitHub Actions. For the simplest upload-only setup, first enable **Show private contributions on my profile** in your GitHub profile's contribution settings. GitHub will then make the daily private contribution counts visible as aggregate counts, without showing private repository names or code. The existing public-calendar refresh can include those counts without a token.

If you do not want to display those aggregate counts publicly, the optional authenticated route is an Actions secret:

1. Create a GitHub personal access token for your own account with the `read:user` scope.
2. In this repository, open **Settings → Secrets and variables → Actions → New repository secret**.
3. Name it `PROFILE_GITHUB_TOKEN` and paste the token as its value. Do not put the token in a project file or share it in chat.
4. Run **Actions → Refresh profile heatmap → Run workflow**. When it finishes, the saved local graph and portfolio deployment will use the refreshed calendar.

GitHub only includes private contribution counts when your profile is configured to share those counts. The graph shows daily totals; it does not publish private repository names or code.
