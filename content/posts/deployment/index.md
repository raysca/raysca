---
title: Continuos Deployment Patterns
date: 2021-10-10T11:30:03+00:00
---

In this post, I will discuss different deployment patterns that you can use to deploy your application. I will also discuss how you can implement these deployment patterns in Kubernetes.

## Recreate

With this deployment pattern, you deploy a new version of your application and delete the existing version of the application. This is the simplest deployment pattern, but it can result in downtime for your application as shown in the following diagram.

![Recreate](/assets/deployment/recreate.png)

## Ramped

With this deployment pattern, you deploy a new version of your application alongside the existing version of the application. Once the new version is ready, you gradually shift traffic from the existing version to the new version. This is the default deployment strategy in Kubernetes.

![RollingUpdate](/assets/deployment/ramped.png)

## Canary

With this deployment pattern, you deploy a new version of your application alongside the existing version of the application. Once the new version is ready, you shift a small percentage of traffic from the existing version to the new version. If the new version performs well, you continue shifting traffic until all traffic is shifted to the new version. If the new version performs poorly, you stop shifting traffic and continue to use the existing version.

![Canary](/assets/deployment/canary.png)

## Blue/Green

With this deployment pattern, you deploy a new version of your application alongside the existing version of the application. Once the new version is ready, you switch traffic from the existing version to the new version.

![Blue/Green](/assets/deployment/blue-green.png)

## A/B Testing

With this deployment pattern, you can test a new version of your application by deploying it to a subset of users alongside the existing version of the application.

![A/B Testing](/assets/deployment/ab-test.png)

## Shadow

With this deployment pattern, you can test a new version of your application by deploying it alongside the existing version of the application. However, instead of sending client traffic to the new version, you send a copy of the traffic to the new version. This allows you to test the new version without impacting the existing version.

![Shadow](/assets/deployment/shadow.png)


Hopefully, this post has given you a better understanding of different deployment patterns that you can use to deploy your application.
