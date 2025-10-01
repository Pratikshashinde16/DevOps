#🚀 Launching EC2, Configuring Git, and Connecting GitHub
#1️⃣ Launching an EC2 Instance (Amazon Linux)
Login to AWS Console.

Search for EC2 service.

Launch a new instance with:

AMI: Amazon Linux 2023
Instance type: t3.micro (Free Tier eligible)
Key pair: Download key.pem
Security Group: Allow SSH (22) from 0.0.0.0/0
Once launched, copy the Public DNS of the instance.

SSH into EC2
ssh -i "key.pem" ec2-user@ec2-3-80-195-140.compute-1.amazonaws.com
#2️⃣ Install and Configure Git
Update packages and install Git:

sudo yum update -y
sudo yum install git -y
git --version
Configure Git:

git config --global user.name "Atul Kamble"
git config --global user.email "atul_kamble@hotmail.com"
git config --list
3️⃣ Setup GitHub Account
Sign up or log in to GitHub.

Create a new repository (example: DevOps).

Add:

README.md
License (MIT recommended)
Edit README.md
Example:

# My First Repo

This is my practice repository.
echo "hello"


1. Step One
2. Step Two
3. Step Three
4️⃣ Clone Repository to EC2
Clone the repo:

git clone https://github.com/Pratikshashinde16/DevOps.git
cd DevOps
5️⃣ Test with Python File
Create a simple Python file:

# helloworld.py
print("Hello World from EC2 + GitHub!")
Run it:

python3 helloworld.py
✅ You have successfully launched an EC2, installed Git, configured GitHub, cloned your repo, and tested Python code.
