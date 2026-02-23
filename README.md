
<img width="504" height="424" alt="MolotovTheCord" src="https://github.com/user-attachments/assets/6c2cde70-7cc8-4088-8046-5ee43d948d5f" />

# MolotovTheCord
**A precision guide for scorched-earth Discord cleanup.**  
*Light the match. Watch your message history turn to ash.*

---

## ⚠️ Important Disclaimer

This repository is a **guide** on reviewing and deleting your Discord data.  

- This is **not a bot**.  
- Some automation methods **may violate Discord's Terms of Service**.  
- You assume all risk if you use automation.  
- Data deletion is **permanent**.  

Use responsibly.

---

# 🔥 How to Delete Your Discord Data

## 1️⃣ Request Your Data From Discord

Before deleting anything, request your full Discord data package.

📘 Official guide: ["Requesting a Copy of Your Data"](https://support.discord.com/hc/en-us/articles/360004027692-Requesting-a-Copy-of-your-Data)

**Steps (Desktop / Browser):**

1. Open **Discord**
2. Go to **User Settings > Privacy & Safety**
3. Click **Request Data**
4. Confirm the request


![7997b816-8583-4aba-89e9-61d6c17536c2](https://github.com/user-attachments/assets/0f841d88-7396-4c20-84e8-c6dfaf5588e4)

---

## 2️⃣ Wait

The data request can take **up to 30 days**.  
You will receive an email when your data package is ready.

---

## 3️⃣ Extract Your Data

1. Download the ZIP file from Discord
2. Extract it
3. Locate the `messages` folder

Your extracted structure should look like:
discord_data/
├── account/
├── messages/
├── servers/
└── index.html


---

## 4️⃣ Use Discorch

Go to: [https://discorch.org/](https://discorch.org/)

Discorch works **entirely offline**, does **not submit your data**, and helps you:

- Create deletion requests for:
  - Servers you no longer access
  - Group DMs you’ve left
- Automate remaining deletion tasks (optional)

---

# 5️⃣ Two Paths

You can choose between:

- **A. Play It Safe** – Fully ToS compliant  
- **B. Live on the Edge** – Automation, violates ToS

---

# 🅰️ Play It Safe (ToS Compliant)

1. Go to [https://discorch.org/](https://discorch.org/)  
2. Select **Play It Safe**
3. Leave **Show 1:1 DMs and servers you still access** unchecked
4. Click **Select Message Folder** and choose the extracted `messages` folder
5. Upload the folder

Channels may appear as:
Unknown Channel in X


6. Click **Export > Request Data Deletion**  

Discorch will guide you to submit a Discord support ticket.
Before submitting as a reminder
Ensure:
- ✅ Attach the **CSV file** (not JSON)  
- ✅ Complete all form fields  
- ✅ Email address is correct  

---

Discord will likely reply with "This channel is reserved for individuals..." You'll need to use the template below to get your request reviewed properly.

### Response Template
Dear Privacy Team,

I believe there may have been a misunderstanding regarding my bulk message deletion request submitted through the official privacy form. This is a legitimate privacy request submitted via the correct channel.

I submitted this request under "Delete your personal data on Discord" and included a properly formatted CSV file containing the message IDs I wish to have deleted. I understand that Discord will only process deletions for messages in servers and group DMs that I have already left, and I have ensured this requirement is met.

For reference, previous tickets like #50057053 demonstrate the standard process for handling such requests. Since December 1, 2024, Discord's privacy team accepts CSV files for these requests, which I have provided in the correct format.

Could you please review my request again and process it according to Discord's established privacy deletion procedures?

Thank you for your time and assistance.

Best regards,
[Your Name]


> After this step, continue to 5B for 1:1 DM deletion.  
> Discord does **NOT** delete 1:1 DMs via privacy requests.

---

# 🅱️ Live on the Edge (Automation)

⚠️ This violates Discord’s Terms of Service. Proceed at your own risk.  

- Uses Discord’s web client code
- Respects rate limits
- No direct access to your authentication token
- No account restrictions observed in practice — still risky

---

## Setup

1. Install **Brave Browser**
2. Open [https://discorch.org/](https://discorch.org/) in Brave
3. Select **Live on the Edge**
4. Toggle:
   - Enable **Include servers and group chats**  
   - Disable if only deleting 1:1 DMs
5. Click **I understand the risk**

## Install Extensions & Scripts

1. **Violentmonkey**: [Chrome Web Store](https://chrome.google.com/webstore/detail/violentmonkey/jinjaccalgkegednnccohejagnlnfdag)  
2. **Vencord Userscript**: [Raw GitHub Link](https://raw.githubusercontent.com/Vencord/builds/main/Vencord.user.js)  
3. **DiscorchDeleter Userscript**: [GitHub Release](https://github.com/Darker-Ink/DiscorchDeleter/releases/download/v1.1.0/discorchdeleter.user.js)  

> once all of these have been installed on the Brave Browser, go ahead and open a new tab in the brave browser and log in to [Discord](https://discord.com/).
> You must use Discord in a brave web browser for this to work!!

---

# Deleting 1:1 DMs & Group DMs

1. Upload your `messages` folder
2. Apply **Filters**:
   - DirectMessage
   - Group DM
3. Select all conversations you want to delete
4. Click **Export > Export for DiscorchDeleter**
5. Leave:
   - ❌ Include full message content unchecked 
   - ❌ Include attachments unchecked
6. Click **Download JSON**
7. Rename file to: DMS_AND_GROUP_DMS_ALL.json


---

# Deleting Server Messages

1. Clear filters
2. Select channel types:
   - Text Channel
   - Announcement Channel
   - Public Thread
   - Voice Channel
   - Announcement Thread
3. Optionally: Only show messages from servers you’ve left
4. Select messages
5. Click **Export > Export for DiscorchDeleter**
6.  Leave:
   - ❌ Include full message content unchecked 
   - ❌ Include attachments unchecked
7. Download JSON
8. Rename to: SERVER_MESSAGES_ALL.json


---

# Running the Scripts

- Run one JSON file at a time
- Expect processing time due to rate limits
- Errors may appear for servers you no longer have access to
- Use Play It Safe method as backup for missing messages

---

# ✅ Final Step: Sanity Check

After:

- Running automation
- Submitting privacy requests

Wait **30 days**, then request your data again to confirm deletion success.

---

# 🧨 Recommended Approach

For maximum coverage:

1. Submit Privacy Request (5A)  
2. Run Automation for 1:1 DMs (5B)  
3. Re-request data after 30 days

---

# License

This repository is provided for **educational purposes only**. Use responsibly.
Link to orginal source: https://codeberg.org/discorch/discorch


