# solas-container
`solas-container` is scaffolding for new container repositories hosted by Samsung CNCT. It implements our best practices, such as issue and PR templates, commit hooks, licensing guidelines, and so on.

SOLAS is also an international maritime treaty to ensure ships comply with minimum safety standards in construction, equipment and operation.

# Quickstart

- The name of container repos should be of the form `container-${NAME}`. For example, `container-zabra` is the name of the repo which builds a container named `zabra`.
- [Create](https://help.github.com/articles/creating-a-new-repository/) a new empty repo under the [`samsung-cnct`](https://github.com/samsung-cnct) org using the GitHub GUI, for example https://github.com/samsung-cnct/container-zabra .
- [Duplicate](https://help.github.com/articles/duplicating-a-repository/) this repo (https://github.com/samsung-cnct/solas-container) and push it to the `container-zabra` repo you created in the previous step. Note the arguments to clone and push.

```
git clone --bare https://github.com/samsung-cnct/solas-container.git
cd solas-container.git
git push --mirror https://github.com/samsung-cnct/container-zabra.git
cd ..
rm -rf solas-container.git
```

- [Fork](https://help.github.com/articles/fork-a-repo/) the `container-zabra` repo (https://github.com/samsung-cnct/container-zabra) from `samsung-cnct` and begin submiitting PRs.

# What to do next?

- You should configure CI/CD by following the instructions for [GitHub](https://github.com/samsung-cnct/template-chart/blob/master/docs/github.md), [Jenkins](https://github.com/samsung-cnct/template-chart/blob/master/docs/jenkins.md),and [Quay](https://github.com/samsung-cnct/template-chart/blob/master/docs/quay.md).

- You may want to update the teams [Slack notifications](https://samsung-cnct.slack.com/apps/search?q=github) to notify developers of PR and issue activiy. To do this you will need [Admin Privileges](https://help.github.com/articles/repository-permission-levels-for-an-organization/). To ensure that you are not the only one who can maintain these integrations, it is recommended that you grant a GitHub Team (e.g. `commontools`) permissions and not a single individual contributor.

- If your project will be administered by a GitHUb team (e.g. `commontools`), you will need to contact an owner of the `samsung-cnct` organization so they can grant the `commontools` team admin privileges. Reachout in the `#cnct-dev` or `#team-tooltime` Slack channels.

- You will likely need to configure our [Jenkins CI](https://common-jenkins.kubeme.io/) to test, release and deploy changes.
