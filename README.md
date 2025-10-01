
---

# 🚀 Launching EC2, Configuring Git, and Connecting GitHub

## 1️⃣ Launch an EC2 Instance (Amazon Linux)

1. Log in to **AWS Console**.
2. Search for **EC2** service.
3. Launch a new instance with:

   * **AMI**: Amazon Linux 2023
   * **Instance type**: `t3.micro` (Free Tier eligible)
   * **Key pair**: Download `key.pem`
   * **Security Group**: Allow **SSH (22)** from `0.0.0.0/0`
4. Once launched, copy the **Public DNS** of the instance.

### SSH into EC2

```bash
ssh -i "key.pem" ec2-user@<your-public-dns>
```

---

## 2️⃣ Install and Configure Git

Update packages and install Git:

```bash
sudo yum update -y
sudo yum install git -y
git --version
```

Configure Git:

```bash
git config --global user.name "Atul Kamble"
git config --global user.email "atul_kamble@hotmail.com"
git config --list
```

---

## 3️⃣ Setup GitHub Repository

1. Sign up or log in to [GitHub](https://github.com).
2. Create a new repository (example: **DevOps**).
3. Add:

   * `README.md`
   * License (MIT recommended)

### Example README.md

```markdown
# My First Repo

This is my practice repository.

Steps:
1. Step One
2. Step Two
3. Step Three
```

Test commit locally:

```bash
echo "hello" >> README.md
```

---

## 4️⃣ Clone Repository to EC2

Clone the GitHub repo to your instance:

```bash
git clone https://github.com/Pratikshashinde16/DevOps.git
cd DevOps
```

---

## 5️⃣ Test with Python File

Create a simple Python file:

```bash
nano helloworld.py
```

Paste:

```python
# helloworld.py
print("Hello World from EC2 + GitHub!")
```

Save → Run it:

```bash
python3 helloworld.py
```

✅ Output:

```
Hello World from EC2 + GitHub!
```

---


