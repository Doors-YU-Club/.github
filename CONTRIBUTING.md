# Contributing to Doors YU Club projects

We welcome members who are learning. Clear communication and review matter more than perfect code on the first try.

1. Read the project's `README.md`, `AGENTS.md`, and open issues before starting. Ask a maintainer when the goal or access level is unclear.
2. Open or claim an issue for work that needs coordination. For a small fix, explain the problem in your pull request.
3. Work on a branch. Keep a pull request focused on one change and describe what changed, why, and how you checked it.
4. Run the project's documented checks. If a check could not run, say so in the pull request.
5. Contributors other than `gqnxx` must request owner review, address comments, and wait for explicit approval before merge. If `gqnxx` authored the PR and no independent reviewer is available, the owner may personally inspect the full diff and checks, leave a short review note, and merge it. This does not allow direct pushes to `main`.

Every code, content, documentation, configuration, and workflow change goes through a branch and pull request. Do not push directly to `main` or use Owner access to bypass review. On private GitHub Free repositories, GitHub cannot enforce this rule technically; it is a mandatory team rule. Report any accidental direct push to `gqnxx` immediately and document the correction.

## AI-assisted work

AI tools may help with learning, drafting, and coding. The member submitting the work remains responsible for understanding and verifying it.

- Give the tool the project's instructions and relevant context. Check its claims against the actual code and documentation.
- Never paste passwords, tokens, private student information, or unpublished club material into an AI service without authorization.
- Review every generated change and dependency. Do not merge code solely because an AI tool or test says it is correct.
- State in the pull request where AI materially helped and what you verified yourself. This is for review clarity, not a penalty.
- AI agents may prepare a branch and PR, but may merge only when `gqnxx` explicitly authorizes that specific merge after review. They must not push to `main`, change review or access settings, deploy, or publish without specific authorization from `gqnxx` for that action. AI output does not count as human review.

Do not commit secrets or personal data. Use local environment files excluded by `.gitignore` and the project's approved secret storage.
