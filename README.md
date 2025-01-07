# branch-analysis-sonarqube
To scan specific branch in sonarqube.

---------------------------------------------------------------------------




### In Jenkins there is two pipeline options:

- New Item -> Pipeline --> `env.BRANCH_NAME` return branch `null`
- New Item -> Multibranch Pipeline --> `env.BRANCH_NAME` return branch `master` or `branch name`



- the pipeline job I'm using `env.GIT_BRANCH` which resolves to `origin/{BRANCH}`

