---
title: Knative Quickstart plugin
linkTitle: Knative Quickstart
author: "Paul Schweigert, Senior Software Engineer @ IBM"
date: 2021-09-17
description: Knative quickstart is a plugin for the Knative client that enables users to quick set up a local Knative environment from the command line
type: "blog"
---

## Announcing the `Quickstart` plugin for Knative

We're pleased to announce that the [`quickstart` plugin](https://github.com/knative-sandbox/kn-plugin-quickstart) for the Knative client is now available. The plugin allows users to very easily set up a local Knative environment with just a single command using a local [KinD](https://kind.sigs.k8s.io/) or [minikube](https://minikube.sigs.k8s.io/) cluster.

```
$ kn quickstart kind
Running Knative Quickstart using Kind
✅ Checking dependencies...
    Kind version is: kind v0.11.1 go1.16.4 linux/amd64

☸ Creating Kind cluster...
    Cluster ready
🍿 Installing Knative Serving v0.25.0 ...
    CRDs installed...
    Core installed...
    Finished installing Knative Serving
🕸️ Installing Kourier networking layer v0.25.0 ...
    Kourier installed...
    Ingress patched...
    Kourier service installed...
    Domain DNS set up...
    Finished installing Kourier Networking layer
🔥 Installing Knative Eventing v0.25.0 ...
    CRDs installed...
    Core installed...
    In-memory channel installed...
    Mt-channel broker installed...
    Example broker installed...
    Finished installing Knative Eventing
🚀 Knative install took: 1m50s
🎉 Now have some fun with Serverless and Event Driven Apps!
```

The plugin provides an easy way to install the main components of Knative (Serving and Eventing) via the command line, using the same tool that you use to create Knative resources...

Use the Knative client to spin up your environment:
```
$ kn quickstart kind
```

Use the Knative client to create a Knative service:
```
$ kn service create hello --image gcr.io/knative-samples/helloworld-go
```

Ready to try it out? Head over to the [Getting Started with Knative](https://knative.dev/docs/getting-started/) guide to learn how to download the plugin and get started with Knative!