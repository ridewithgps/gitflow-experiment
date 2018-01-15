# gitflow-experiment
# On GH, make a fork of RWGPS/gitflow-experiment.git
# clone your fork onto your computer
git clone git@github.com:<your-GH-username-here>/gitflow-experiment.git
# setup remote to point to RWGPS central repo
git remote add upstream git@github.com:ridewithgps/gitflow-experiment.git
# setup to track the RWGPS "upstream" remote develop branch as our local "develop"
git branch -u upstream/develop develop
