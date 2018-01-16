# gitflow-experiment
Testing for gitflow's compatibility with GitHub PRs and the fork
model.

## Setup
* On GH, make a fork of RWGPS/gitflow-experiment.git
* clone your fork onto your computer

```git clone git@github.com:<your-GH-username-here>/gitflow-experiment.git```

* setup an "upstream" remote to point to RWGPS central repo

```git remote add upstream git@github.com:ridewithgps/gitflow-experiment.git```

* setup to track the RWGPS "upstream" remote develop branch as our local "develop"

```git branch -u upstream/develop develop```

## Work on a new feature off of the develop branch.
This would be done for each GH issue during a feature development cycle.

```git-flow feature start myfeature```

* Do some editing, commit, etc.
* Now, publish this work to your fork (this does to ```your-fork/myfeature```)

```git-flow feature publish```

* Make a PR on GitHub from the newly published branch of your fork on RWGPS upstream repo
* Get a review, merge the PR
* Now, back on your machine, close out the feature branch:

```git-flow feature finish```

