Certainly! Here’s your guide formatted in Markdown for **LEVEL 1: Launch Your First EC2 Instance**:

---

# LEVEL 1: Launch Your First EC2 Instance

**Objective:**  
Create and run your first virtual computer in AWS.

---

#### 🛠️ Steps

1. **AWS Console**  
   - Search for **"EC2"**  
   - Click **Launch Instance**
     <img width="1901" height="967" alt="image(2)" src="https://github.com/user-attachments/assets/54bdf40b-dbaf-4a05-acdf-51dee04711bf" />

2. **Configure:**
   - **Name:** `ZeroToHero-EC2-{Your Name}`
   - **AMI:** Amazon Linux 2023 (Free tier)
   - **Instance Type:** `t3.micro (Free tier elligible)`
     <img width="1911" height="934" alt="image(3)" src="https://github.com/user-attachments/assets/f432fc62-393e-4a31-b41d-7e557892cb1a" />


3. **Create Key Pair:**
   - **Name:** `zth-keypair`
   - **Type:** RSA
   - **Format:** Check `.pem`
   - **DOWNLOAD and save it in a SAFE location**  
     <video width="1911" height="934" alt="image(3)" src="https://github.com/user-attachments/assets/9ecb2e76-caed-4fcf-ad40-d4f1f6954c2e" />


4. **Network Settings:**
   - **Create security group:** `zth-security-group`
   - **Allow:** SSH (port 22) from **"My IP"**
     <video width="1911" height="934" alt="image(3)" src="https://github.com/user-attachments/assets/9a7374b8-97ce-445b-95b1-5415e0af32da" />

5. **Launch Instance**
   <img width="1907" height="902" alt="image(3)" src="https://github.com/user-attachments/assets/7bbd59a1-7752-4a1b-988e-c7f074abaa4b" />


---

#### 📸 Required Screenshots

Save these screenshots in this folder:

- **01-instance-running.png**
  - Instance State: Running
  - Instance ID visible

- **02-instance-details.png**
  - Instance ID
  - Public IPv4 address
  - Instance type (`t2.micro`)

- **03-launch-log.png** (optional)
  - Initial launch confirmation

---

#### 📝 Also create a file named `instance-info.txt` and fill in the information:

```
Instance ID: i-xxxxxxxxxxxxx
Public IPv4: xx.xx.xx.xx
Availability Zone: us-east-1x
Key Pair Name: zth-keypair
```

---

#### 📤 Submission

```bash
git add level-1-launch-ec2/
git commit -m "Complete Level 1: Launch EC2 Instance"
git push origin main
```

---

#### ✅ Validation

- **Instance state:** Running
- **Status checks:** 2/2 passed
- **Screenshots saved**
- **instance-info.txt created**
- **Files committed**

---

#### 🏆 Badge Earned: 🟡 Instance Launcher

**Next:** → [Level 2](https://github.com/awssccuba/aws-ec2-zero-to-hero-launch-challenge/blob/main/level-2-connect-ssh/README.md)
