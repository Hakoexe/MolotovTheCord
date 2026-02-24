
<img width="504" height="424" alt="MolotovTheCord" src="https://github.com/user-attachments/assets/6c2cde70-7cc8-4088-8046-5ee43d948d5f" />

# MolotovTheCord
**A precision guide for scorched-earth Discord cleanup.**  
*Light the match. Watch your message history turn to ash.*

---

## ⚠️ Important Disclaimer

This repository is provided strictly for **educational and informational purposes only**.  
It explains how users can review and delete their own Discord data.

- This project is **not a bot**
- The information presented here is **not intended to encourage, promote, or facilitate the circumvention of Discord's Terms of Service or any platform rules**.
- Certain automation methods discussed may violate Discord's Terms of Service. You are solely responsible for ensuring your actions comply with all applicable rules and policies.
- I, the author does **not endorse, support, or take responsibility** for misuse of the information provided.
- Any actions you take are done **at your own risk**.
- Data deletion is **permanent and irreversible**.

By using this repository, you acknowledge that you understand these risks and agree to use the information responsibly and in compliance with Discord's Terms of Service.

---

# 🔥 How to Delete Your Discord Data

## 1️⃣ Request Your Data From Discord

📘 Official guide: ["Requesting a Copy of Your Data"](https://support.discord.com/hc/en-us/articles/360004027692-Requesting-a-Copy-of-your-Data)

**Steps (Desktop / Browser):**

1. Open **Discord**
2. Go to `User Settings > Data & Privacy`
3. Click `Request Data`
4. Select `Messages`
5. Confirm the request

![7997b816-8583-4aba-89e9-61d6c17536c2](https://github.com/user-attachments/assets/0f841d88-7396-4c20-84e8-c6dfaf5588e4)

---

## 2️⃣ Wait

The data request can take **up to 30 days**.  
Discord will send a download link to the email address linked to your account when you made the request
Your request will be canceled if you disable or delete your account before receiving the download link.
> NOTE: Your Discord account must be verified with an email address before requesting your data. Having trouble accessing your account? Contact privacy@discord.com for help with your data request.
---

## 3️⃣ Extract Your Data

1. Download the ZIP file from the email from Discord
2. Extract it
3. Locate the `messages` folder

Your extracted structure should look like:

`discord_data/`

`├── account/`

`├── messages/`

`├── servers/`

`└── index.html`

---

## 4️⃣ Use Discorch 

Go to: [Discorch](https://discorch.org/)

Discorch works **entirely offline**, does **not submit your data**, and helps you:

- Create deletion requests for:
  - Servers you no longer access
  - Group DMs you’ve left
- Automate remaining deletion tasks (optional)

---

# 5️⃣ Two Paths

You can choose between:

- **A. Play It Safe** – Fully ToS compliant  
   Follow Discord's Terms. Only delete messages from servers and group chats you can no longer access. 
- **B. Live on the Edge** – Automation, violates ToS
   Understand the risks. Automate deleteion of 1:1 DMs against Discord's terms.
  
---

## 🅰️ Play It Safe (ToS Compliant)

1. Go to [Discorch](https://discorch.org/)  
2. Select **Play It Safe**
3. Leave **Show 1:1 DMs and servers you still access** unchecked
4. Click `Select Message Folder` and choose the extracted **messages** folder
5. A pop-up will come up - Click on `Upload`

> Channels will appear as: Unknown Channel in Server or Group DMs 

6. Select all channels you wish to be deleted 
7. Click `Export` > 
8. Click `Request Data Deletion`  

**Discorch will guide you to submit a Discord support ticket**

Before submitting as a reminder
Ensure:
- ✅ Attach the **CSV file** (not JSON)  
- ✅ Complete all form fields  
- ✅ Email address is correct

> After submitting your request, you'll receive updates about its status via email from Discord's privacy team.

---

**Discord's Reply Process**
Discord will likely reply with "This channel is reserved for individuals..." You'll need to use the template below to get your request reviewed properly

 **Response Template**
 ```
Dear Privacy Team,

I believe there may have been a misunderstanding regarding my bulk message deletion request submitted through the official privacy form. This is a legitimate privacy request submitted via the correct channel.

I submitted this request under "Delete your personal data on Discord" and included a properly formatted CSV file containing the message IDs I wish to have deleted. I understand that Discord will only process deletions for messages in servers and group DMs that I have already left, and I have ensured this requirement is met.

For reference, previous tickets like #50057053 demonstrate the standard process for handling such requests. Since December 1, 2024, Discord's privacy team accepts CSV files for these requests, which I have provided in the correct format.

Could you please review my request again and process it according to Discord's established privacy deletion procedures?

Thank you for your time and assistance.

Best regards,
[Your Name]
```

After this step, continue to 5B for 1:1 DM deletion.

Discord does **NOT** delete 1:1 DMs via privacy requests.

---

## 🅱️ Live on the Edge (Automation)

## How this works:
This method hooks into Discord's web client and uses the exact same deletion code that runs when you manually press delete on a message. It respects Discord's rate limits and does not access your authentication token directly.
While this violates Discord's terms of service, we have not observed any account restrictions in practice. This is considered the safest automation method available, but use your own judgement.
Requires installing browser extensions and userscripts. The setup process is guided in the next steps.
This approach does violate the terms, but it still keeps the automation within Discord's own client code. We have not observed any account restrictions in practice, but use your own judgement when proceeding with this flow.

> Note: No account restrictions observed in practice
 
---

## Setup

1. Install [Brave Browser](https://brave.com/download/)
2. Open [Discorch](https://discorch.org/) in Brave
3. Select **Live on the Edge**
4. Toggle off `include server and group chats` 
>We will use filters to select DMs/Group Dms and Servers
5. Click `I understand the risk`

## Install Extensions & Scripts

1. **Violentmonkey**: [Chrome Web Store](https://chrome.google.com/webstore/detail/violentmonkey/jinjaccalgkegednnccohejagnlnfdag)  
2. **Vencord Userscript**: [Raw GitHub Link](https://raw.githubusercontent.com/Vencord/builds/main/Vencord.user.js)  
3. **DiscorchDeleter Userscript**: [GitHub Release](https://github.com/Darker-Ink/DiscorchDeleter/releases/download/v1.1.0/discorchdeleter.user.js)  
4. Click `Select Message Folder` and choose the extracted **messages** folder
5. A pop-up will come up - Click on `Upload`

---

## Deleting 1:1 DMs & Group DMs

1. In the top right Click `Filters Active`
   - DirectMessage
   - Group DM
2. Select all channels you want to delete
3. Click  `Export` > `Export for DiscorchDeleter`
4. Leave unchecked:
   - ❌ Include full message content and attachments
> Only select this if you are trying to archive your messages, as selecting this will not work in discorch
5. Click `Download JSON for DiscorchDeleter`
6. Rename file to: DMS_AND_GROUP_DMS_ALL.json

---

## Deleting Server Messages

1. In the top right Click `Filters Active`
   - Text Channel
   - Announcement Channel
   - Public Thread
   - Voice Channel
   - Announcement Thread
2. Select all channels you want to delete
3. Click  `Export` > `Export for DiscorchDeleter`
4. Leave unchecked:
   - ❌ Include full message content and attachments
> Only select this if you are trying to archive your messages, as selecting this will not work in discorch
5. Click `Download JSON for DiscorchDeleter`
6. Rename to: SERVER_MESSAGES_ALL.json

---
## 🔥 Using DiscorchDeleter

1. In Brave open a new tab and log into [Discord](https://discord.com/).
> You must use Discord in a brave web browser for this to work!!
2. Once logged in you should see DiscorchDeleter 
> you can move this window around in discord and adjust the size
<img width="710" height="754" alt="image" src="https://github.com/user-attachments/assets/9f29b08d-2c57-48be-8a36-f8c534d69d77" />

3. Click on `File`
4. Select the **DMS_AND_GROUP_DMS_ALL.json**
5. set the **Delete Interval** to `2500`ms
6. Click `Start`
> This can take some time to be completed depending on how large the JSON file is.
> ⚠️ Note: This can only be done one at a time. You can not open up two browser tabs to do this at the same time.
> ** If you select one DM during your JSON file setup and find that DM in discord you can watch in real time the messages being deleted.**

7. Once this is completed you can repeat Steps 1-6 to complete for **SERVER_MESSAGES_ALL.json**
> ⚠️ Note: This can only be done one at a time. You can not open up two browser tabs to do this at the same time.

---

# ✅ Final Step: Sanity Check

After:
- Running automation
- Submitting privacy requests

Wait **30 days**, then request your data again to confirm deletion success.

---

# License

This repository is provided for **educational purposes only**. Use responsibly.
Link to orginal source: https://codeberg.org/discorch/discorch

