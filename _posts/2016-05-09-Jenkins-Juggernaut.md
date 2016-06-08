---
layout: post
title: "Jenkins - The Juggernaut of Continuous Delivery."
date: 2016-5-09
categories: jenkins
tags: jenkins
---
![Los Hermanos Jenkins](https://media.licdn.com/mpr/mpr/jc/AAEAAQAAAAAAAAdLAAAAJDU3ZDVjMjI2LTU0ODgtNGZjOS1hMzBhLTM4NDVhNTE2MmJkMw.jpg)

# Exec Summary
Today, continuous delivery (CD) is en-vogue. As companies adopt CD, they are faced with a choice on the tools to establish their delivery pipelines. Jenkins is often the obvious choice and best of all it is likely used by the engineering division already. This blog looks at various data points to paint a picture of the pervasiveness of Jenkins for CD.

# Blog
When I started at CloudBees a half a dozen years ago, CD wasn’t in the lexicon - in fact I named “Jenkins Pipelines” feature to be “Workflow” - pipelines is much better! Asking customers about their Dev-to-Production software delivery strategy was often met with a quizzical look.

The four-minute-mile barrier of software delivery was delivering software maybe once-a-month and that barrier has long been broken. Fabled stories of Amazon, Etsy and FaceBook delivering software multiple times a day have set a new bar that every company aspires to.

Google trends shows a continuous (pun intended) rise in the interest of CD. 
![Trends](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAigAAAAJDY1ODdkOGQ2LTMxNDYtNDIxOS04YTMwLTZhZTE2ZmE1MzhjNQ.png)

Since data science is the hottest trend in the market now, I have used data science to provide for a relative scale.
![Data science](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAkdAAAAJGY3ZjY1ZTBkLTA4YjgtNDBmYy05MDU4LTc4YTEzMGFlOWEwMQ.png)

It has been clear that Jenkins is the de-facto CI leader in the market. The ZeroTurnAround survey shows that Jenkins is most adopted CI server in the market with 70% of the market share.

![ZeroTurnaround](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAg4AAAAJDYwOTUwYjdkLWE5ZmItNDAwZi1hYjFjLWMxNzhkYmM5ZWI1MQ.png)

(source: Zeroturnaround)

Active (ones that report active usage) Jenkins installations count is 127k  and growing.
![Active Installations](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAc6AAAAJDhiOWExZmU1LTMxNDQtNDVjNS1iNGE3LWJhZDdiY2EyMDY1Mw.png)

(source: Jenkins stats site)

My guess is that non-reporting installations must be 2-4 times the active installations. Typically, a Jenkins installation supports anywhere between 5-100 people (dev, qa etc) - conservatively this could mean anywhere from 1M+ people using Jenkins (counting 10 developers per active installation).

Let’s look at data from Jenkins Survey in 2013 and 2015 to see some trends.

## Jenkins for Operations 
In the 2 years between the surveys, the usage of Jenkins for operations activities has grown by 9%.

![Jenkins for Operations](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAdSAAAAJGFjYmIzMDViLTg2YWUtNGMzMy1iY2YyLTI4NTQyMGVmZjg4Yg.png)

(source: Jenkins 2013 survey)
![Jenkins Jobs](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAdNAAAAJDY0NWFiY2U5LWFiZmUtNGQ3Ny04ZmRmLWM2ZDQ0ZGI5ZTM3Yw.png)
(source: Jenkins 2015 survey)

## Jenkins for Deployment
The story for deployment is even better with 60% of Jenkins users using the tool for deployment. Note: this number is likely higher as in some cases activities under “release, operations” overlap into the deployment zone. About 70% of those doing deployment are either doing continuous delivery (manual flag to deploy to production) or continuous deployment (auto-deploy).

![Deployment](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAkXAAAAJDMyMDA5MzJkLTRhNWQtNDQwNy1hZmZiLTM1NTQ1NmE4ZGMwNg.png)

(source: Jenkins 2015 survey infographic)

If we take the 127k active installation number and apply it here (70% of 127k)- we have about 88k installations using Jenkins for deployment. Is Jenkins the #1 CD tool in the market? Looks like it!  Can other tools make this claim - doubt it!

83% of deployments happen multiple times a week! Talk about breaking the 4 minutes mile barrier! Delivering is no longer stressful!

![Multiple deployments](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAj1AAAAJGRhN2JmNDFjLTljZTYtNDQ2OC04YTljLThjZDQ5MGQ3NDczOA.png)

## Building modern pipelines with Docker

Last year, the community churned out a number of plugins to help build pipelines with Docker. It is no surprise to now that Jenkins with Docker is a common use case. In other story, Jenkins is the most popular Docker image on Docker Hub with 5M+ (yes million) pulls.

## Increase in the number of plugins

A key reason for Jenkins’ success has been the number of plugins that connect into existing tools. After all, if an organisation brings in a tool to do CD - it has to work with existing tools in the market.

Jenkins has about 1100+ plugins that connect to almost any tool out there. The number of installations of these plugins is north of 4.5M (yes million - it isn't a typo). 
![Usage](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAkCAAAAJDYxM2IxMGRhLTM5ZWMtNGYxNi05MmI1LWIzZmJiNmI0NjI2ZA.png)

No wonder, the actual usage of Jenkins within an organisation keeps increasing with 89% respondents saying that their usage in Jenkins increased.


![Actual usage](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAeRAAAAJDUwMDMxYjk0LTNjZjEtNDNiNy1iY2I0LThhMGNmMjBjMDY4ZA.png)

## Mission Critical Jenkins 
Given that an organisations' entire software delivery chain is dependent on Jenkins, it is no surprise Jenkins is considered mission critical. Between 2013 and today the growth is about 9%. 92% of respondents say that Jenkins is mission critical - not a surprise, given that at-least 50% of developers in organisation are using Jenkins. A colleague asked a question in talk recently “What would happen if Jenkins goes down?”, only to be met with nervous laughter.

![Mission critical](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAi5AAAAJGQ4YTIwNmJhLWY4ZGUtNDNjZC04MzYyLWVlMWNlYjRhM2ViZA.png)

A testament to Jenkins is that 89% of teams are satisfied with Jenkins.
[Satisfaction](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAeUAAAAJGQwZjczZTc4LThiMDgtNDUwZS04NmVlLTViYmM4ZGE0NjRmOQ.png)

This satisfaction shows up in numerous awards!

![Awards](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAegAAAAJGJlMzllNDY1LWMwMGItNDE5My04YThlLTE0ODk5MzNiMzc1Mg.png)

## Increase in the number of jobs - Jenkins jobs
In the last 3 years, the number of jobs created in Jenkins has grown almost 3 times from ~2.25M to 7M.
![Number of jobs](https://media.licdn.com/mpr/mpr/shrinknp_400_400/AAEAAQAAAAAAAAkLAAAAJGQ4OTgxZDViLTZhZWQtNGU4Mi1iN2NiLWI5ZjBhMDIwMTQzMg.png)
 

## Increase in the number of jobs - human jobs
With the increase in Jenkins usage, its usage in CD, there is no surprise that people in the “DevOps” role using Jenkins has more than doubled to 48%.
![Number of human jobs](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAhrAAAAJDAzM2Y0NWRjLTkxNmUtNDYxNS05ZGM3LWEwNjk3NGZjMzc1NQ.png)

## This is somewhat borne in the job postings in the market as well. There seems to be a growth in the specialised role that is focused on continuous delivery. There is a corresponding growth in Jenkins jobs - doubling in the last 2 years!

![Job Role](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAmIAAAAJDkwZmFiMzdiLTVmMGQtNGZjZS04NjYxLWU3Y2UyMTIwZTk0YQ.png)

![Job Trend](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAl9AAAAJGQzZmIyYzNlLTU1M2YtNDgyMC04YzE4LWIxNGJjYjk1YTAwOQ.png)

To make sense of the data, I added data scientist job in there for fun 😃 and was more than presently surprised to see that there are 3x jobs in continuous delivery.
![Job trend 2](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAfWAAAAJGFkMGJlMWRjLWQ2ZDYtNGJlMC1hYzZmLTNlNDZhY2VjMjcxNQ.png)

## So what does this mean for you?
The Jenkins community has worked in the last two years to build the Jenkins Pipeline feature that brings native support for Pipelines. So if you are considering walking the continuous delivery path, ask your engineers to look at Jenkins Pipelines - most likely they are already using Jenkins and Pipelines is just a plugin away. Join the 79% of Jenkins users who are going to move to pipelines in the next 12 months.

![Pipeline plugin](https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAesAAAAJDM5OTMxNzFhLTAzNDQtNGQ1NC1hZTQzLTZmNDJmYWY2MWM3Yw.png)

I have given an overview in an [earlier blog](https://www.linkedin.com/pulse/jenkins-20-makes-easy-organisations-deliver-software-harpreet-singh?trk=prof-post) and more recently the Jenkins community did a [virtual conference](https://plus.google.com/events/cd3i7445t7819a1j2t0nboi1168) that goes into details here. These should be good starts.

# Summary
Unicorn companies have proven to the world that delivering software continuously is possible. Regular companies are now well on the path of delivering software continuously. A significant number of Jenkins users are now using it to deliver software continuously. Given, Jenkins’ large reach, it is not a stretch to say that it is the #1 tool in the market to do CD.

Opinions here are all mine and do not reflect that of my employers.

 Reference
* [Jenkins 2015 Survey](https://jenkins.io/files/2015-Jenkins-Community-Survey-Results.pdf)
* [Jenkins survey infographic](https://jenkins.io/files/State-of-Jenkins-Infographic-2015.pdf)
* [Jenkins 2.0 virtual conference](https://plus.google.com/events/cd3i7445t7819a1j2t0nboi1168)
* [Jenkins stats site](http://stats.jenkins-ci.org/jenkins-stats/svg/total-jenkins.svg)
