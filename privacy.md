---
layout: default
title: Privacy Policy — Academy Director
---

# Privacy Policy

**Effective date:** 2026-05-14
**App:** Academy Director (iOS)
**Operator / Controller:** Hashim AlMahmeed (sole developer)
**Contact:** hashimaakbar@gmail.com

This Privacy Policy explains what data Academy Director collects, why, how it is stored, and the choices you have. The app now uses a cloud backend so multiple staff members in the same academy can share data across their devices. We collect the minimum needed to run that service.

If anything in this policy is unclear, please email us at **hashimaakbar@gmail.com**.

## 1. Summary

- We collect: your **email address** and **password** (for sign-in), a **display name** you choose, and the **academy data you enter** in the app (branches, members, memberships, sessions, attendance, equipment, costs, alerts).
- We use these to: authenticate you, keep your data in sync across your devices, and let your teammates (with codes you issue) see the same data.
- We do **not** sell or share your data with third parties for advertising. No analytics SDKs, no ad SDKs, no third-party trackers.
- Data is processed and stored by **Supabase Inc.** (our database and authentication provider) on servers in the region you initially provisioned, and on your device as a local cache.
- You can delete your account from inside the app at any time (Settings → Account → **Delete My Account**), which permanently removes your record from our servers.

## 2. Data we collect and why

### 2.1 Account information

- **Email address** — used as your unique login identifier. Required.
- **Password (hashed)** — handled by Supabase Auth. We never see your plaintext password; it is stored as a bcrypt-hashed credential by our backend provider.
- **Display name** — a name you choose for yourself (often your first name); shown to other staff in your academy.
- **Role** — one of Manager, Co-Manager, Administrator, Coach, or Other. Set by the academy's manager.

### 2.2 Academy operational data

Created and edited by you. Linked to your academy, visible to other signed-in staff of the same academy:

- Branches, courts, coaches (profile info you enter), memberships (group / private / other), members (names, ages, phone numbers, attendance, absences, cancellations, notes), scheduled sessions, equipment inventory, costs, and generated reports.

This information may include personal information about your academy's **members** (e.g. children attending classes). You are responsible for ensuring you have a lawful basis to enter that information — see Section 7.

### 2.3 Optional academy assets

- An **academy logo image** you choose via the iOS photo picker. Used inside the app, on report PDFs, and as the report watermark. Stored alongside your other settings; not exposed publicly.
- Contact info you optionally enter (address, phone, email) for the academy itself. Used inside the app and on reports.

### 2.4 Information we do **not** collect

- We do not use third-party analytics, advertising, crash-reporting, or tracking SDKs.
- We do not collect device identifiers, IDFA, advertising IDs, IP addresses (beyond standard request logs at our infrastructure provider), location, contacts, or browsing activity.
- We do not access your photo library beyond the single image you explicitly choose via the iOS picker.

## 3. How and where your data is stored

We use **Supabase Inc.** ([https://supabase.com](https://supabase.com)) as our backend service provider for both authentication and the Postgres database. Supabase hosts data on Amazon Web Services in the region selected when the project was created. Their security and privacy practices are documented at [https://supabase.com/privacy](https://supabase.com/privacy) and [https://supabase.com/security](https://supabase.com/security).

In addition to the server, a copy of your academy's data is cached locally on your iOS device so the app can work briefly when offline. This local cache is stored in the app's sandbox and is removed if you uninstall the app.

Transport between your device and Supabase is encrypted with TLS (HTTPS / WSS). Data is encrypted at rest at the storage layer by AWS.

## 4. Sharing

Your data is shared with the following parties, only as needed to operate the service:

- **Supabase Inc.** — sub-processor that hosts our database, authentication, and realtime sync. They process the data on our instructions.
- **Apple** — only to the extent your device backs up its local cache to your personal iCloud, which is outside our control.
- **Other members of your academy** — staff your manager invites (using invite codes generated inside the app) see the same academy data, scoped by row-level security so no other academy's data is visible.

We do **not** sell or rent personal information. We do not share it for advertising or cross-context behavioural advertising purposes.

## 5. Retention

We retain your data for as long as your account exists and you operate an academy. Specifically:

- **Account & profile**: kept until you (or your manager) delete the account.
- **Academy operational data**: kept until the manager deletes the academy or the relevant rows. The manager has unilateral control over the academy's data.
- **Backups**: Supabase keeps point-in-time recovery snapshots of the database for up to 7 days (configurable). After that window snapshots are purged.
- **Deletion**: When you delete your account, your profile row is removed immediately from the database. Cascade rules also remove any data that belonged solely to you. If you were the only manager of an academy, your academy and all its data are deleted with you.

## 6. Your rights

Depending on where you live, you may have one or more of the following rights:

- **Access** — request a copy of the personal information we hold about you.
- **Rectification** — correct inaccurate information (most of this can be done in-app).
- **Deletion / "Right to be forgotten"** — delete your account in-app (Settings → Account → **Delete My Account**) or email us.
- **Portability** — request export of your account data in a machine-readable format.
- **Objection / Restriction** — object to or restrict certain processing.
- **Withdraw consent** — where processing was based on consent (e.g. photo library access).
- **Complaint** — lodge a complaint with your local data protection authority. In the EU/EEA, that is your national supervisory authority; in the UK, the ICO.

To exercise any right, email **hashimaakbar@gmail.com** from the address linked to your account. We aim to respond within 30 days.

## 7. Members under 13 (children)

Academy Director is designed for academy **operators** (managers, co-managers, administrators, coaches) — not for children to use directly. Children are not the intended users.

However, as a coach or manager you may enter information about minors who attend your academy (names, ages, phone numbers, attendance). When you do this you act as the data controller for that information. You are responsible for:

- having a lawful basis under the laws that apply to you (e.g. GDPR, COPPA, etc.),
- obtaining any required consent from the child's parent or legal guardian,
- responding to data-subject requests from the children or their guardians.

If you become aware that you have entered the data of a child for whom you do not have appropriate consent, please delete the record from inside the app immediately.

We do not knowingly process the personal information of any individual under 13 except in the context described above where a verified adult academy operator records it.

## 8. International data transfers

If you access the app from outside the region where your Supabase project is hosted, your data is transferred to that hosting region. Where applicable, we rely on Standard Contractual Clauses (SCCs) approved by the European Commission for transfers out of the EU/UK, as offered by Supabase Inc.

## 9. Security

We use industry-standard practices:

- All network traffic is encrypted in transit (TLS 1.2+).
- Database data is encrypted at rest by our infrastructure provider.
- Authentication uses bcrypt-hashed passwords. The app never stores plaintext passwords.
- Row-Level Security (RLS) policies in the database ensure each user can only see their own academy's rows.
- The mobile app does not embed any secret keys; it uses a public "anon" key whose access is gated by the same RLS policies.

No system is 100% secure. If you believe your account has been compromised, email us immediately.

## 10. Photo library

If you choose to set an academy logo, the app uses the standard iOS photo picker. The picker runs out-of-process under iOS — the app only sees the image you explicitly select, never your full library. The selected image is uploaded to our backend so other staff and report PDFs can use it.

You can refuse access; the app continues to work without a logo.

## 11. Local notifications

The app schedules local notifications on your device to alert you about expiring memberships, low equipment stock, group memberships outside expected size, and confirmations after manually adding a member in Attendance. These notifications are produced by your device — they are not sent through any external push notification service. You can turn them off in iOS Settings → Notifications → Academy Director.

## 12. Reports and sharing

When you generate a PDF or CSV report from inside the app, the file is created and stored locally on your device. Nothing is uploaded by the app beyond what was already in the database. If you tap the iOS share sheet and choose where to send it (email, AirDrop, Files, etc.), the destination is handled by the app you choose to share it with, governed by their own privacy policy.

## 13. Account deletion

You can delete your account at any time in **Settings → Account → Delete My Account**. This:

1. Signs you out on the current device.
2. Permanently deletes your profile from our backend.
3. Removes any data linked solely to your account.

If you were the only manager of an academy, your academy and all its data are also deleted (this cannot be undone).

If you need help deleting an account but no longer have access to the app, email **hashimaakbar@gmail.com** from the address linked to your account and we will process the deletion within 30 days.

## 14. Changes to this policy

We will update this policy if the app's behaviour changes. Material changes will be reflected by updating the **Effective date** above and, where relevant, by an in-app notice the next time you launch the app. If a change reduces the rights or protections you previously had, we will give you advance notice and, where required by law, ask for your consent.

## 15. Contact

If you have any questions about this policy, your data, or wish to exercise any of the rights described above:

- Email: **hashimaakbar@gmail.com**

---

[Back to home](index.html) · [Support](support.html)
