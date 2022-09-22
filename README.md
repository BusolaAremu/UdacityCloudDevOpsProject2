Link to Infrastructural Diagram
https://lucid.app/lucidchart/5eb006f6-568e-47f2-8fe9-0f66ec215f12/edit?viewport_loc=162%2C322%2C2220%2C974%2C0_0&invitationId=inv_361116a5-0843-4e13-9342-e8519fb951fb#

Website Link:
http://udagr-webap-b1umz2d20g3v-466917891.us-east-1.elb.amazonaws.com/ 

#### In this project, I did the following:
1. Created a launch configuration to deploy four servers, two located in private subnets, and two in public subnets, i.e. one each per subnets. This launch configuration is to be used by an auto-scaling group.
2. I provisioned two vCPU's, 4Gb of RAM and an Ubuntu 18 OS choosing  the appropriate instance size and machine image (AMI) that best fits
3. I created an IAM role with admin privileges that allows my instances use the s3 service.
4. I deployed a Load balancer loacted in the public subnet and opened the outbound port on HTTP Port: 80 so it can communicate with the private subnets. All inbound public traffic (0.0.0.0/0) was allowed on port 80
5. Deployed the application into the private subnets
6. Ensured that my cloudformation script exported the public URL of the load balancers