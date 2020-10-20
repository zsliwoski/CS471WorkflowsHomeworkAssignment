---
name: '#1 User Story'
about: 'The only user story for this assignment'
title: 'Workflow Integrating Strategies'
labels: story
assignees: ''

---

As a developer, I need to understand how to create pull requests (PRs) linked to tasks, how to integrate changes from branches into the master branch using different workflow integration strategies and how to correctly establish traceability between commits and tasks (and pull requests), so that I will be proficient and effective in working in the remaining sprints of the group project, while emphasizing and practicing software engineering techniques for writing high quality software.

**Acceptance Criteria:**
- [ ] Given a branch with the name `task-<ID_of_task_it_implements>_<some_short_task_description>` containing changes that are not yet integrated into `master`, when a new pull request is created (having the **base** branch `master` and the **compare** branch `task-<ID_of_task_it_implements>_<some_short_task_description>`), then the description of the PR should reference the task it implements (i.e., `#<ID_of_task_it_implements>`)
- [ ] Given the PR for branch `task-2_merge`, when the branch is integrated into `master`, then the `Merge pull request` integration option of the PR should be used, and the commit message should be the default one provided by GitHub (e.g., `Merge pull request #<ID_PR> from <yourGitHubUserName>/task-2_merge`)
- [ ] Given the PR for branch `task-3_rebase`, when the branch is integrated into `master`, then the `Rebase and merge` integration option of the PR should be used
- [ ] Given the PR for branch `task-4_squash`, when the branch is integrated into `master`, then the `Squash and merge` integration option of the PR should be used, and the commit message should be the default one provided by GitHub (e.g., `Task 4 squash (#<ID_PR>)`)
- [ ] Given the PR for branch `task-5_squash_with_link_to_task`, when the branch is integrated into `master`, then the `Squash and merge` integration option of the PR should be used, and the commit message should be `Closes #5 (#<ID_PR>)`; In this way, any developer inspecting the commit in `master` can directly navigate to task `#5` or to the PR (to see all the intermediate commits for the implementation)
- [ ] Given the PR for branch `task-6_squash_preferred_project_workflow`, when the branch is integrated into `master`, then the `Squash and merge` integration option of the PR should be used, and the commit message should be `Closes #6 (#<ID_PR>)`; In this way any developer inspecting the commit in `master` can directly navigate to task `#6` (which will be referenced by only one "atomic" commit containing the final implementation of the task) or to the PR (which will contain all the intermediate commits for the implementation, without any traceability to the task)
- [ ] Given a PR for a branch with the name `task-<ID_of_task_it_implements>_<some_short_task_description>`, when the changes from the branch are successfully integrated into `master` and the PR is closed, then the branch is deleted (using the GitHub interface)
