# EC2 Setup

ssh-dev-env does not currently provide any automation for provisioning the EC2 instance. Here's what you'll need to do.

## 1. Launch an EC2 Instance

* consider a `dev` VPC
* choose a Linux variant
* [enable hibernation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html#enabling-hibernation)
* add a tag named `Owner` with a value equal to your [personal IAM user's name](iam-setup.md)
* attach a security group with the same tag

## 2. Create User on EC2 Instance

* Create a personal user on the system in the sudo (or admin) group.
* Add your SSH public key to the new user's `~/.ssh/authorized_keys` directory for quick access.
* Grant the new user passwordless permission to shutdown:

    **/etc/sudoers.d/01-shutdown**

    ```
    %sudo ALL=(ALL) NOPASSWD: /sbin/shutdown
    ```
