# Workflow Strategies for Integrating/Merging Pull Requests and Establishing Traceability between commits and tasks (and pull requests).

## Step 1 - Create a New Repository
Using your personal GitHub account [create new a GitHub repository](https://github.com/new) called `CS471WorkflowsHomeworkAssignment`.
- The following option: `Initialize this repository with a README` should be **disabled**/**unchecked**.

## Step 2 - Clone Starter Code Repository
Clone this [CS471-Assignments-Workflows](https://github.com/BoiseState/CS471-Assignments-Workflows) repository.

```bash
$ git clone https://github.com/BoiseState/CS471-Assignments-Workflows.git

$ cd CS471-Assignments-Workflows
```

## Step 3 - Push the Cloned Code to the New Repository
The contents of `master` branch of the **cloned repository** (from [`Step 2`](#step-2)) will be pushed the **repository that you created** (in [`Step 1`](#step-1)).

### Step 3a
Check the existing `origin` remote, which should indicate the URL of the cloned repository:
```bash
$ git remote --verbose
origin  https://github.com/BoiseState/CS471-Assignments-Workflows.git (fetch)
origin  https://github.com/BoiseState/CS471-Assignments-Workflows.git (push)
```

Inspect the history of the repository via:
- the GitHub [visualization](https://github.com/BoiseState/CS471-Assignments-Workflows/network) and
- the command line:
```bash
$ git log --oneline --decorate --graph --all --author-date-order
```

### Step 3b
Create local branches from all remote branches:
```bash
$ for remote_branch in `git branch -r | grep -v HEAD | grep -v master`
do
    # the ${remote_branch#"origin/"} means remove (#)
    # the pattern "origin/" from the string variable ${remote_branch}
    # to end up with the name of the local branch
    git branch ${remote_branch#"origin/"} $remote_branch
done
```

### Step 3c
Remove the `origin` remote pointing to the cloned repository:
```bash
$ git remote remove origin
```

Add a new `origin` remote that will point to the repository that you created (in [`Step 1`](#step-1)):
```bash
$ git remote add origin https://github.com/<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git
or
$ git remote add origin git@github.com:<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git

$ git remote --verbose
origin  https://github.com/<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git (fetch)
origin  https://github.com/<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git (push)
or
origin  git@github.com:<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git (fetch)
origin  git@github.com:<GitHubUsername>/CS471WorkflowsHomeworkAssignment.git (push)
```

### Step 3d
Push only the `master` branch to your newly create repository (in [`Step 1`](#step-1)):

```bash
$ git push -u origin master
```

## Step 4 - Create a User Story and Tasks
In your `CS471WorkflowsHomeworkAssignment` repository created in [`Step 1`](#step-1), go to `Issues` -> `New issue` and **create one type of each of the six issues** (i.e., one user story and five tasks), in the ascending order specified.

NOTE: The [GitHub issue templates](https://help.github.com/en/github/building-a-strong-community/configuring-issue-templates-for-your-repository) have already been [configured](.github/ISSUE_TEMPLATE) to create these issues with ease.

At the end of this step, you should have the following issues created:

Issue ID | Issue Type | Title
-------- | ---------- | -----
`#1`     | User Story | Workflow Integrating Strategies
`#2`     | Task       | Merge Integration Strategy
`#3`     | Task       | Rebase Integration Strategy
`#4`     | Task       | Squash with Default Message Integration Strategy
`#5`     | Task       | Squash with Traceability to Task and PR in Commit Message Integration Strategy, but with Some Commits in the Branch Referencing the Task
`#6`     | Task       | Squash with Traceability to Task and PR in Commit Message Integration Strategy, without Any Commits in the Branch Referencing the Task

## Step 5 - Understand the User Story and Tasks
Read and understand the user story `#1`, and the tasks `#2`, `#3`, `#4`, `#5` and `#6` which are all linked to user story `#1`.

## Step 6 - Push All Remaining Local Branches
Push **all** remaining local branches to your newly create repository (in [`Step 1`](#step-1)):
```bash
$ git push --all
```

## Step 7
Complete task `#2` according to its specifications.

Answer the corresponding questions in the [Blackboard](https://blackboard.boisestate.edu/) assignment.

## Step 8
Complete task `#3` according to its specifications.

Answer the corresponding questions in the [Blackboard](https://blackboard.boisestate.edu/) assignment.

## Step 9
Complete task `#4` according to its specifications.

Answer the corresponding questions in the [Blackboard](https://blackboard.boisestate.edu/) assignment.

## Step 10
Complete task `#5` according to its specifications.

Answer the corresponding questions in the [Blackboard](https://blackboard.boisestate.edu/) assignment.

## Step 11
Complete task `#6` according to its specifications.

Answer the corresponding questions in the [Blackboard](https://blackboard.boisestate.edu/) assignment.
