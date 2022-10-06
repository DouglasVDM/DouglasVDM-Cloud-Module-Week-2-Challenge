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

# Day 02
1. Went through [How to connect to AWS ec2 instance from Ubuntu terminal](https://www.how2shout.com/linux/how-to-connect-to-aws-ec2-instance-from-ubuntu/) blog to connect.
2. ssh: connect to host 52.31.72.40 port 22: Connection timed out
3. Will revisit connecting to my instance later today by going through [I'm receiving "Connection refused" or "Connection timed out" errors when trying to connect to my EC2 instance with SSH. How do I resolve this?
](https://aws.amazon.com/premiumsupport/knowledge-center/ec2-linux-resolve-ssh-connection-errors/)

# Day 03
1. Signed in to AWS with IAM user account.
2. A while ago, I setup my AWS account with MFA (multi-factor authentication), when I started studying for AWS Cloud Practitioner Exam (few months ago).
3. 1st Spent some reading the [Best Practices](https://docs.aws.amazon.com/accounts/latest/reference/best-practices.html)
4. Then stepped through Launching an Instance
5. Managed to connect to my instance via SSH client(Terminal) ![Connected to ubuntuVM instance via SSH Client](https://user-images.githubusercontent.com/74470226/194221550-a9a92088-71ae-434e-a203-a8ab83fd105b.png) 
6. To connect from my local PC to my ubuntuVM on AWS, I followed these steps ![image](https://user-images.githubusercontent.com/74470226/194220883-c81a4916-0031-40e3-938b-6e4469ea7c22.png)
7. ubuntuVM Instance Status ![instance status](https://user-images.githubusercontent.com/74470226/194222474-9a67d28b-5b1e-4670-aa3f-2891255d6f0f.png)


# Notes on the challenges
