# Doors GitHub maintainer playbook

This is the club's starting access model. Update it through a pull request when the leadership structure changes.

## Roles

| Role | Access | Use |
| --- | --- | --- |
| Organization owner | Full organization administration | A small number of trusted, named people responsible for continuity. Keep at least two active owners. |
| Tech Maintainers team | Maintain on assigned repositories | Review and merge project work; manage routine repo settings without broad organization control. |
| Tech Contributors team | Write on assigned repositories | Develop on branches and open pull requests. |
| Other club members | No default repository access | Grant Read or Triage on specific repositories when their work calls for it. |

Every person uses their own GitHub account with two-factor authentication. Do not use a shared club login. The club email is for contact or billing, not a root account.

## Starting a repository

1. Choose public or private visibility based on the data and the club's publication permission. Do not put student records, credentials, or unpublished material in a public repository.
2. Create from [`doors-project-template`](https://github.com/Doors-YU-Club/doors-project-template). Replace the placeholders in `README.md` and `AGENTS.md`.
3. Give Tech Maintainers **Maintain** and the assigned contributor team **Write**. Keep Admin with owners unless a specific person needs it.
4. Confirm that `CODEOWNERS` names a team with Write or Maintain access to the repository.
5. Add actual build, test, and lint commands, then run them in CI. Protect `main` and require a pull request. Require one human approval once at least two active reviewers are available.
6. Record where secrets live and how to report security issues. Do not store real secrets in Git.

## Handover and routine review

- Before an owner or project lead leaves, appoint a successor, verify their access, and update billing if necessary.
- Review team membership and repository access each term and remove access that is no longer needed.
- Review GitHub Apps, deploy keys, tokens, and Actions secrets before reusing an old project.
- Revisit branch protection whenever a project gains reviewers or CI checks. Avoid rules that no current member can satisfy.
