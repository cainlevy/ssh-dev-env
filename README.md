# SSH Development Environment

Move your development environment into the cloud with a pausable EC2 server.

## Problem

You want portability and power, but a laptop is a poor trade. The development environment you're supposed to run locally can barely coexist alongside Chrome and Slack, and when you try to screen share or boot Sketch everything crunches to a halt.

## Solution

Move your development environment into a rentable EC2 instance, and manage costs by only running it when you need it.

The instance hibernates any time your computer idles. Resuming takes seconds.

## Setup

* Install [AWS CLI](https://aws.amazon.com/cli/) where ssh-dev-env can find it.
* Create a personal IAM user with necessary permissions ([guide](docs/iam-setup.md))
* Configure AWS CLI with a [profile for personal IAM user](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html#cli-quick-configuration-multi-profiles)
* Provision an EC2 instance ([guide](docs/ec2-setup.md))
