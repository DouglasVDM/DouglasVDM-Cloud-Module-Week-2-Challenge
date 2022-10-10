# DouglasVDM-Cloud-Module-Week-2-Challenge

## Week 2: Basic Networking. 

### Given challenge week 0, add API and a data source. Make it secure. Introduce HTTP(S). Ports, authentication.

   * I hope you are doing well, this task will cut across networking, APIs, ports and 3-Tier App architecture.
   * Moreover, you’ll need your previous skills in Git, development and general architecture to finish.
   * We will also visit subnetting and HTTPS by next week. Happy hacking.
   
## Task:
1. Deploy static flask app, 1st API and 2nd API on 3 different EC2 instances - AWS.
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

    

