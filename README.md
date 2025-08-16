# EthStorage V1 Trusted Setup Ceremony Guide

This guide will help you participate in the **EthStorage V1 Trusted Setup Ceremony** 

---

## 📌 Requirements
- Ubuntu 22.04 VPS (2 vCPU, 4GB RAM, 30GB+ SSD recommended)
- Basic SSH access
- GitHub account (for authentication)
  - Account age: ≥ 1 month  
  - At least 1 public repository  
  - Follow ≥ 5 accounts & have ≥ 1 follower  
  - Allow tool to read/write GitHub Gists

---

## 🛠 Step-by-Step Setup

### 1️⃣ Update & Install Dependencies
```
apt update && apt upgrade -y
apt install -y curl git build-essential

```

### 2️⃣ Install Node.js v18 & npm v9.2
```

curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
apt install -y nodejs
npm install -g npm@9.2
```

### 3️⃣ Check Versions


```
node -v
npm -v
```

### 4️⃣ Create Temporary Directory

```
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp

```
### 5️⃣ Install Phase2 CLI

```
npm install -g @p0tion/phase2cli
```

### 6️⃣ Verify CLI Installation


```
phase2cli --version
```

### 7️⃣ Authenticate with GitHub

```
phase2cli auth
```

* Follow the browser link shown in the terminal
* Login to GitHub & authorize **p0tion** to access Gists
* Return to terminal

### 8️⃣ Contribute to the Ceremony

```
screen -S ceremony
```

```
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

---

## 🧹 Cleanup After Contribution

```
phase2cli clean
phase2cli logout
cd ~ && rm -rf ~/trusted-setup-tmp
```

---

### 🖥 Screen Session Controls
- Detach: CTRL + A, then D  
- Reattach: `screen -r ceremony`

## 💡 Pro Tips

 **Destroy VPS after participation for maximum security**

---

## ✅ Final Step
- Once all commands are run, wait for your queue.  
- When your turn comes, the tool will process your contribution.  
- Done! 🎉 You have successfully contributed to the EthStorage V1 Trusted Setup Ceremony.

---
🟢 That’s it!

