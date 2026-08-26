# design-lead — project context
Memory: see _brain.md. Status/decisions live there.

Public skill pack (repo private until launch). Personal state goes in LOCAL.md (gitignored), never in tracked files.

## Build / Run / Test
- No build step (Markdown pack). Lint gate for any example HTML: `npx -y @gessobuild/anti-slop check <file>`.
