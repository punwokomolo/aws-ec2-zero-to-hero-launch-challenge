## LEVEL 6: Instance Lifecycle Management

**Objective:** Control your EC2 instance states.

---

### 🔄 Perform These Actions

From the EC2 Console:

1. **Stop Instance**  
   - Select your instance  
   - Click **Instance State → Stop**  
   - Wait until the state shows **Stopped**  
   - Note the **Public IP** (it will disappear once stopped)

2. **Start Instance**  
   - Click **Instance State → Start**  
   - Wait until the state shows **Running**  
   - Compare the new **Public IP** with the old one (it usually changes)

3. **Reboot Instance**  
   - Click **Instance State → Reboot**  
   - Check if the **Public IP** changed (it usually stays the same)

4. **Check EBS Data**  
   - [SSH](../level-2-connect-ssh/README.md#run) back into your instance  
   - Run: `ls /mydata`  
   - Verify your test file still exists (your EBS volume data should persist)

---

### 📝 Answer These Questions

Create a file named `lifecycle-observations.txt` and answer:

1. What happened to the Public IP when you stopped and started the instance?  
   Answer: _______________________________________________

2. What happened to the Public IP when you rebooted the instance?  
   Answer: _______________________________________________

3. Did your EBS volume data remain after stopping and starting?  
   Answer: _______________________________________________

4. What's the difference between Stop and Terminate?  
   Answer: _______________________________________________  
   _______________________________________________

---

### 📸 Required Screenshots

Save these screenshots in your project folder:

- **01-instance-running.png**  
  Instance running with original Public IP

- **02-instance-stopped.png**  
  Instance in stopped state

- **03-instance-started-new-ip.png**  
  Instance running again with new Public IP highlighted

- **04-ebs-data-persisted.png**  
  Terminal showing `/mydata` contents still exist

---

### 🔑 Quick Reference

| Action    | Instance State | Data       | IP        | Cost       |
|-----------|----------------|------------|-----------|------------|
| Stop      | Paused ✅      | Kept ✅    | Changes   | EBS only   |
| Reboot    | Restarts ✅    | Kept ✅    | Same      | Full       |
| Terminate | Deleted ❌    | Lost* ❌   | Gone      | $0         |

*Unless EBS "Delete on Termination" is disabled

---

### ⚠️ Important

**DO NOT terminate your instance yet!** You still need it for Level 7.

---

### 📤 Submission

```bash
git add level-6-lifecycle/
git commit -m "Complete Level 6: Lifecycle Management"
git push origin main
```

---

### ✅ Completion Checklist

- [ ] Stopped and started instance  
- [ ] Rebooted instance  
- [ ] IP behavior documented  
- [ ] EBS persistence verified  
- [ ] 4 questions answered  
- [ ] 4 screenshots saved  
- [ ] Files committed  

---

### 🏆 Badge Earned: 🟩 Lifecycle Commander

Fill out this form to earn your badge: https://forms.gle/C6jcziHv615Zypug6

**Next:** → [Level 7](../level-7-cost-optimization)
