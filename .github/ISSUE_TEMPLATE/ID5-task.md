---
name: '#5 Task'
about: 'Task that should be linked to user story #1'
title: 'Squash with Traceability to Task and PR in Commit Message Integration Strategy, but with Some Commits in the Branch Referencing the Task'
labels: ''
assignees: ''

---

References user story #1

NOTE: there are commits in the branch `task-5_squash_with_link_to_task` that are referencing the task `#5`

## TODO:
- [ ] Create a new PR having the **base** branch `master` and the **compare** branch `task-5_squash_with_link_to_task`
- [ ] Edit the description of the PR to reference this task
- [ ] Understand the commits and changes made to the PR
- [ ] In the PR, use the `Squash and merge` option to integrate the changes into `master` and the commit message should be `Closes #5 (#<ID_PR>)`, and **remove the extended description in the squashed commit, which lists the individual commits that are in the pull request**
- [ ] Use the GitHub interface to delete the branch of the PR after successfully integrating it into `master`

## Advantage of this workflow
:thumbsup: Any developer inspecting the commit in `master` can directly navigate
- to task `#5` or
- to the PR (to see all the intermediate commits for the implementation)

## Disadvantage of this workflow
:heavy_exclamation_mark: If the branch contains commits (having partial implementations of the task) that are referencing task `#5` (like is the case for branch `task-5_squash_with_link_to_task`), these commits will automatically appear in task `#5` as being referenced, and this may unnecessarily clutter task `#5` and confuse any developer trying to understand the changes performed in task `#5`