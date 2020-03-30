---
title: Amazon States Language
date: 'Mon, 30 Mar 2020 10:03:07 -0700'
stacks: []
---

I've discovered [Amazon States Language](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-amazon-states-language.html)

It's the AWS Step Functions way to chain tasks, to create workflows and build a state machine for data processing.

It's interesting, and much more usable than [WDL](https://github.com/openwdl/wdl), which I found to be too cumbersome and not user-friendly at all.

Unlike OpenWDL, which has three workflow engines to support it - Cromwell, MiniWDL, and dxWDL, ASL only has one - AWS Step Functions.

It's custom built and since it's JSON, it's quite well suited for the task.

However, I'm going to create an engine to parse ASL and use it for my own workflows. There are examples of LocalStack, and [Serverless Framework](https://github.com/serverless-operations/serverless-step-functions) and a repo called [Local Step Functions](https://github.com/fadams/local-step-functions) which talks about letting us run Step Functions locally. It even has a WIP engine called [asl-workflow-engine](https://github.com/fadams/local-step-functions/tree/master/asl-workflow-engine) which can potentially parse ASL JSON and also execute against it.

I even found a python library called [StairStep](https://github.com/adamgilman/stairstep) which can create ASL output programmatically, but it's incomplete - it doesn't have the Map function, which is one of the main things I need. 


