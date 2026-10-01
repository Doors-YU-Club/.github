# Doors GitHub maintainer playbook

This is the club's starting access model. Update it through a pull request when the leadership structure changes.

## Roles

| Role | Access | Use |
| --- | --- | --- |
| Organization owner | Full organization administration | A small number of trusted, named people responsible for continuity. Keep at least two active owners. |
| Tech Maintainers team | Triage on current project repositories | Coordinate issues and reviews while private branch protection is unavailable. |
| Tech Contributors team | Triage on current project repositories | Claim and organize issues without a direct push path. |
| Other club members | No default repository access | Grant Read or Triage on specific repositories when their work calls for it. |

Every person uses their own GitHub account with two-factor authentication. Do not use a shared club login. The club email is for contact or billing, not a root account.

An additional Owner is a continuity backup, not an exemption from the review workflow. The president and every other Owner must use a branch and PR for code, content, documentation, configuration, and workflow changes; request `@gqnxx` and wait for their explicit approval before merge. No self-approval or self-merge. The president's approval of public event content is a separate decision and does not replace `gqnxx`'s review of repository changes. If the designated reviewer changes at leadership handover, update this rule and CODEOWNERS through a reviewed PR first.

## Starting a repository

1. Create **private** project repositories only. The `.github` repository is public to display the organization profile and shared contribution guidance. A deployed website can be public while its source repository remains private. Do not put student records or credentials in either place.
2. Create from [`doors-project-template`](https://github.com/Doors-YU-Club/doors-project-template). Replace the placeholders in `README.md` and `AGENTS.md`.
3. Give teams **Triage** initially. Grant Write or Maintain only to named people when their work requires it and the organization owner accepts the current branch-control limitation. Keep Admin with owners.
4. Keep `CODEOWNERS` pointed at `gqnxx` until a named reviewer has Write or Maintain; GitHub only requests reviews from code owners with sufficient access.
5. Add actual build, test, and lint commands, then run them in CI. Use branches and pull requests for all changes. **GitHub Free does not enforce branch protection on private organization repositories**; the API returns HTTP 403. The club will stay on Free, so this remains a team policy rather than a technical lock. Do not start a trial, upgrade, or change project repository visibility. Before granting a named coder Write access, explain the direct-`main` risk to `gqnxx`.
6. Record where secrets live and how to report security issues. Do not store real secrets in Git.

## Current projects

- The university plans to create the permanent club website and hand it over later. Handover details are not known. The club's earlier `doors-club-website` repository was deleted at the owner's request on 2026-10-01; do not direct members to it.
- [`mental-health-awareness-2026`](https://github.com/Doors-YU-Club/mental-health-awareness-2026) is the private, time-limited event site project. Event details are tentative until leadership confirms them. The president has supplied a [public card-explorer MVP](https://singular-mochi-b53902.netlify.app/) hosted outside this repository. Its source, deployment ownership, content, rights, and accessibility need review before the committee reuses it. The requested Boost messages board is tracked in the event issues.

The event repository has unassigned issues for volunteers, including noncoding tasks and a repo lead opening. Its workflow explains how to claim work. Its source remains private; a public MVP exists separately on Netlify. Do not treat the MVP's existence as approval of new code or content.

## Handover and routine review

- Before an owner or project lead leaves, appoint a successor, verify their access, and update billing if necessary.
- Review team membership and repository access each term and remove access that is no longer needed.
- Review GitHub Apps, deploy keys, tokens, and Actions secrets before reusing an old project.
- Revisit branch protection whenever a project gains reviewers or CI checks. Avoid rules that no current member can satisfy.
