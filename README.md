# gitflow-experiment version 1.8.3
Testing for gitflow's compatibility with GitHub PRs and the fork
model.

## Setup
* On GH, make a fork of RWGPS/gitflow-experiment.git
* clone your fork onto your computer

```git clone git@github.com:<your-GH-username-here>/gitflow-experiment.git```

* setup an "upstream" remote to point to RWGPS central repo

```git remote add upstream git@github.com:ridewithgps/gitflow-experiment.git```

* setup to track the RWGPS "upstream" remote develop and master branches

```git branch -u upstream/develop develop```
```git branch -u upstream/master master```

* get all the things

```git fetch --all```

## Work on a new feature off of the develop branch.
This would be done for each GH issue during a feature development cycle.

```git-flow feature start feature-xxx```

* Do some editing, commit, etc.
* Now, publish this work to your fork (this does to ```myfork/feature-xxx```)

```git-flow feature publish```

* Make a PR on GitHub from the newly published branch of your fork on RWGPS upstream repo
* Get a review, merge the PR
* Now, back on your machine, close out the feature branch:

```git-flow feature finish```
* Notice that branch has now been deleted from your local repo as well.

## Make a new release
* Make a new release branch off of develop

```git flow release start release_1.8.1```

* Do some more editing and committing, like you do
* Make PRs for any final fixes?
* When done, run

```git flow release publish```

