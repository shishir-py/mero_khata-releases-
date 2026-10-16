# Mero Khata — Privacy Policy

_Last updated: 16 October 2026_

Mero Khata (मेरो खाता) is a personal expense tracker for Android. It is built to work entirely on your
phone. This policy explains what the app accesses, what it stores, and what it never does.

## Summary

- **No data leaves your phone through the app.** Mero Khata has no internet permission, no account,
  no server, no ads, no analytics and no tracking libraries.
- **We (the developer) never receive any of your data.**
- Your records are stored in an **encrypted database** (SQLCipher, AES-256) in the app's private storage.

## What the app accesses, and why

| Access | When | Purpose |
|---|---|---|
| SMS inbox (`READ_SMS`) | Only if you allow it (full version) | To find bank and wallet transaction messages (money debited, credited, withdrawn, paid, refunded) so you do not have to type them. |
| Incoming SMS (`RECEIVE_SMS`) | Only if you allow it (full version) | To notice new transaction messages as they arrive. |
| Text you share or paste into the app | When you do it | To find transactions in that text. |
| Files and folders you pick | When you export, restore, or choose an automatic-backup folder | To write or read the backup file you chose. |
| Fingerprint / screen lock | Only if you turn on the app lock | Unlocking the app; handled entirely by Android. |
| Notifications | Only for reminders you schedule | Local reminders for upcoming income and expenses. No push server is used. |

The app cannot send SMS, does not read contacts, call logs or location, and cannot use the internet.

## How SMS are processed

Messages are analysed **only on your phone** by built-in rules. One-time passwords (OTPs), verification
codes, promotions, telecom messages and personal messages are skipped. **The full text of a message is
never stored.** For a detected transaction the app keeps only the extracted details — amount, date,
bank or wallet, the last digits of the account, merchant or counterparty, reference — and, only if the
"Keep short message excerpts" setting is on, up to 140 masked characters of the message. Every detected
item waits for you to review it. For each processed message the app stores a one-way hash so the same
message is not imported twice.

SMS data is never shared, sold or transferred to anyone, and is never used for advertising,
credit scoring or lending.

## What is stored on your phone

Transactions you confirm or enter; accounts, banks and categories; scheduled income and expenses;
detected items waiting for review; settings; and a small encrypted list of upcoming reminders.
All of it stays in the app's private storage on your phone.

## Backups

- **Backups you export** are files encrypted with a password you choose (AES-256-GCM, key derived with
  PBKDF2-SHA256). They are saved where you choose. Without the password they cannot be read — not even by us.
- **Automatic backups** (if you turn them on) are encrypted the same way and saved to the folder you pick.
  Android's own device backup (to your Google account, under Google's privacy policy) and phone-to-phone
  transfer may copy these encrypted backup files only. The database, its keys and your settings are never
  included in Android backup.

## Your choices and deleting data

- Revoke SMS access at any time in Android settings, or use the Lite version, which has no SMS permission.
- Delete individual transactions or detected items at any time.
- **Settings → Delete all data** permanently erases the database, its key and all settings.
- Uninstalling the app or using Android's "Clear storage" also permanently deletes everything that was
  not exported. Backup files you saved elsewhere remain until you delete them.

Because no data is sent to us, there is no account to delete and no copy of your data held by the developer.

## Security

Data is encrypted at rest with a key protected by the phone's Android Keystore (or by your password, if you
choose password protection). No app can protect data on a rooted or compromised phone, or from someone who
knows your password.

## Children

Mero Khata is a personal finance tool intended for adults. It is not directed at children under 13.

## Changes

If this policy changes, the new version will be published at this address with a new date.

## Contact

Questions about this policy: open an issue at
https://github.com/shishir-py/mero_khata-releases-/issues
