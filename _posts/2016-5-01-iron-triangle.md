---
layout: post
title: "Escape the Iron Triangle - ship better software faster and cheaper with Jenkins Pipelines."
date: 2016-5-01
categories: jenkins
tags: jenkins
---

![continuos software delivery](https://media.licdn.com/mpr/mpr/jc/AAEAAQAAAAAAAAhYAAAAJDU5ZjVkYWI1LTUxZjUtNDA4My04M2M4LTBjMmFmNjE4ZDJlYw.png)
Delivering software continuously, in other words "keeping software in
an always shippable state" is a challenge for companies. Recently
released Jenkins 2.0, is focussed on solving this problem through
**Pipelines**. This blog gives a quick overview of key benefits of Jenkins
Pipelines.

# Executive Summary


Software delivery in any organisation is a complex process that spans
tools, is hand-stitched and fragile. In-efficiencies and failures in
the process have a **make or break** effect on an applications success in
the market place.

Jenkins Pipelines **automates** the process through code, connecting into
the gargantuan number of tools of used by companies for software
delivery. Once modelled, teams get insights into their delivery
performance - to optimise their delivery times. Pipelines survive
infrastructure failures and thus teams can deliver applications
on-time, every time.

A month early due to a stream lined process is a month's revenue while
a month late in delivery due to infra failures is a month that
competition can steal your customers!

# Why Continuous Delivery (CD)?

Accelerating the pace of software delivery mandates code in an always
shippable state and Continuous Delivery is the process that takes
software to the always shippable state.

"Thou shalt choose between good, fast or cheap" said the Iron Triangle
of software delivery. Continuous Delivery upends that case to help
teams deliver good software, faster and cheaper .

# Why Jenkins?


Software goes through various phases (build, test, deploy) and
interacts with a multitude of tools (junit, sonar, nexus etc) on its
way to production. Jenkins is the orchestrator that drives the entire
pipeline and interacts with each of these tools. Jenkins’ strength is
that it has 1200 (and counting) plugins that let you interact with any
of the tools that are in your organisation.

### Jenkins Pipelines


Jenkins 2.0 has introduced a key area called Pipelines. With
Pipelines, organisations can define their delivery pipeline through a
DSL (Pipeline-as-code). Pipelines, thus, can be versioned, checked
into source and easily shared within an organisation.

**Pipelines model YOUR delivery process rather than straight-jacketing you in an “opinionated” process**

Typical delivery value stream within organisations have one
commonality - _atypicality_. Most of the delivery processes are
dissimilar unlike the canonical “build, test, deploy” examples that
you see in examples. Here is an example from an earlier blog from
Viktor Farcic on a delivery pipeline.

![Delivery pipeline](https://www.cloudbees.com/sites/default/files/jenkins2-harpreet-blog2-1.png)


 The Pipeline DSL helps you capture complex process requirements
 through code - thus you can try-catch on deployment failures, loop
 through deployments, run tests in parallel. This is immensely
 powerful - the DSL brings the power of a programming language
 (groovy) to do so. At the same time, the DSL is simple enough to
 capture simple cases easily without having to write groovy code. DSL
 encourages the DRY principle - capture common patterns in functions,
 keep them in a global library so that new applications can build on
 these functions.
![Pipeline-as-code](https://www.cloudbees.com/sites/default/files/jenkins2-harpreet-blog2-2.png)

Pipelines survive infrastructure failures

A number of applications have pipelines that run into multiple days. A
pipeline typically runs on Jenkins executors (slaves) and it will
continue running even in case of a master failure. If you use the
CloudBees Jenkins Platform, you can checkpoint your pipelines so if an
executor fails, you can pick from the last check-pointed location
instead of re-running the pipeline.

You can imagine the productivity benefits on an existing pipeline
where if a master crashed (itself or due to infrastructure failure) on
day 4 of day 7 and it didn’t have to restart from day 1 -
phenomenal. This can mean the difference between shipping on-time or
delays in months!

**Analyse and optimise your value stream process**

Optimising the value stream process is the next logical step after
modelling your delivery process, Pipeline Stage View helps you analyse
the process delivery across multiple runs. You can see which stages
consume the most time, which stages are blocked on manual user input
and so on. Thus, you can quickly hone in on a problematic phase and
optimise it.

![Pipeline stage view](https://www.cloudbees.com/sites/default/files/jenkins2-harpreet-blog2-3.png)

Developers can quickly get an insight into how far is their code into
the pipeline. Teams waiting on artifact delivery on the code can also
see where in the pipeline is the code.

# Summary

Jenkins Pipeline brings in native support for pipelines into
Jenkins. It is aimed at an audience that wants to continuously deliver
software and is well worth a spin.

**Resources**:

* [Create a Pipeline](https://jenkins.io/doc/pipeline/)

* [Continuous Delivery microsite on Jenkins.io](https://jenkins.io/solutions/pipeline/)

