Instructions on how to configure the EC2 with teardnwn instructions.

# AWS-Homework-1

PULL LUP AWS CLOUD
1. Sign into the AWS Consule
2. Select your region
3. Go the the Dashboard and seleact EC2

Create Security Group
1. Selecte security group on the left side
2. Click "Create Security Group"
3. Enter name and description (Usually they are the same)
4. Verify VPC is set to default
5. Add inbound HTTP TCP 80 ipv4 anywhere (0.0.0.0/0)
6. Add inbound SSH TCH 22 ipvd anywhere  (0.0.0.0/0)
7. DO NOT TOUCH OUTBOUND RULES - Verify it says "All traffic" is allowed
8. (Optional: Add tags)
9. CLICK  "CREATE SECURITY GROUP"

VERIFY YOUR SECURITY GROUP IS CREATED AND CORRETCLY CONFIGURED IN THE CONSULE

GRAB YOUR STARTUP SCRIP
1. Choose from the availalble start up scripts in the class (anyones will work)
2. Copy the script from Github

LAUNCHING EC2 INSTANCE
1. on the left column click on instance
2. Click "Launch Instance"

CREATING INSTANCE
1. Enter the instance name and add relevant tags if desired
2. AMI Selection: Review menu, esure defaults are selected, collapse
3. Instance Type: Review instance type menu, select proper sizing, collapse
4. Key Pair: select "Proceed without key pair" , Collapse  (IN MOST CASES YOU WILL NEED TO GENERATE A NEW KEY PAIR)

NETWORK SETTING
1. Dont click "Edit"
2. Verify VPC selection
3. Note: Subnet selection is not critical for this lab
4. Make sure " Autho-assign public IP" is enabled
5. Select your created Security Group (NOT "launch-wizard")
6. Collapse Section

STORAGE CONFIGURATION
1. Review storage menu
2. Collapse section

ADVANCED SETTINGS
1. Open advanced settings
2. Focus on User Data section only - ignore everything else
3. Paste your chosen startup script

LAUNCH
1. Review configuration
2. Click "Launch Instance"

TEST THE WEB SERVER
1. Wait for the instance to pass status checks
2. Copy the instances PUBLIC DNS ADDRESS
3. Open a browser
4. Use:  TYPE   http://  Then paste the Public DNS Address behind it


TEARDOWN
TERMINATE THE EC2 INSTANCE
1. Go to the EC2 Instance
2. Select your intance
3. Click the drop down and click TERMINATE INSTANCE

DELETE THE SECURITY GROUP (Optional)
1. Go to EC2 --- Security Groups
2. Select your security group you want to delete
3. Actions -- Delete Secutity Group
Note: The security group can only be deleted after the instance in terminated
