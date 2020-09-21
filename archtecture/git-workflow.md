## Git Workflow Strategy

#### Requirments
- Create Git workflow for CI/CD.

#### Architecture
- Traditional git flow
  - Develop branch from master branch.
  - Release branch from develop branch.
  - Feature / bugfix branch from release branch.
  - Developers commit to feature / bugfix branch.
  - Merge release branch to develop branch after test.
  - Merge develop branch to master branch to deploy.
![git-flow](./images/git-flow-1.png)

- Git flow for CI/CD
  - Staging branch from production branch.
  - Develop branch from staging branch.
  - Topic branch from develop branch.
  - Developers commit to topic branch.
  - Merge topic branch to develop branch after local test, and use **--squash option** to maintain one commit for one feature.
  - Merge develop branch to staging branch with **interative rebase** to select feature to deploy.
  - Merge staging branch to production branch after production environment test.
  ![git-flow](./images/git-flow-2.png)

#### Reference
- [Reid Blog](https://blog.ull.im/engineering/2019/06/25/git-workflow-for-ci-cd.html)
- https://velog.io/@godori/Git-Rebase
