---
layout: post
title: "Jenkins 2.0: Makes it easy for organisations to deliver software continuously"
date: 2016-4-28
categories: jenkins
tags: jenkins
excerpt_separator: <!--more-->
---

I have spent the last 3 years of my life helping Jenkins claim its
place upfront and central in the Continuous Delivery market. The
journey first started by providing first class support for CD
pipelines through Jenkins Pipelines and has culminated in the first
major release of Jenkins in 10 years. I am incredibly privileged to
have helped Kohsuke Kawaguchi in this journey. The following is a blog
post that I put out on cloudbees.com for the release.
<!--more-->

Jenkins 2.0 is generally available now. It is the first major release
of Jenkins in 10 years after about 700 weekly releases. It is indeed a
major milestone in the Jenkins project. The primary focus of the
release is Pipelines - a means to helping organisations deliver better
software faster.

**Why should I care?**

A fair enough question so I will wear a different
“I” hat and answer why Jenkins 2.0 is relevant to you.

**Role**: Engineering Manager

**Key Issue**: My team delivers an application from development to production - what does Jenkins 2.0 bring to the table?

*Pipelines: An easy to use DSL to model, view and optimise your
 application delivery value stream that can significantly improve the
 pace of delivery for your applications.*{:.underline}

Jenkins 2.0 natively supports the notion of pipelines and helps to
model your delivery pipeline through a DSL that is checked into the
source code repository (Jenkinsfile). This file can then be version
controlled and shared with other teams.

If your team was using multiple (existing) Jenkins plugins to model
your pipeline, Pipelines greatly simplifies expressing the delivery
pipeline, maintaining and managing it.

Pipeline stage view helps your team analyse the performance of the
delivery pipeline and hone in on problematic stages in the delivery
chain.
![Pipeline Stage View](https://www.cloudbees.com/sites/default/files/jenkins2-harpreet-blog-1.png)

Pipelines support GitHub and BitBucket organisations and pull requests. Point Jenkins to a GitHub organisation that has a Jenkinsfile checked in, Jenkins will automatically create a job, run and manage it - very useful when onboarding new teams.

**Role**: Shared Services Engineering Manager, VP of Engineering, Tools Group Manager

**Key Issues**:

* My team is responsible for minimizing the impact of downtimes for
various teams that depend on the tools supplied by my team.

* My team is responsible for fostering best practices across
engineering groups delivering applications.

Pipelines survive infrastructure outages; common delivery patterns can
be stored in global libraries that are shared across various teams.

Pipelines are durable and resumable. Thus, if you support an
engineering team whose application delivery spans multiple days, you
can support them with the confidence to know that pipelines has
inbuilt resilience to survive infrastructure failure. The pipeline job
continues running even if the master fails. If you use CloudBees
Jenkins Platform - your job can resume from the last checkpoint on
executor failures.

Pipelines follow the DRY principle - your team can capture common
deliverability patterns (“deploy to Tomcat”) into functions that can
be invoked by teams that you support. Thus, your team can share best
practices within the organisation.

**Role**: An existing Jenkins user

**Key Issue**: Any usability improvements?

Besides Pipelines, Jenkins 2.0 brings in a number of improvements for
usability. Jenkins 1.x configuration page becomes overloaded with
configuration choices introduced by plugins. Improvements to the
configuration management has been an area of focus for Jenkins 2.0.

![Config UI](https://www.cloudbees.com/sites/default/files/jenkins2-harpreet-blog-2.png)

A new startup wizard helps newbies get to a running installation
quickly with a pre-configured set of plugins as well.

**Role**: Jenkins administrator
**Key Issue**: Will an upgrade break an existing installation?

Jenkins 2.0 is backward compatible and a drop-in replacement. So
upgrade without worries.

So go ahead - bring in Jenkins 2.0 and earn good karma within your
organisation

**Resources**:

* [Create a Pipeline](https://jenkins.io/doc/pipeline/)

* [Continuous Delivery microsite on Jenkins.io](https://jenkins.io/solutions/pipeline/)

