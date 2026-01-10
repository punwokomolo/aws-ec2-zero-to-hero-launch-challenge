ZERO-TO-HERO EC2 BASICS LAUNCH CHALLENGE

**Theme:** *Launch, Configure, Secure, Connect & Monitor your first EC2 instance*

📋 Table of Contents

- [About This Challenge](#about-this-challenge)
- [What You'll Learn](#what-youll-learn)
- [Prerequisites](#prerequisites)
- [Challenge Levels](#challenge-levels)
- [Getting Started](#getting-started)
- [Support & Resources](#support--resources)


🎯 About This Challenge

Welcome to the **Zero-to-Hero EC2 Challenge**! This hands-on learning experience will take you from AWS beginner to confidently launching and managing your own cloud servers. Through 8 progressive levels, you'll build real-world skills that cloud engineers use every day.

By the end of this challenge, you'll have deployed a live web server on AWS EC2, configured storage, managed security, and learned cost optimization strategies.


What You'll Learn

- ✅ **What EC2 is** and why companies use it
- ✅ **How to launch** an EC2 instance from scratch
- ✅ **Choose AMIs & instance types** for different use cases
- ✅ **Create and use key pairs** for secure authentication
- ✅ **Configure security groups** as cloud firewalls
- ✅ **SSH into a Linux server** and run commands
- ✅ **Install software** (Apache web server) on EC2
- ✅ **Create & attach EBS volumes** for storage
- ✅ **Manage instance lifecycle** (stop, start, reboot, terminate)
- ✅ **Optimize costs** and avoid unexpected bills
- ✅ **Monitor resources** using CloudWatch basics


## 🔧 Prerequisites

- **AWS Account** (Free tier eligible)
- **Basic terminal knowledge** (helpful but not required)
- **Computer** with internet access
- **Software**: if using thw Windows OS, download [Git Bash](https://git-scm.com/install/windows)
- **Enthusiasm** to learn cloud computing!

**Cost Estimate:** $0 if using AWS Free Tier correctly (t2.micro instance)


🏆 Challenge Levels

### **LEVEL 0: AWS Warm-Up** 🟤
*Beginner Orientation*

**Objective:** Understand the basic idea of EC2

Learn that EC2 is essentially a virtual computer in the cloud that behaves just like a physical laptop.

**Tasks:**
- Identify 5 real companies that use EC2
- List 3 scenarios where you might use EC2
- Define key terms: EC2, AMI, Instance Type, Key Pair, Security Group

**Badge Earned:** 🟤 Cloud Explorer



### **LEVEL 1: Launch Your First EC2 Instance** 🟡
*Create your virtual computer*

**Objective:** Successfully launch an EC2 instance

**Configuration:**
- **Name:** ZeroToHero-EC2
- **AMI:** Amazon Linux 2023 (Free tier)
- **Instance Type:** t2.micro
- **Key Pair:** Create new → `zth-keypair`
- **Security Group:** Allow SSH from your IP

**Deliverables:**
- Screenshot of running instance
- Instance ID recorded
- Public IPv4 address noted

**Badge Earned:** 🟡 Instance Launcher



### **LEVEL 2: Connect to the EC2 Instance** 🟨
*Access your server like a real cloud engineer*

**Objective:** SSH into your EC2 instance

**Tasks:**

**Linux/Mac:**
```bash
ssh -i zth-keypair.pem ec2-user@<Public-IP>
```

**Windows:** Use PowerShell or PuTTY

**Commands to run:**
```bash
uname -a      # Shows OS and kernel
whoami        # Confirms your user
ls -la        # Shows your current directory
```

**Badge Earned:** 🟨 Terminal Explorer


**LEVEL 3: Install Software on Your EC2** 🟪
*Use it like your own server*

**Objective:** Deploy a web server

**Tasks:**

1. **Install Apache web server:**
```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

2. **Create a webpage:**
```bash
echo "Welcome to my Zero-to-Hero EC2 Challenge!" | sudo tee /var/www/html/index.html
```

3. **Test in browser:**
```
http://<Public-IP>
```

**⚠️ Important Teaching Moment:**

If the page doesn't load, you've discovered **THE MOST IMPORTANT EC2 LESSON:**

**Security Groups = Cloud Firewalls**

"The server is running, but AWS is protecting it."

**Fix:**
- Go to EC2 → Security Groups
- Edit inbound rules
- Add: Type: HTTP, Port: 80, Source: 0.0.0.0/0

**Key Insight:** *"Cloud isn't insecure. It's secure by default."*

**Badge Earned:** 🟪 Cloud Developer


### **LEVEL 4: EBS Volume Challenge** 🟫
*Work with cloud storage*

**Objective:** Attach and mount external storage

**Tasks:**

1. **Create EBS volume:**
   - Size: 2 GB
   - Same Availability Zone as EC2

2. **Attach to instance**

3. **Format and mount:**
```bash
sudo mkfs -t xfs /dev/xvdf
sudo mkdir /mydata
sudo mount /dev/xvdf /mydata
```

4. **Verify:**
```bash
df -h
```

**Concept:** "EBS volumes are detachable hard drives. Storage is modular in the cloud."

**Badge Earned:** 🟫 Storage Handler


### **LEVEL 5: Security Group Upgrade** 🔵
*Understand cloud firewalls*

**Objective:** Master security group rules

**Tasks:**
- Confirm HTTP rule (port 80) is enabled
- Remove the rule → refresh browser → observe what happens
- Re-enable the rule
- Write a 2-line explanation of security groups

**Badge Earned:** 🔵 Security Defender


### **LEVEL 6: Lifecycle Control** 🟩
*Manage server states*

**Objective:** Control instance lifecycle

**Tasks:**

From the AWS Console:
1. **Stop** the instance
2. **Start** it again
3. **Reboot** it
4. **Terminate** it (when ready to end the challenge)

**Questions to answer:**
- What happens to the IP address when you stop/start?
- Does EBS data remain after stop/start?

**Badge Earned:** 🟩 Lifecycle Commander


### **LEVEL 7: Cost Optimization Mini-Challenge** 🟧
*Know how to save money*

**Objective:** Understand AWS billing

**Questions:**
1. Why is "t2.micro" free tier eligible?
2. What's the difference between "Stop" vs. "Terminate"?
3. When does EC2 cost money?
4. List 3 ways to avoid extra billing

**Badge Earned:** 🟧 Cloud Economist

Getting Started

1. **Sign up** for an AWS Free Tier account at [aws.amazon.com](https://aws.amazon.com)
2. **Clone or download** this repository
3. **Start with LEVEL 0** and progress sequentially
4. **Take screenshots** and document your progress
5. **Ask questions** when stuck (that's part of learning!)

📚 Support & Resources

### Official AWS Documentation
- [EC2 User Guide](https://docs.aws.amazon.com/ec2/)
- [AWS Free Tier](https://aws.amazon.com/free/)

### Key Concepts Explained

**EC2 (Elastic Compute Cloud):** Virtual servers you rent from AWS

**AMI (Amazon Machine Image):** The operating system template for your instance

**Instance Type:** The hardware specifications (CPU, RAM, etc.)

**Key Pair:** SSH credentials for secure server access

**Security Group:** Virtual firewall controlling inbound/outbound traffic

**EBS (Elastic Block Store):** Persistent storage volumes for EC2

Completion

Once you've earned all 7 badges, you've officially gone from **ZERO → HERO** in EC2!

You now have hands-on experience with:
- Cloud infrastructure
- Linux system administration
- Web server deployment
- Storage management
- Security configuration
- Cost management

**Next Steps:**
- Explore other AWS services (S3, RDS, Lambda)
- Learn about auto-scaling and load balancing
- Study for AWS Certified Cloud Practitioner
- Build your own projects on EC2

⚠️ Important Reminders

- **Terminate instances** when done to avoid charges
- **Delete EBS volumes** that aren't needed
- **Monitor** your AWS billing dashboard regularly
- **Use Free Tier wisely** (750 hours/month for t2.micro)

Contributing

Found a typo or have suggestions? Feel free to:
- Open an issue
- Submit a pull request
- Share your completion screenshots

📄 License

This challenge is open-source and free to use for educational purposes.

**Ready to begin?** Start with [LEVEL 0](#level-0-aws-warm-up-) and let's launch your cloud journey!

*"Every expert was once a beginner. Today, you start your cloud journey."*
