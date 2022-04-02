---
layout: post
title:  "S6. GitHub Actions Part 2"
date:   2022-03-18 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# Core Concepts

GitHub Actions is a platform by which a developer can automate the build, testing, and deployment of their application. This platform has multiple components that help support this goal which are called events, workflows, jobs, actions, and runners. 

## Events

An `Event` is something that happens in our connected Github repository that initially triggers our Github Action workflow. Some of the events that can be utilized are as follows:
'''
create
delete
deployment
fork
issue_comment
issues
pull_request
push
release
schedule
etc.
'''
## Workflows

A `workflow` is the accumulation of everthing that occurs after the initial event begins. Everything that follows this initial start can either begin manually or run at a predetermined time and is determined and coded in a .yml file by the developer.

## Jobs

A `job` essentially containes the individual `steps` that are conducted within each workflow. These steps are performed sequentially and thus require the previous step to sucessfully complete before it can begin. 

## Actions

Similarly to what is done with modularization, an action is another component within the initialized workflow that serves to perform larger, repetitive complex tasks to ease the code that needs to be written. A new action can be custom made by the unique developer or one can be found and used from the GitHub Marketplace.

Some of the available Actions that can be found in GitHub marketplace are as follows:
```
actions/checkout@v2
actions/setup-java@v2
actions/setup-node@v3
aws-actions/configure-aws-credentials@v1
hashicorp/setup-terraform@v1
docker/login-action@v1
```

## Runners

Once a trigger starts up a workflow, a runner is setup that gives our workflow a server to run the processes on. These runners perform tasks individually and sequentially and thus each workflow that is performed is done so on a newly-provisioned virtual machine to give the new workflow a fresh space to work in. This cloud server can be specifie to run any environment customizations.


![image](/images/actions.png)

# References

GitHub [https://docs.github.com/en/actions/learn-github-actions](https://docs.github.com/en/actions/learn-github-actions)
