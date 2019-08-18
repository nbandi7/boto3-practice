# boto3-practice
AWS Lambda and boto3

# boto3-practice/ec2/
Steps to be followed to stop the **running EC2 instances** run the code in AWS Lambda
1. Start EC2 instances(atleast 2)
2. Create IAM Role and give EC2 and Cloudwatch full access
3. Create Lambda function 
	a. Choose Runtime environment 3.7
	b. Select the role that you created
	c. Use the stopEC2.py code for lambda function

Steps to be followed to start the **stopped EC2 instacnes** run the code in AWS Lambda
1. Check for the stopeed instances
2. Create IAM Role and give EC2 and Cloudwatch full access
3. Create Lambda function
	a. Choose Runtime environment 3.7
	b. Select the role that you created
	c. Use startEC2.py code for lambda function	

To automate the process Create **Cloudwatch Rule**
1. stopEC2Rule
	a. Event Source -> Scheduled
	b. Give cron expresison for the time you needed to stop EC2 in GMT Time
	c. Add Target stopEC2

2. startEC2Rule
	a. Event Source - Scheduled
	b. Give cron expression for the time you needed to start EC2 in GMT Time
	b. Add Target startEC2
