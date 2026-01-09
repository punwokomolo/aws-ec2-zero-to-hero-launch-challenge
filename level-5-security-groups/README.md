LEVEL 5: Security Group Deep Dive
Objective: Master cloud firewalls through experimentation.

🔬 Experiment
Test 1: Remove HTTP Access

Go to Security Groups → zth-security-group
Delete the HTTP (port 80) rule
Try to access http://<Your-IP> in browser
Record what happens

Test 2: Restore Access

Add back the HTTP rule
Refresh browser
Record what happens


✍️ Write Your Explanation
Create security-group-explanation.txt:
What are Security Groups?
Line 1: _______________________________________________
Line 2: _______________________________________________

What I learned from the experiment:
_______________________________________________
_______________________________________________

📸 Required Screenshots
Save in this folder:

01-rules-with-http.png

Security group showing HTTP rule enabled


02-rules-without-http.png

Security group with HTTP rule removed


03-browser-blocked.png

Browser unable to connect (rule removed)


04-browser-working.png

Browser working again (rule restored)




📋 Final Security Group Rules
Your zth-security-group should have:

 SSH (22) from your IP
 HTTP (80) from anywhere (0.0.0.0/0)


📤 Submission
bashgit add level-5-security-groups/
git commit -m "Complete Level 5: Security Groups"
git push origin main

✅ Completion

 HTTP rule tested (remove + restore)
 Explanation written
 4 screenshots saved
 Files committed

🏆 Badge Earned: 🔵 Security Defender
Next: Level 6 →
