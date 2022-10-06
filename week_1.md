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
5. After launching the ubuntuVM instance, I ticked the box to select the ubuntu instance, clicked on actions, next clicked on SSH Client tab and followed the steps ![image](https://user-images.githubusercontent.com/74470226/194226268-2fe63830-101f-4d33-90fe-d130fc03e903.png)
7. To connect from my local PC to my ubuntuVM on AWS, I followed these steps ![image](https://user-images.githubusercontent.com/74470226/194220883-c81a4916-0031-40e3-938b-6e4469ea7c22.png)
    * Firstly, I changed my directory to where my .pem file is stored ```cd Downloads```
    * To connect to ubuntuVM, I ran ```sh -i "ubuntuVM.pem" ubuntu@ec2-54-89-187-240.compute-1.amazonaws.com``` in the terminal
    * **ubuntu@ip-172-31-92-136:~$** indicates I've connected to ubuntuVm via SSH Client
9. Managed to connect to my instance via SSH client(Terminal) ![Connected to ubuntuVM instance via SSH Client](https://user-images.githubusercontent.com/74470226/194221550-a9a92088-71ae-434e-a203-a8ab83fd105b.png)
10. Checked my ubuntuVM Instance Status on AWS ![instance status](https://user-images.githubusercontent.com/74470226/194222474-9a67d28b-5b1e-4670-aa3f-2891255d6f0f.png)
11. How to add welcome message with ```cowsay```
    * Followed [Cool Custom Welcome Messages on Linux terminal](https://www.geeksforgeeks.org/cool-custom-welcome-messages-linux-terminal/) blog post to implement my welcome message
    * Started by installing fortune (prints out a random interesting proverb) and cowsay (displays a speaking cow in terminal window) by running ```sudo apt-get install fortune cowsay``` in the terminal
    * Next, opened the terminal to open the ./bashrc file using any editor of your choice. (Here, vim is used) ``` vim ~/.bashrc ```
    * Followed by adding a small line at the beginning of ~/.bashrc file, 
    * Saved the file and exit: Pressed “Esc” to exit this mode. Then typed “:w” to save my script. After that typed :wq to exit Vim
    * Finally typed ```exit``` to stop my instance then connected to my instance again by running the command in step 7 above
    * ![cowsay-welcome-message](https://user-images.githubusercontent.com/74470226/194425991-90f4c572-0865-4b6d-b36d-d53dd7675fbf.png)



# Notes on the challenges
