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

# Integrations Used by the Samsung CNCT Tools Team

- Configure CI/CD by following the instructions for [GitHub](https://github.com/samsung-cnct/solas/blob/master/docs/github.md), [Jenkins](https://github.com/samsung-cnct/solas/blob/master/docs/jenkins.md), and [Quay](https://github.com/samsung-cnct/solas/blob/master/docs/quay.md).

- Configure [Slack](https://github.com/samsung-cnct/solas/blob/master/docs/slack.md) notifications.
