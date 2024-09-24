**AWS Account Opening with Root and User creation Guide**


*Opening an AWS Account*

Visit AWS Website
Go to https://aws.amazon.com and click on “Create an AWS Account.”

![1727174238187](image/creationofawsaccount/1727174238187.png)

![1727174291971](image/creationofawsaccount/1727174291971.png)

*Account Information*


Enter your email address, a password, and an account name. Make sure the email address is valid and accessible.
This is for **root user** account , the users will be created later

![1727174469804](image/creationofawsaccount/1727174469804.png)

*Contact Information*


Choose whether you are creating a Personal or Business account and fill in the necessary contact details. Enter a strong password for your root user, confirm it, and then choose

* **Continue** . AWS requires that your password
  meet the following conditions:

  * It must have a minimum of 8 characters and a maximum of 128
    characters.
  * It must include a minimum of three of the following mix of
    character types: uppercase, lowercase, numbers, and ! @ # $ % ^
    & * () <> [] {} | _+-= symbols.
  * It must not be identical to your AWS account name or email
    address.
* **Business** or  **Personal** account.
  Personal accounts and business accounts have the same features and
  functions.
* Enter your company or personal information.

![1727174827567](image/creationofawsaccount/1727174827567.png)

Fill in the below and agree to termas and conditions

![1727174979111](image/creationofawsaccount/1727174979111.png)

*Payment Information*

Enter your credit card or bank details. AWS will charge a small refundable fee to verify your payment method.

![1727175132370](image/creationofawsaccount/1727175132370.png)

*Identity Verification*


You may be prompted for phone verification. Provide a valid phone number, and AWS will send a code via SMS or a call.

![1727175317637](image/creationofawsaccount/1727175317637.png)

*Choose a Support Plan*


Select a support plan. You can choose the Free Basic Plan if you're just starting.

![1727175380035](image/creationofawsaccount/1727175380035.png)

*Sign In to AWS Console*


Once the account is set up, sign in to the AWS Management Console using the **root** email and password created earlier.


![1727175608208](image/creationofawsaccount/1727175608208.png)


![1727176078298](image/creationofawsaccount/1727176078298.png)


**Creating IAM User with Permissions to Launch EC2 and RDS**

*Go to IAM (Identity and Access Management)*


In the AWS Management Console, search for IAM in the services menu and select it.
![1727176127893](image/creationofawsaccount/1727176127893.png)

*Create a New User*


Go to Users on the left-hand sidebar.

![1727176187310](image/creationofawsaccount/1727176187310.png)

Click Create User.

![1727176264617](image/creationofawsaccount/1727176264617.png)

Enter a username (e.g., ec2-rds-user).

![1727176326123](image/creationofawsaccount/1727176326123.png)


On the next screen, choose Attach existing policies directly.
![1727176446998](image/creationofawsaccount/1727176446998.png)

Assign Permissions

Search for and select the following policies:
AmazonEC2FullAccess
![1727176566401](image/creationofawsaccount/1727176566401.png)

AmazonRDSFullAccess

![1727176603618](image/creationofawsaccount/1727176603618.png)

(Optionally) AdministratorAccess if you want full access for the user. (**Administrator access** in AWS refers to a level of permission granted to a user, group, or role that allows full, unrestricted access to all AWS services and resources, one level down from root access, cannot close the account)

![1727176715900](image/creationofawsaccount/1727176715900.png)

*Review and Create*

![1727176672385](image/creationofawsaccount/1727176672385.png)


*Review the user's details and click Create User.*



![1727177131201](image/creationofawsaccount/1727177131201.png)

Need to create Security credentials for the user to log on (console access recommended),


*Check “Programmatic Access” and “AWS Management Console Access” (optional based on access requirements, if only need to EC2 and RDS permissions then just give these permissions only).*

![1727177224636](image/creationofawsaccount/1727177224636.png)


![1727177293125](image/creationofawsaccount/1727177293125.png)

![1727177317854](image/creationofawsaccount/1727177317854.png)

![1727177348686](image/creationofawsaccount/1727177348686.png)


If needed CLI / Programmatic acccess then You do the following.

![1727177440303](image/creationofawsaccount/1727177440303.png)

![1727177478585](image/creationofawsaccount/1727177478585.png)


![1727177518958](image/creationofawsaccount/1727177518958.png)

![1727177602597](image/creationofawsaccount/1727177602597.png)





AWS Create Account:[ https://aws.amazon.com/resources/create-account/]()

AWS IAM Documentation:[ https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html]()

AWS EC2 Documentation:[ https://aws.amazon.com/ec2/]()
AWS RDS Documentation: [https://aws.amazon.com/rds/]()


***This document outlines the basic steps for opening an AWS account and setting up a user to manage EC2 and RDS resources. Feel free to modify the steps according to specific requirements for users, access permissions, or resources.***




###### Important

Because of the critical nature of the [root user](https://docs.aws.amazon.com/accounts/latest/reference/root-user.html) of the account, we strongly recommend that you
                                use an email address that can be accessed by a group, rather than
                                only an individual. That way, if the person who signed up for the
                                AWS account leaves the company, the AWS account can still be
                                used because the email address is still accessible.

If you lose access to the email address associated with the
                                AWS account, then you can't recover access to the account if you
                                ever lose the password.
