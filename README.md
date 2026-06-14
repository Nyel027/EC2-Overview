### **CREATING AND CONNECTING TO AN EC2 INSTANCE**
##

The Amazon EC2 (Elastic Cloud Compute) is a service on AWS that allows you create, access and use virtual computer in the cloud.


An EC2 instance is the actual virtual server you create using the EC2 service. An EC2 instance basically comprises the following; 

1. CPU (processing power)
2. RAM (memory)
3. Disk (storage space)
4. Operating System (Windows, Linux, etc)


\
And just like a regular computer, you can start (launch) an instance, stop, terminate and reboot too. 

EC2 instances fall under various suggestive categories such as; 
* general instances
* compute optimized
* storage optimized
* memory optimized
* accelerated compute instance


\
![INSTANCE TYPES IMAGE](images/img1.png) 

\
You can simply identify instance type or categories is based off their names.

Instance names are a combination of the instance family, generation and size. A good example is the t3.micro. They can also indicate additional capabilities and features such as specific processor type or optimised networking performance.

##
**LAUNCHING AND CONNECTING AN EC2 INSTANCE**

*(A hands-on guide to launching an EC2 instance from the AWS console)*

##

Having defined and explained what an EC2 instance is, we shall now proceed to launching on directly from the AWS console and them go a step further by connecting it via SSH on Linux. 

It’s a pretty straightforward process and quite easy to understand as well. Also, since this is a test launch, we’d be going with the basic selections for everything (general purpose instance, default settings, etc).

\
**LAUNCHING THE INSTANCE**
1. Login to the AWS console and from the dashboard, select ‘EC2'
2. Now in the EC2 tab, you want to select ‘Launch Instance’ 
3. Fill in your Instance name and leave the the options as default as highlighted in the image below.

![INSTANCE OVERVIEW](images/img2.png) 

4. Select Instance type (t3.micro)


5. Create a new key pair with the .pem format.
6. Now, we have to select and edit our network and security group but for the purpose of this exercise, they shall all be left as default as highlighted in the image below but for actual work, it is important to carefully create a security group solely for that specific instance. 

![NETWORK OPTIONS](images/img3.png)

7. Perform a quick overlook to make sure everything is as they should be and then go ahead to launch the instance. 

\
After successfully launching the instance, we can now access it by selecting **‘View All Instances’** at the bottom of the page and we should see our newly created instance there. We need to wait for a couple of minutes for the health checks to be passed successfully for it is only after this point we can confidently say an EC2 instance has been launched. 


##

**CONNECTING TO THE INSTANCE**

After launching and verifying the instance is healthy and running, we can now proceed to connecting via SSH client. 

1. Select the instance by clicking the empty box beside the instance name and then choose ‘connect’.

![CONNECT OPTION](images/img4.png)

2. After selecting ‘connect’, some options would appear upon which you are to select SSH Client and then follow the instructions to connect your instance.

\
Upon following the instructions accordingly, to confirm success of the actions, you should see something resembling the image below in your terminal. 

![INSTANCE CONNECTED SUCCESSFULLY](images/img5.png)


\
***NB; The commands should be done via your terminal and under your Downloads folder where you have you key pair saved.***


\
And that's pretty much it. We have successfully launched an instance and connected it.