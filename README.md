# 🚀 DNS Configuration on Windows Server 2022 – A Quick Overview 🖥️🌐
Whether you're building a lab environment or setting up enterprise infrastructure, understanding how to configure DNS (Domain Name System) is essential for network communication and domain management.

---

### 🧠 What You’ll Learn
- How to install the DNS Server role via Server Manager (Image 2)
- How to verify DNS setup in the Server Manager dashboard (Image 3)
- How to manage DNS zones and records using DNS Manager (Image 1)


## 🔧 Step-by-Step DNS Configuration

### 🔹 1. Install the DNS Server Role
- Open **Server Manager**
- Navigate to: **Manage > Add Roles and Features**
- Select **DNS Server**, then proceed through the wizard to install

### 🔹 2. Configure Forward Lookup Zone
- Open **DNS Manager**
- Right-click **Forward Lookup Zones** > **New Zone**
- Choose **Primary Zone**
- Name your domain (e.g., `Server.local`) and complete the setup

### 🔹 3. Create Host (A) Records
- Within your zone, right-click > **New Host (A or AAAA)**
- Add device entries (e.g., `dc01.server.local → 192.168.1.10`)

### 🔹 4. Set Reverse Lookup Zone *(Optional but Recommended)*
- Enables IP-to-hostname resolution
- Right-click **Reverse Lookup Zones** > **New Zone**
- Follow the wizard to configure

### 🔹 5. Test DNS Resolution
- Use `nslookup` or `ping` from client machines to validate DNS functionality

---


### ScreenShots WalkThrough
| Steps | Description | ScreenShot |
|-------|-------------|------------|
|  1️⃣  | Shows configured forward & reverse zones, AD-integrated folders, and forwarders. | ![Image Alt](https://github.com/Shaifalim02/Windows_Server_2022/blob/8990e543770d816af5d0fbb52cf10a2ac3182821/image.png) |
| 2️⃣   | DNS Server role is selected and installed via Server Manager. | ![Image Alt](https://github.com/Shaifalim02/Windows_Server_2022/blob/7016a5884228af6273629b74566805a92eb187f4/image%201.png) |
| 3️⃣   | Overview of installed roles (AD DS, DNS, File Services) and their status. | ![Image Alt](https://github.com/Shaifalim02/Windows_Server_2022/blob/68191814b846196a0190463d8edcac2bdaac953a/image%202.png) |

---

## 🛡️ Bonus: Configure Forwarders
- Improve external name resolution by adding public DNS like **8.8.8.8**
  - In DNS Manager, right-click server > **Properties**
  - Go to **Forwarders** tab and add external DNS IPs

---

## ✅ Why It Matters
DNS is the **backbone of Active Directory** and a vital component in enterprise networks. A properly configured DNS server ensures smooth authentication, service discovery, and name resolution across the domain.

---

### 💬 Got Tips or Troubleshooting Stories?
Have you configured DNS on Windows Server 2022? Share your best practices or common gotchas in the [Discussions](https://github.com/Shaifalim02/Windows_Server_2022/discussions) section!

---



### 🙌 Author

Shaifali Shaifali
- 🔗 Sharing labs and real-world IT demos.
- 📍 Connect with me on [LinkedIn](https://www.linkedin.com/in/shaifali-shaifali/) | More labs on [GitHub](https://github.com/Shaifalim02)
