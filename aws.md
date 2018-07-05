Aws tasks:

create iam user:

go to iam section -&gt; there select the user -&gt; next select the Adduser -&gt;

here we create the passsword for the specific user and also we will create the policy.

Then download the csv file user related information available in that file.

Then go iam section select the link open the new window here paste that link login to the user.

![iam](https://github.com/malli2221/ops/blob/master/images/Screenshot%20from%202018-07-05%2011-20-57.png)

![iam1](https://github.com/malli2221/ops/blob/master/images/user%202018-07-05%2011-46-05.png)



Create inline         policies :

go to iam section there we need to select the exsting user and select the add permission

there we need to config the service, actions, resources, request conditions.

Click on the addpermission.

![permission](https://github.com/malli2221/ops/blob/master/images/inline1%202018-07-05%2012-19-48.png)

click on the import the management policy

![per](https://github.com/malli2221/ops/blob/master/images/inline2%202018-07-05%2012-20-14.png)

![police](https://github.com/malli2221/ops/blob/master/images/inline3%202018-07-05%2012-27-54.png)

attach the polici to user

![attach](https://github.com/malli2221/ops/blob/master/images/inline5%202018-07-05%2013-13-46.png)



Create Roles :  go to iam section there we need to  select the role, click on the create role here we have to create the role like (Ec2,Lamda,Rds) this role assign to ec2 instances.

Create roles:

![role](https://github.com/malli2221/ops/blob/master/images/role1%202018-07-05%2015-18-18.png)

![role1](https://github.com/malli2221/ops/blob/master/images/role3%202018-07-05%2015-19-04.png)

when ec2 instace launching time we need to select this, it communitcate to other aws server.

![role2](https://github.com/malli2221/ops/blob/master/images/role52018-07-05%2015-42-53.png)









Create Vpc:

 go to network&amp;context delivery here click on the vpc.

Vpc-&gt; create new vpc here we have to give the name and ipv4 details then click on the create vpc button.

![vpc](https://github.com/malli2221/ops/blob/master/images/vpc1%202018-07-05%2016-01-42.png)



Create subnets :

in this section i created three subnets for this vpc webserver,appserver,dbserver.

Go subnets -&gt; create subnets here we have to given name , vpc ,avalibilityzone and ipv4 details once give the details click on the create button.

![subnet](https://github.com/malli2221/ops/blob/master/images/vpc2%202018-07-05%2016-04-29.png)

Create internet gateway and attach to vpc:

go to internet gateway -&gt; create internet gateway here he given the name and create the igw this igw  attach to our vpc.

![igw](https://github.com/malli2221/ops/blob/master/images/vpc-igw2018-07-05%2016-12-09.png)

Create routing table and assign IGW and subnets:

go to routing table -&gt; create routing table here we given name tag and select our vpc in this section, then click create routing table.

To under edit section add the subnets to our routing table.

![routun](https://github.com/malli2221/ops/blob/master/images/vpc-routing%202018-07-05%2016-31-12.png)

Create a security group and allow tracffic:

go to security group-&gt; create security group

here give nametag , group name, description and vpc once given this click create.

![secu](https://github.com/malli2221/ops/blob/master/images/vpc-secuirty2018-07-05%2016-36-35.png)



Once done this things we will create one keypair public key. Using that key we will create the one ec2 instance on that we have select the our own vpc.
