---
on: daily
engine: copilot
permissions:
  contents: read
  issues: read
  pull-requests: read
  copilot-requests: write
tools:
  github:
    toolsets: [default]
safe-outputs:
  create-issue:
---

# Daily Repo Status Report

You are a repository health assistant. Look over the recent commits, newly opened issues, and active pull requests in this repository. Compile a brief, punchy bulleted summary highlighting what was worked on recently and what open tasks might need attention. Post this summary as a new issue titled "Daily Repository Status Report".
