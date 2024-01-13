# Progressive Delivery

In this post, we will be looking at what progressive delivery is, why it is important and how to do it. we will also compare it with a traditional deployment strategy often referred to as Big Bang Deployment.

## Traditional Delivery

Traditional Deployment or often referred to as Big Bang Deployment is a deployment strategy where the entire application is deployed at once. This is the most common deployment strategy used in the industry today. It is also the most risky deployment strategy and prone to a lot of problems.

- **Risky**: It exposes end users to the new version of the software at the same time the dev team is experiencing same version in production. If there is a bug in the new version of the software, it will affect all end users at the same time.

- **Ineffective Testing**: In many cases, teams might have a pre-production environment where the new version of the software is tested before deploying it to production. This is often referred to as a `staging environment` but from experience, staging environments are often not a true representation of production environments. There are configuration differences, data differences, and other differences that make staging environments not a true representation of production environments.

- **Debug Difficultly**: In the case of a defect, because of the nature of the delivery strategy, it is often difficult to keep the defective version running though not exposed to end users while the defect is being fixed.

- **Difficult to Experiment**: It is difficult to experiment with new features or new versions. E.g If the development team is planning to evaluate the performance of a new version of the software of a framework, it is difficult to do so without exposing end users to the new version of the software.

![Traditional Delivery](traditional.svg)

In the scenario above, because of the nature of the deployment strategy, both customers and the development team are exposed to the new (and potentially defective) version of the software at the same time.

Progressive delivery can help immensely with these problems by de-risking deployments and making it easier to experiment with new versions of software and limiting the impact of defects on end users.

## What is Progressive Delivery?

Progressive Delivery is a delivery strategy that allow dev teams to release new versions of software safely, quickly and in a sustainable way. It builds on the foundations of Continuous Delivery, but focuses on the safety of deployments and the predictability of releases.

## Why Progressive Delivery?

The main purpose of progressively delivery is to **gradually build confidence** in a new version of the software before exposing it to end users. It is about making sure that we can release software without causing harm to our users or our business.

The release of a new version of the software is done in stages. Each stage will be designed to build confidence in the new version and as confidence grows, the newer version is exposed to end users equally.

![Progressive Delivery](progressive-stages.svg)

The stages above are just examples of stages that can be used in a progressive delivery strategy. The stages can be customized to suit the needs of the team. The stages can also be automated to make the process of releasing new versions of software easier.

If there is a defect in the new version of the software, the impact of the defect is limited to the users in the stage where the defect was discovered. This makes it easier to debug and fix the defect without affecting all end users.

## Benefits of Progressive Delivery

Here are some of the benefits of progressive delivery:

- **Safety**: Progressive Delivery is about reducing the risk of deployments. It is about making sure that we can release software without causing harm to our users or our business.

- **Sustainability**: Progressive Delivery is about making sure that we can release software in a way that is sustainable for our teams. It is about making sure that we can release software without burning out our teams.

- **Predictability**: Progressive Delivery is about making sure that we can release software in a way that is predictable for our users and our business. It is about making sure that we can release software without causing harm to our users or our business.

-- **Mitigation**: In the case of a defect or a bug, a progressive delivery strategy allows us to mitigate the impact of the defect on end users.

## How to Build Confidence?

In order to build confidence in a new version of the software, we need to have a way to measure the confidence in the new version of the software. This is where metrics come in. We need to have metrics that will help us measure the confidence in the new version of the software.
