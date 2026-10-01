---
on: workflow_dispatch
engine: copilot
model: gpt-4o
permissions:
  contents: read
  issues: read
tools:
  github:
    toolsets: [default]
  web-fetch: 
network:
  allowed:
    - defaults
    - "wttr.in"
safe-outputs:
  create-issue:
---

# Instructions
1. Invent or pick a completely random, well-known city somewhere in the world (e.g., Tokyo, Paris, Cairo, Lima, Reykjavik). 
2. Use your web-fetch tool to check the current live weather conditions for that random city by sending an HTTP request to: http://wttr.in
3. Take the raw weather data returned by the tool, format it into a friendly, beautiful message, and post it as a brand new issue in the repository.
4. Title the issue: "Random Weather Report: [City Name]"
5. If the weather fetch fails or no city data is found, you MUST call the `noop` tool with a message explaining why: {"noop": {"message": "No action needed: [brief explanation]"}}
