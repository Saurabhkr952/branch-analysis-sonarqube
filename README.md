# branch-analysis-sonarqube(Supported in Developer Version)
To scan specific branch in sonarqube.

[SonarQube Branch Analysis Official Docs](https://docs.sonarsource.com/sonarqube-server/latest/analyzing-source-code/branch-analysis/setting-up-the-branch-analysis/#limit-to-relevant-branches)



### In Jenkins there is two pipeline options:

- New Item -> Pipeline --> `env.BRANCH_NAME` return branch `null`
- New Item -> Multibranch Pipeline --> `env.BRANCH_NAME` return branch `master` or `branch name`


- the pipeline job I'm using `env.GIT_BRANCH` which resolves to `origin/{BRANCH}`

