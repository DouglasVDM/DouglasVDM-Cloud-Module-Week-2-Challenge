# DouglasVDM-Cloud-Module-Week-2-Challenge

## Week 2: Basic Networking. 

### Given challenge week 0, add API and a data source. Make it secure. Introduce HTTP(S). Ports, authentication.

   * I hope you are doing well, this task will cut across networking, APIs, ports and 3-Tier App architecture.
   * Moreover, you’ll need your previous skills in Git, development and general architecture to finish.
   * We will also visit subnetting and HTTPS by next week. Happy hacking.
   
## Task:
1. Deploy static [flask app](https://github.com/DouglasVDM/Cloud-Module-Week-0-Challenge/blob/master/mySteps.md), [1st API](https://github.com/b4ssey/cyf-first-api) and [2nd API](https://github.com/b4ssey/cyf-second-api) on 3 different EC2 instances - AWS.
2. Make sure they are all connected and keep security groups to just HTTPS. 
3. It is recommended to start with API2 → API1 → FlaskApp.
4. Post URL’s to the 3 instances on the slack channel, in this format:
   | No. | Item | URL |
   | - | - | - |
   | 1 |App |{Your_ec2_IP_app} |
   | 2 |1st API |{Your_ec2_IP_API1}:5000/ |
   | 3 |2nd API |{Your_ec2_IP_API2}:5001/worstfood |
5. Wait for 2 other trainers to approve that they can see it before going to the next objective.
6. Create a new Virtual Private Cloud (VPC) or make use of an existing one. 
7. Make sure your app is consuming properly. 
8. Optional, It should have a CIDR that supports using at least 60,000 hosts.
9. Post the URLs in the format shown in 3 and see if your 2 API’s can be accessed. 
10. If you get 2 approval that they can’t access them, proceed to the next objective.

# Notes on the challenges
    * Internal API is more secure, a bit more complex though (...@Harry Li recommends it, if you can implement it)
    * There's a lot of examples out there for Free Tier applications, read that up 1st to understand the concept
    * Do an architectural diagram, it's recommended. Look-up "How to do a diagram" AWS has their own logo's. It's a professional way to present an infrastructure

# Todo: 
  1. Access Flask App
  2. Architectural Diagram
  3. Phase 2
  4. I need to look into how to [Set up dynamic DNS on Your Amazon Linux instance] (https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dynamic-dns.html)
  5. 
    
# Day 01

1. Started reading blog posts, I found [How to Deploy and Automate Projects with AWS Free Tier — Part 1](https://aws.plainenglish.io/part-1-design-how-to-deploy-and-automate-your-projects-with-aws-free-tier-79eeab5fff62) to be an interesting read. Didn't understand the majority of the contents but put it in my head anyway. I was hooked when I saw there's a **Sample Project**!
2. Next article on my list is [How You Can Use AWS Free Tier — Cloud Compute](https://www.msp360.com/resources/blog/aws-free-tier-ec2-lambda/). It also contains **example projects**, which is what I'm looking for.
3. Some of the more popular use cases for the cloud

|Use case|Descripttion|
|----|----|
|Saas (Software as a Service)| Delivering a single application through a web browser to thousands of customers using a multitenant architecture.
|Utility Computing| This form of cloud computing is getting new life from Amazon, Sun, IBM, and others who now offer storage and virtual servers that IT can access on demand.|
|Web Services in the Cloud| Closely related to SaaS, Web service providers offer APIs that enable developers to exploit functionality over the Internet, rather than delivering full-blown applications|
|Platform-as-a-Service| This form of cloud computing delivers development environments as a service. You build your own applications that run on the provider’s infrastructure and are delivered to your users via the Internet from the provider’s servers.|
|MSP (Managed Service Providers)| One of the oldest forms of cloud computing, a managed service is basically an application exposed to IT rather than to end-users, such as a virus scanning service for e-mail or an application monitoring service.|
|Service Commerce Platforms| A hybrid of SaaS and MSP, this cloud computing service offers a service hub that users interact with. They’re most common in trading environments.|

4. 

# Day 02
1. 

# Day 03
1. 

# Day 04
1. 

# Day 05
1. 

# Day 08
  1. Working on an ip address that doesn't change when I start up my instance. [Elastic IP addresses
](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)
  2. I'm constantly thinking about not incurring costs on AWS [Tracking your AWS Free Tier usage](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/tracking-free-tier-usage.html), I discovered that [Elastic IP](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html#eip-pricing) is not part of the Free Tier 
  
  #### Is Elastic IP free in free tier?
    * An Elastic IP address doesn't incur charges as long as all the following conditions are true: 
      * The Elastic IP address is associated with an EC2  instance. 
      * The instance associated with the Elastic IP address is running. 
      * The instance has only one Elastic IP address attached to it.07 Dec 2021.
      
# Day 09
  1. I found this blog post to [Deploying a Node.js App on an AWS EC2 Instance
](https://medium.com/@justinpaoletta_dev/deploying-a-node-js-app-on-an-aws-ec2-instance-ee75f1f6630).
  2. The deployment went well, one issue is that I can't view both Node apps in the browser. 
  3. Both [first-api](http://ec2-54-197-43-140.compute-1.amazonaws.com:5000/) and [second-api](http://ec2-54-91-101-162.compute-1.amazonaws.com:5001/worstfood) timed out
  4. Managed to set inbound rules on Security Group for both instances to accept **SSH** on **PORT: 22** and **HTTPS** on **PORT: 443** ![image](https://user-images.githubusercontent.com/74470226/196754752-839bd615-b161-451a-86b8-556e95a7dd5c.png). I'm hoping this inbound rule change will fix the timeout issue
  5. I stopped both instance so that I can move on to **Flask App instance**
  6. I stepped through [Creating a Virtual Environment on an AWS EC2 Ubuntu 20.04 Instance](https://python.plainenglish.io/creating-a-virtual-environment-on-an-aws-ec2-ubuntu-20-04-instance-2f47dce1c2a3) to create a Virtual Environment

# Day 10
  1. I managed to access my node servers by adding a **Custom TCP Inbound Rule** to my **Security Group** to accept web traffic on **PORT: 5001** and **PORT: 5000** respectively.
  2. For connecting API instances to Flask App instance, I'm going to test [How to connect an EC2 linux instance to another Linux instance](https://www.edureka.co/community/51996/how-to-connect-an-ec2-linux-instance-another-linux-instance) blog post. I've read it 2x and it sounds like it may be the solution for my current Todolist item.

# Day 11
  1. On the list for today is the Architectural Diagram and the new Flask app. Before attempting the Architectural diagram, I decided to watch my first **YouTube** video [AWS VPC Beginner to Pro - Virtual Private Cloud Tutorial](https://www.youtube.com/watch?v=g2JOHLHh4rI). Up to this point, I've only been reading **blog posts** and **documentation**. A ***task*** that I've been avioding for the longest time!
  2. # Amazon VPC Components
     | VPC Component | What it's used for |
     | --- | --- |
     | Virtual Private Cloud (VPC) | A logically isolated virtual network in the AWS cloud |
     | Subnet | A segment of a VPC's IP address range where you can place groups of isolated resources |
     | Internet Gateway Egress-Only (outbound) | The Amazon VPC side of a connection to the public Internet using the IPv6 protocol |
     | Internet Gateway Egress & Ingress (inbound & outbound) | The Amazon VPC side of a connection to the public Internet using the IPv4 protocol |
     | Router | Routers interconnect subnets and direct reaffic between internet gatewats, vitual private gateways, NAT gateways, and subnets |
     | Peering Connection | Direct connection between two VPC's |
     | VPC Endpoints | Private connection to public AWS services |
     | NAT Instance | Enables Internet access for EC2 instances in private subnets managed by you |
     | NAT Gateway | Enables Internet access for EC2 instances in private subnets managed by AWS |
     | Virtual Private Gateway | The Amazon VPC side of a Virtual Private Network (VPN) connection |
     | Cudtomer Gateway | Customer side of VPN connection |
     | AES Direct Connect | High speed, high bandwidth, private network connection from customer to aws |
     | Security Group | Instance-level firewall |
     | Network ACL | Subnet-level firewall |

# Day 12

  1. Architectural diagram v0 ![image](https://user-images.githubusercontent.com/74470226/197410848-4bab6d38-23c9-4aee-881d-eb30d5095f14.png)
  2. The start of setting up VPC, Subnets, Internet Gateway, Security Group, etc.
  
### Click create VPC
* Add a name tag for ease of reference
* Select: IPv4 CIDR manual input
* IPv4 CIDR: `10.0.0.0/16`
* The rest of the settings will remain as per defaults
* Select: No IPv6 CIDR block
* Tenancy Info: Default
* Click `Create VPC` button

### Create a Public Subnet
* Click `Subnets` in the left menu -> click `Create Subnet` button
* Select the `VPC` created in the previous step
* Choose availability Zone `us-east-1a`
* IPv4 CIDR block Info `10.0.1.0/24`
* Click `Create Subnet`

### Create a Private Subnet
* Click `Subnets` in the left menu -> click `Create Subnet` button
* Select the `VPC` created in the previous step
* Choose availability Zone `us-east-1b`
* IPv4 CIDR block Info `10.0.2.0/24`
* Click `Create Subnet`

### Create a new EC2 Instance on custom VPC
* Select `existing` key pair or `create` new key pair
* On new EC2 settings -> `Network settings` Click `Edit` button -> change `VPC` to the custom VPC created in previous step
* Set `Public IP Address` to `Enable` 
* Add name tag for security group `public-security group-01`
* Add rule `HTTPS` from anywhere `0.0.0.0/0`
* Add rule for SSH

### Create Internet Gateway
* Click `Internet gateways` in the left menu -> click `Create internet gateway` button
* Add name tag `my-app-internet-gateway`
* Click `Create Internet Gateway`
* Once created, Click the `Actions` button, select `Attach to VPC`
* Select `Custom VPC`
* Click `Attach Internet Gateway`

### Create Route Table (Manages where internet traffic goes)
* Click `Route tables` in the left menu -> click `Create route table` button
* Add name tag `my-app-public-route-table`
* Click `Create route table`
* Once created, Click the `Edit routes` button
* `Add route` set `Destination` to accept any other address `0.0.0.0/0` that the instance is trying to connect to can be forwarded to the `Internet Gateway` created in the previous step 
* `Save Changes`
* Go to `Subnets` to `Public Subnet` -> `Route Table` -> `Edit Route Table Association` -> select `my-app-public-route-table`
* `Save`
* 
* Confirmed the instance is working, I can SSH on my local machine.
```bash
Welcome to Ubuntu 22.04.1 LTS (GNU/Linux 5.15.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Oct 23 20:51:16 UTC 2022

  System load:  0.35546875        Processes:             102
  Usage of /:   19.5% of 7.57GB   Users logged in:       0
  Memory usage: 20%               IPv4 address for eth0: 10.0.1.186
  Swap usage:   0%

0 updates can be applied immediately.


The list of available updates is more than a week old.
To check for new updates run: sudo apt update


The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

ubuntu@ip-10-0-*-***:~$
```
# Day 13

1. Hopefully, How To Serve Flask Applications with Gunicorn and Nginx on Ubuntu 22.04(https://www.digitalocean.com/community/tutorials/how-to-serve-flask-applications-with-gunicorn-and-nginx-on-ubuntu-22-04), will help me, serve the Flask App and sort out the access via the internet.
2. Found another blog post [Deploy flask app with nginx using gunicorn and supervisor](https://medium.com/ymedialabs-innovation/deploy-flask-app-with-nginx-using-gunicorn-and-supervisor-d7a93aa07c18). This seems to be more aligned to the setup I need
3. [Deploy Flask The Easy Way With Gunicorn and Nginx!](https://dev.to/brandonwallace/deploy-flask-the-easy-way-with-gunicorn-and-nginx-jgc)

# Day 14

1. Previous blog posts didn't get me very far. On to the next blog post [How to deploy your Flask App on AWS EC2 instance with Nginx, Gunicorn
](https://berkoc.medium.com/how-to-deploy-your-flask-app-to-aws-ec2-instance-with-nginx-gunicorn-b734df606a14). Spent a fair amount of time reading the current post, a few times over. Ready for implementation later. Mainly keeping an eye on AWS Free Tier usage, which is at 89%
2. Finally a blog post that includes screen shots to verify that I'm not missing any steps. [Step-by-step visual guide on deploying a Flask application on AWS EC2](https://medium.com/techfront/step-by-step-visual-guide-on-deploying-a-flask-application-on-aws-ec2-8e3e8b82c4f7) Especially, the `.service` file step below needs to executed after running `deactivate` on the `venv`. This is an important oversite on most blog posts. I managed to catch it on the `terminal recording` included in the post.
3. A `volunteer` spent time with me in a `live session` to debug` why my Flask App` is not accessible on the `internet`. It all came down to `<projectname>.service` file in the `/etc/systemd/system` directory

# Day 15
1. I had all 3 instances running today, with the following error, see entry below
2.     curl localhost:8000
       <!doctype html>
       <html lang=en>
       <title>500 Internal Server Error</title>
       <h1>Internal Server Error</h1>
       <p>The server encountered an internal error and was unable to complete your request. Either the server is overloaded or there is an error in the application.</p>
3. The image below helped me to visualise Client, Nginx, Gunicorn, Flask App flow
4. ![image](https://user-images.githubusercontent.com/74470226/198844702-65a179b4-ac97-4778-bddf-5efedb205e4b.png)

# Day 16
1. Thank you to one of the volunteers for pointing me in the right direction. I was trying to solve the "y-problem" when the "x-problem" was not running on my local yet!:bang-head: 
2. ON LOCAL: Solved the issue. For me it was changing the ports in the api's. I had an error that port 5000 was already in use (ie. the flask app). I then set api 1 to 5001, api 2 to 5002. Started both apis up before staring the flask app
Going to tackle EC2 instances today (edited![image](https://user-images.githubusercontent.com/74470226/199653762-a90920e8-6f25-4d8e-9ae7-7c08216fbbad.png)

# Day 17
  
1.EC2 instance day! I started by checking / setting the `Inbound Rules` on the `APISecurityGroup`. ![image](https://user-images.githubusercontent.com/74470226/199654933-f275cd87-b7fc-4683-87d6-abe1de3fc18f.png)

2. The `First API` consumes the `Second API`. 
        To achieve this: 
        * In the `First API`, I changed the `URL` variable to point to `const URL = "http://Second API - Private IPv4 address:PORT"`. Because comms will now take place inside the `VPC` not the over the internet.
        * ![image](https://user-images.githubusercontent.com/74470226/199655733-97a2a3b3-9bd7-4590-b50f-9351d53aebfd.png)
        * ![image](https://user-images.githubusercontent.com/74470226/199655902-4befd83d-8d80-467c-8a40-ebd7c932edd1.png)
        * ![image](https://user-images.githubusercontent.com/74470226/199655975-1ab493c3-4d23-462a-9cc1-86ddec2df515.png)
  3. It seems as 1st and 2nd API is communicating
  4. Next step is for `Flask App` to consume both APIs
 
# Day 18


  

