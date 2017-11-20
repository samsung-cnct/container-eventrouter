# container-eventrouter 

A container repository for Heptiolabs eventrouter.  This defines the Dockerfile and CI/CD pipeline to build, test, and deploy an eventrouter image.  The image will be named `eventrouter-container` and hosted by Samsung CNCT.

We use GitLab to implement our CI/CD pipelines. There is one GitLab repository for 
each GitHub repository. Each job builds, tests and, then deploys an artifact
to Quay.


# Purpose 

Deploy eventrouter to Kubernetes using [this helm chart](https://github.com/samsung-cnct/chart-eventrouter/).
Eventrouter is used to get events from the kubernetes api server and write them to stdout.  
We have EFK logging installed in Kubernetes.  Fluentbit or Fluentd send stdout messages to Elasticsearch. Kibana
is used to view the kubernetes events.
