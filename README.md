# Connect-EC2-to-EBS-using-cli
1. Launch EC2 instance

aws ec2 run-instances --image-id your-ami-id --count 1 --instance-type your-instance-type --key-name your-key-pair --security-group-ids your-security-group-id --subnet-id your-subnet-id

2. Create an EBS Volume

aws ec2 create-volume --availability-zone your-availability-zone --size your-size-in-gb

3. Attach the EBS Volume to the EC2 Instance

aws ec2 attach-volume --volume-id your-volume-id --instance-id your-instance-id --device /dev/xvdf
