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

## Starting a repository

1. Create **private** repositories only. A deployed website can be public while its source repository remains private. Do not put student records or credentials in either place.
2. Create from [`doors-project-template`](https://github.com/Doors-YU-Club/doors-project-template). Replace the placeholders in `README.md` and `AGENTS.md`.
3. Give teams **Triage** initially. Grant Write or Maintain only to named people when their work requires it and the organization owner accepts the current branch-control limitation. Keep Admin with owners.
4. Keep `CODEOWNERS` pointed at `gqnxx` until a named reviewer has Write or Maintain; GitHub only requests reviews from code owners with sufficient access.
5. Add actual build, test, and lint commands, then run them in CI. Use branches and pull requests for all changes. **GitHub Free does not enforce branch protection on private organization repositories**; the API returns HTTP 403. To technically require PRs on private repositories, move to a plan that supports it, then configure protection on every `main` branch, including admins, with no bypass. Require one approving human review once a second active reviewer can approve the owner's PRs.
6. Record where secrets live and how to report security issues. Do not store real secrets in Git.

## Current projects

- [`doors-club-website`](https://github.com/Doors-YU-Club/doors-club-website) is the permanent club site project.
- [`mental-health-awareness-2026`](https://github.com/Doors-YU-Club/mental-health-awareness-2026) is a separate time-limited event site project. Event details are tentative until leadership confirms them. The supplied burnout-card prototype is reference material and must pass content, source, rights, and accessibility review before publication.

Both repositories have unassigned issues for volunteers, including noncoding tasks and a repo lead opening. The project workflow documents explain how to claim work. The projects are private, and neither is deployed yet.

## Handover and routine review

- Before an owner or project lead leaves, appoint a successor, verify their access, and update billing if necessary.
- Review team membership and repository access each term and remove access that is no longer needed.
- Review GitHub Apps, deploy keys, tokens, and Actions secrets before reusing an old project.
- Revisit branch protection whenever a project gains reviewers or CI checks. Avoid rules that no current member can satisfy.
