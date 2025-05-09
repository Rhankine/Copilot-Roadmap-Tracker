# 🧭 Microsoft 365 Copilot Roadmap Notifier

A Power Automate solution that posts **new and updated items** from the [Microsoft 365 Roadmap](https://www.microsoft.com/en-us/microsoft-365/roadmap) to a Microsoft Teams channel using Adaptive Cards. Ideal for tracking Copilot and modern workplace developments.

---

## ✨ Features

![image](https://github.com/user-attachments/assets/4e8f13a4-f97f-42dd-b4c7-09336438ae71)
- Detects new vs. updated roadmap items
- Highlights GA date and rollout status
- Posts Adaptive Cards to Teams for easy visibility
- Includes separate card designs for new and updated items
- Fully customizable and deployable via solution package

---

## 🚀 Installation

1. **Download the solution zip file** from the [GitHub repository](https://github.com/YOUR-USERNAME/copilot-roadmap-tracker) under `/CopilotRoadmapTracker_1_0_0_1.zip`
2. Go to [Power Automate](https://make.powerautomate.com/)
3. Navigate to **Solutions > Import**
4. Upload the downloaded zip file
5. During import:
   - Assign required connections (Teams, RSS, etc.)
   - Provide values for environment variables if prompted

---

## ⚙️ Configuration

### 🔍 How to find your Teams Channel ID and Team ID

1. Go to Microsoft Teams and navigate to the channel where you want to post the roadmap updates.

2. Click the `...` next to the channel name → **Get link to channel**.

3. Paste the link into a text editor. It will look like this:

   ```
   https://teams.microsoft.com/l/channel/19%3aabc123xyz456%40thread.tacv2/General?groupId=...&tenantId=...
   ```

4. The **Channel ID** is the part after `/channel/` and before the next `/`:

   ```
   19:abc123xyz456@thread.tacv2
   ```

5. Use this ID as the value for the **Teams channel ID** field in the flow.

### 🆔 How to find your Team (Group) ID

1. Follow the same steps as above to get the link to the channel.

2. In the link, locate the `groupId` parameter:

   ```
   https://teams.microsoft.com/l/channel/...?...groupId=abcdef12-3456-7890-abcd-ef1234567890&tenantId=...
   ```

3. The long string after `groupId=` is your **Team ID**:

   ```
   abcdef12-3456-7890-abcd-ef1234567890
   ```

4. You may need this value if you're calling Microsoft Graph or working with advanced Teams connectors.

---

## 🧩 Customization

You can modify the card layouts by editing the files in the `adaptive-cards/` folder:

- `new-item.json`
- `updated-item.json`

Paste your changes into the corresponding Post Adaptive Card action in the flow.

---

## 📄 License

This project is licensed under a modified MIT License. You are free to use and adapt the solution, but **you may not resell or package it as part of a commercial product**.

See [`LICENSE`](LICENSE) for full terms.

---

> This project is community-built and is **not affiliated with or supported by Microsoft.**
