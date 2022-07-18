# Artitechure-for-website like Facebook,Twitter,Instagram

<p> I have design a architecture for social media application like Instagram Facebook twitter etc. which will increase the latency performance and availability of their application. Also It is cost efficient as It is pay for what you use.Frontend was in Wordpress so if anyone post any comments or message that message will first come to route 53 and then route 53 will route it to the load balancer after that load balancer  will balance the load of data coming from the frontend to different server and autoscaling will increase the server and decrease the server according to the need and from the server instance it will store in RDS  database also there are two bucket for backup one for storing the media backup and another one is used for storing the code backup.To increase the latency I have added the cloudfront which is connected to the media bucket so that data will be store in the cache and the data will be access fastly.</p>
<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/80382150/179578402-ce248819-7201-46a0-8f61-8a6ba15018f4.png">
</p>



![image](https://user-images.githubusercontent.com/80382150/179585134-f71c9927-692a-4a27-9657-3fa8255d86a3.png)

![image](https://user-images.githubusercontent.com/80382150/179586597-c7bd95f3-76c4-409b-9dc8-2ea36441f784.png)

![image](https://user-images.githubusercontent.com/80382150/179587213-b20d201f-1b9b-4e6d-8ee6-827b23da34dd.png)

<h3>Created two security group one for instance and one for rds in instance all traffic allowed in rds only TCP is allowed</h3>

![image](https://user-images.githubusercontent.com/80382150/179589158-5d9a7e06-ecaf-4576-abd7-e175dd8b2228.png)

![image](https://user-images.githubusercontent.com/80382150/179589747-0faf90a4-43c0-487b-a976-699af8dd0abb.png)

IAM role given full access to S3 bucket so that instance can store data inside the s3 bucket

![image](https://user-images.githubusercontent.com/80382150/179590285-7496701b-16f6-4b27-ab49-15802eceb8b2.png)

![image](https://user-images.githubusercontent.com/80382150/179598711-aabc6224-3ab6-4235-8900-b5e15aec46e4.png)

![image](https://user-images.githubusercontent.com/80382150/179599486-51018f2e-f9dc-47dc-9857-93eb9d4436ed.png)

![image](https://user-images.githubusercontent.com/80382150/179599633-d526b2e9-90c1-4d6c-81d8-6ce0cfb4d48c.png)

![image](https://user-images.githubusercontent.com/80382150/179599745-b8e73990-9c02-4d29-bbde-0c43c5dd9bca.png)

![image](https://user-images.githubusercontent.com/80382150/179599839-4c9556e6-148c-42f0-8cae-1878fb7ddb4b.png)

![image](https://user-images.githubusercontent.com/80382150/179599927-9578e413-511c-41c4-ae42-e20be2b57163.png)

![image](https://user-images.githubusercontent.com/80382150/179600016-237acebd-9c21-42f9-842b-d2425bc6b824.png)

