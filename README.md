# boto3-practice
AWS Lambda and boto3

# boto3-practice/ec2/
Steps to be followed to run the code in AWS Lambda
1. Start EC2 instances(atleast 2)
2. Create IAM Role and give EC2 and Cloudwatch full access
3. Create Lambda function 
	a. Choose Runtime environment 3.7
	b. Select the role that you created
	c. Use the stopEC2.py code for lambda function
