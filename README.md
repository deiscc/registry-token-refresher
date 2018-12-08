
# Registry Token Refresher
[![Build Status](https://ci.deis.cc/job/registry-token-refresher/badge/icon)](https://ci.deis.cc/job/registry-token-refresher)
[![Docker Repository on Quay](https://quay.io/repository/deiscc/registry-token-refresher/status "Docker Repository on Quay")](https://quay.io/repository/deiscc/registry-token-refresher)

Deis (pronounced DAY-iss) Workflow is an open source Platform as a Service (PaaS) that adds a developer-friendly layer to any [Kubernetes](http://kubernetes.io) cluster, making it easy to deploy and manage applications on your own servers.

For more information about the Deis Workflow, please visit the main project page at https://github.com/deiscc/workflow.

We welcome your input! If you have feedback, please [submit an issue][issues]. If you'd like to participate in development, please read the "Development" section below and [submit a pull request][prs].

# About
The Registry Token Refresher service creates the [imagePullSecret][imagePullSecrets] and updates it at regular interval of time for each app(namespace) created by Deis Workflow. The secrets are used by [dockerbuilder][dockerbuilder] and [controller][controller] for authenticating with the private registry.

This service is run only when using Amazon's [ECR][ecr] or Google's [GCR][gcr] as they provide short lived tokens for authentication.

[issues]: https://github.com/deiscc/workflow/issues
[prs]: https://github.com/deiscc/workflow/pulls
[imagePullSecrets]: http://kubernetes.io/docs/user-guide/images/#specifying-imagepullsecrets-on-a-pod
[dockerbuilder]: https://github.com/deiscc/dockerbuilder
[controller]: https://github.com/deiscc/controller
[ecr]: http://docs.aws.amazon.com/AmazonECR/latest/userguide/ECR_GetStarted.html
[gcr]: https://cloud.google.com/container-registry/
[v2.18]: https://github.com/deiscc/workflow/releases/tag/v2.18.0
