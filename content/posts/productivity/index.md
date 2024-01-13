---
title:  "7 Ideas for creating a highly productive development team"
date:   2023-09-20 17:52:34 +0100
---


## Consistent Development Environment

The development environment should be consistent across all developers. This is important because it reduces the time it takes to onboard new developers and it also makes it easier for developers to collaborate with each other and debug issues when they arise.

If possible, the development environment should be automated so that developers can easily spin up a new development environment when they need to.

![Devs](/assets/team-productivity/devs.svg)

This scenario above will be a nightmare to manage. The developers are running a different version of node in dev compared to the version of node running in production and even amongst themselves.

This is where a docker setup comes in handy to keep a consistent development environment across all developers and even in production

## Development vs Integration Environment

The differences between the development environment and the integration environment should be minimal. Nothing kills productivity like having to debug a test failure that only occurs on the Integration environment but not reproducible on the development environment.

Developers should be able to run the test suites exactly as they run on the integration environment with similar configurations if possible.

![Integration](/assets/team-productivity/integration.svg)

This scenario above will be a nightmare to manage is all too common and is usually difficult to rectify unless the development environment is as close to the integration environment as possible.

## Production Simulation

The development/integration environment should be as close to production as possible. This is important because when bugs are found in production, it will be easier to reproduce the bug in question, fix and test in the development environment if environments don't diverge much.

The further away the development environment is from production, the more difficult it will be to reproduce bugs found in production.

![Production](/assets/team-productivity/production.svg)

Each stage between development and production is a potential point of difference in configuration and blind spots that could be a source of bugs.

## Fast & Stable Testing

Flaky tests are the worst. They are a huge productivity killer. They make it difficult to trust the test suite and they make it difficult to trust the codebase. They kill productivity as the stop features from being shipped and they make it difficult to debug issues when they arise.

Slow tests are the cousins of flaky tests. When tests are slow, quick feedback grinds to a halt and productivity suffers.

## Fast & Consistent Builds

Slow build process eats into the time it takes to get features out and get feedback from end users. It also makes it easier to debug issues when they arise. Flaky builds grinds the entire dev process to a halt.

## Fast Deployments & Rollbacks

Deployments and rollbacks should be fast. Long pipelines are a productivity killer. How fast aa development can get features in front of end users is an essential metric for productivity. Equally important is the ability to rollback a deployment if something goes wrong.

## Solid Monitoring & Alerting

Monitoring and alerting is an essential part of the development process. It is important to know when things go wrong and when things are about to go wrong. It is also important to know when things are going well. Going into production without monitoring and alerting is a recipe for disaster, it is basically flying blind into a potential storm.

If these ideas are implemented, it will go a long way in building a highly productive development team. A team can ship software faster, with more confidence and with less stress.

These are some of the ideas that I have found to be useful in building a highly productive development team over the years as a member of a development team.

## Consistent Development Environment

The development environment should be consistent across all developers. This is important because it reduces the time it takes to onboard new developers and it also makes it easier for developers to collaborate with each other and debug issues when they arise.

If possible, the development environment should be automated so that developers can easily spin up a new development environment when they need to.

![Devs](/assets/team-productivity/devs.svg)

This scenario above will be a nightmare to manage. The developers are running a different version of node in dev compared to the version of node running in production and even amongst themselves.

This is where a docker setup comes in handy to keep a consistent development environment across all developers and even in production

## Development vs Integration Environment

The differences between the development environment and the integration environment should be minimal. Nothing kills productivity like having to debug a test failure that only occurs on the Integration environment but not reproducible on the development environment.

Developers should be able to run the test suites exactly as they run on the integration environment with similar configurations if possible.

![Integration](/assets/team-productivity/integration.svg)

This scenario above will be a nightmare to manage is all too common and is usually difficult to rectify unless the development environment is as close to the integration environment as possible.

## Production Simulation

The development/integration environment should be as close to production as possible. This is important because when bugs are found in production, it will be easier to reproduce the bug in question, fix and test in the development environment if environments don't diverge much.

The further away the development environment is from production, the more difficult it will be to reproduce bugs found in production.

![Production](/assets/team-productivity/production.svg)

Each stage between development and production is a potential point of difference in configuration and blind spots that could be a source of bugs.

## Fast & Stable Testing

Flaky tests are the worst. They are a huge productivity killer. They make it difficult to trust the test suite and they make it difficult to trust the codebase. They kill productivity as the stop features from being shipped and they make it difficult to debug issues when they arise.

Slow tests are the cousins of flaky tests. When tests are slow, quick feedback grinds to a halt and productivity suffers.

## Fast & Consistent Builds

Slow build process eats into the time it takes to get features out and get feedback from end users. It also makes it easier to debug issues when they arise. Flaky builds grinds the entire dev process to a halt.

## Fast Deployments & Rollbacks

Deployments and rollbacks should be fast. Long pipelines are a productivity killer. How fast aa development can get features in front of end users is an essential metric for productivity. Equally important is the ability to rollback a deployment if something goes wrong.

## Solid Monitoring & Alerting

Monitoring and alerting is an essential part of the development process. It is important to know when things go wrong and when things are about to go wrong. It is also important to know when things are going well. Going into production without monitoring and alerting is a recipe for disaster, it is basically flying blind into a potential storm.

If these ideas are implemented, it will go a long way in building a highly productive development team. A team can ship software faster, with more confidence and with less stress.
