# Week_1

## 2.) Individual assignment:
    - Create an ubuntu VM on one of the main cloud providers. 
        If you have no preference, go with AWS.
    - Able to access your VM remotely.
    - Create a 2nd user that can also access the VM with a separate credential.
    - *Slack message* Berkeli Halmyradov. You should be able to SSH or SFTP to the VM
    - Use **cowsay** to set a welcome back message for the users every time they log into the server.
    - Advance: Secure your VM access to from your laptop only.
    - Advance: Setup anything useful on the server that you can showcase to the class.
    
    ### Important notes:
    - When setting up your cloud account, make sure you configure the MFA security right away.
    - AWS - when launching resources, make sure you are have chosen the 'free-tier' ones.
    - Keep an eye on the billing monitor.


# Day 01

1. Started [AWS Launch a Linux Virtual Machine](https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/) tutorial
   - I have an AWS account setup with MFA
2. I was trying to understand **key pairs**. Did some digging and found AWS [Creating, displaying, and deleting Amazon EC2 key pairs](https://docs.aws.amazon.com/cli/latest/userguide/cli-services-ec2-keypairs.html#creating-a-key-pair) doc
3. After reading up on key pairs, I moved on to setting up of my Linux instance. First I read [Amazon EC2 key pairs and Linux instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)
4. I'm enjoying the process of reading documentation.[Use EC2 Instance Connect to provide secure SSH access to EC2 instances with private IP addresses](https://aws.amazon.com/blogs/security/use-ec2-instance-connect-to-provide-secure-ssh-access-to-ec2-instances-with-private-ip-addresses/) seems to be a good overview on what is required.

# Notes on the challenges
