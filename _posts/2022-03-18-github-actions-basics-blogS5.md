---
layout: post
title:  "S5. GitHub Actions Basics"
date:   2022-03-18 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# What is GitHub Actions?

![github-actions](/images/github-actions.png)

GitHub Actions is a GitHub-created service that primarily deals with enabling automation services to software development developers and their companies. These automation services provide ease of test, release, and deployment to companies that manage their code within GitHub repositories. This service bridges the gap between the need for multiple third-party services because GitHub Actions is already built into GitHub. 

# Workflows

In order to start using GitHub Actions, a `workflow` must be created within YAML syntax. These YAML files must also be contained inside a `.github/workflows/` folder.

```
name: Test Terraform Plan (#`O′)
on: [push] 
jobs:
  tf-plan: 
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Test Echo o((>ω< ))o
        run: |
          echo "Hello World!! ┗|｀O′|┛"
          ls -l 
```

After a `git commit` and after any developer makes a push to the repository (as referenced in line 2) teh following code is executed. 

1. name:
> This line is optional and merely names our workflow

2. on: [push]
> This line denotes what will trigger our workflow to begin. Other triggers that may be used are `push`, `pull_request`, `schedule`, `workflow_call`, `workflow_run`, etc. 

3. jobs:
> This line groups together the things that are done in a single job.

4. *new-job-name*:
> This line defines and names one job.

5. runs-on:
> This line configures what virtual machine runner is used for our job. 

6. steps:
> This line groups together the steps that are performed in our job. This can be viewed as shell script or as the individual lines of code written in a terminal.

7. - uses: actions/name-of-action
> This line defines the pre-made action to be used

8. - name: new-step-name
> This line defines and names this action.

9. run:
> This line executes a simple command. 

Below is how the above code would be seen when viewing the results of our example workflow on the GitHub actions GUI. The details of each step and its logs can be seen at each dropdown.

![github-action-ex](/images/github-action-ex.png)

# Workflow Diagram

Below is a simple visual to help piece together how these steps work together.

![overview-actions-event](/images/overview-actions-event.png)

# References

GitHub [https://docs.github.com/en/actions/learn-github-actions](https://docs.github.com/en/actions/learn-github-actions)

GitHub Quick [https://docs.github.com/en/actions/quickstart](https://docs.github.com/en/actions/quickstart)

GitHub Resources [https://resources.github.com/downloads/What-is-GitHub.Actions_.Benefits-and-examples.pdf] (https://resources.github.com/downloads/What-is-GitHub.Actions_.Benefits-and-examples.pdf)