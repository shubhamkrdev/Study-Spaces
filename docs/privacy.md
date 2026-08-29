# Privacy Policy — Study Spaces

!!! warning "Draft — not yet in force"

    This policy is published for review and is not the operative version. Values shown as
    `[PLACEHOLDER — …]` are not yet filled in.

**Effective date:** `[PLACEHOLDER — date of publication]`

---

## 1. Who we are

Study Spaces is an Android application for owners and managers of study halls, reading rooms and
coworking spaces. It is published by `[PLACEHOLDER — registered legal entity name]`, `[PLACEHOLDER —
registered address]` ("we", "us").

This policy explains what personal data the app handles, why, and what you can do about it. It
applies to the Study Spaces Android app (package `com.spaces.study`) and its backend services.

## 2. Two different kinds of data — please read this first

The app handles two categories of personal data, and our role differs for each. This distinction
determines who you contact about what.

**(a) Your account.** If you sign in to Study Spaces — as a space owner or as a staff member — we
hold your account and identity data. For this data we are the **Data Fiduciary**. Contact us
directly (§17).

**(b) Your students' records.** The student names, phone numbers, fees and attendance you enter into
the app belong to the space that collects them. For that data the **space owner is the Data
Fiduciary** and we act only as a **Data Processor**, on the owner's instructions. We do not decide
what is collected, we do not use it for our own purposes, and we do not combine it across spaces.

If you are a student whose details are held in Study Spaces, see §15 — your request goes to the
study space, not to us.

## 3. What we collect

### 3.1 Account holders (owners and staff)

| Data | Source | Why |
|---|---|---|
| Firebase user ID (`uid`) | Created at sign-up | Identifies you; every access-control check in the system depends on it |
| Email address | You, or your Google account | Sign-in, password reset, email verification |
| Name, phone number, address | Entered by you in Settings | Displayed to your colleagues; used on receipts |
| Space membership and role | Set by the space owner | Determines what you can see and do |

We support **email-and-password sign-in** and **Google sign-in**. Authentication is handled by
Firebase Authentication; we never see or store your password, and we never see your Google account
password.

### 3.2 Student records (processed for the space owner)

Entered by the owner or staff, not by the student:

- **Required:** name, phone number
- **Optional:** address, guardian name and phone, date of birth, ID proof type and number, blood
  group, school or organisation, programme of study, notes, tags
- **Fee records:** amount, payment mode, date, period covered, receipt number, who recorded it,
  cancellation reason
- **Seat and shift allocation, enrolment and exit dates, status**

Two honest notes about the optional fields:

- **Date of birth drives the under-18 check.** Where it makes a member a minor, the form requires
  guardian details and guardian consent before it will save. It is used for nothing else.
- **ID proof number is stored for a purpose that does not yet exist** — possible future identity
  verification. It is optional and may be left blank.
- **Who can see an ID proof number.** Staff without the owner's explicit grant cannot see it at all.
  Staff with the grant see only the last four digits on the member's record — but the **edit form
  shows the full number**, because correcting it requires reading it. Treat the grant as access to
  the whole number.

### 3.3 Device and technical data

- An app-generated device identifier, a device label you choose, terminal number, app version, and
  the time the device last synced. This exists so a receipt can be traced to the terminal that
  issued it.
- The device's reported clock time at sync, so we can detect a device whose clock is wrong — the
  device clock decides which month a receipt is filed under.

## 4. What we deliberately do not collect

These are commitments, not oversights:

- **No location data.** No GPS, no coarse location, no location permission is requested.
- **No advertising identifier, IMEI, MAC address or other hardware identifier.**
- **No analytics or crash-reporting SDK.** The app ships with no analytics, telemetry, or crash
  reporting library of any kind.
- **No advertising.** We show no ads and share no data with advertisers or data brokers.
- **No staff location or login history.** We record which staff member last used a terminal, so a
  receipt traces to a person. We do not keep a history of where an employee was and when.
- **No student photographs.** The data model has a photo field, but the app provides no way to
  capture or attach an image, and no image file is uploaded to our servers.
- **No contacts, call log, SMS, microphone or camera access.**
- **No processing of your students' fee payments.** Money changes hands directly between the space
  and the student. The app is a record-keeping tool, not a payment intermediary.

## 5. Permissions the app requests

| Permission | Why |
|---|---|
| Internet | Sync with the cloud |
| Notifications | Local reminders about dues and expiring seats |
| Phone (place a call) | Lets you tap a stored number to dial it. We do not access your call log, and we do not record calls |

The app can also **compose a fee reminder addressed to a student and hand it to WhatsApp or your
share sheet**. This uses Android's standard sharing mechanism: no contacts permission is requested,
we do not read your WhatsApp, and nothing is sent until you press send inside that app.

## 6. How we use data, and on what basis

We process account data to provide the service you signed up for: to authenticate you, to enforce
who can see what, to sync your data across devices, to apply your subscription plan's limits, and to
respond when you contact support. Under India's Digital Personal Data Protection Act, 2023, this is
processing for the specified purpose for which you gave consent at sign-up.

Student records are processed **only on the space owner's instructions**, to provide the service to
that owner.

**We do not build cross-space analytics on student or payment data.** No benchmarking, no
platform-wide revenue insight, no churn analysis across customers. This is an architectural
commitment, not just a policy statement.

**We do not sell personal data**, and we do not use it to train machine-learning models.

## 7. Who else handles the data

| Party | Role | Where |
|---|---|---|
| Google — Firebase Authentication | Sign-in and identity | Google infrastructure |
| Google — Cloud Firestore | Primary data store | `asia-south1` (Mumbai, India) |
| Google — Cloud Functions | Server-side processing | `asia-south1` (Mumbai, India) |

That is the complete list. We disclose personal data to no one else, except where we are legally
required to, or where it is necessary to establish or defend a legal claim.

A small number of our personnel can access production data using an administrative credential, for
support and incident response. Such access is occasional and only for a stated reason.

**Google Play Billing** processes subscription payments for the app itself. Google is the merchant
of record: we never see or store your card, UPI ID or bank details. We receive only a purchase token
and an order id, which tell us which plan to activate. Your students' fees are not processed by
anyone — see §4.

## 8. Where data is stored

**Storage and processing are in India, end to end.** The database and the server-side functions both
run in Google Cloud's `asia-south1` (Mumbai) region.

The app also keeps a **copy of your space's data on your device**, so it works without a network
connection. Two things you should know about that copy:

- It is stored in the app's private storage and is **not encrypted beyond the protection Android
  gives app data**. Anyone with your unlocked device, or with root access to it, can read it. Use a
  screen lock.
- It is **erased when a different account signs in** on that device, so a shared device does not
  leak one person's students to the next.

## 9. How long we keep data

| Data | Retention |
|---|---|
| Your account and profile | While your account is active — see §11 |
| Student personal details | Personal details are cleared **12 months** after the student is archived |
| Fee and payment records | **8 years**, to meet tax and company-law record-keeping obligations |
| Device records | While the device is registered to a space |

Fee records are kept for the full 8 years even after a student's personal details are cleared. At
that point the records no longer identify anyone — they remain as an accounting trail.

Our database keeps a **7-day point-in-time recovery window**. Deleted or changed data may exist in
that recovery window for up to 7 days before it is gone.

## 10. Your rights

Under the DPDP Act you may:

- **Access** a summary of the personal data we hold about you and how it is processed
- **Correct** data that is inaccurate, and complete data that is incomplete
- **Erase** your personal data, subject to the legal retention in §9
- **Nominate** another person to exercise these rights if you die or become incapacitated
- **Complain** to our Grievance Officer (§17), and then to the Data Protection Board of India

To exercise any of these, contact us at [shubhamkr.devapps@gmail.com](mailto:shubhamkr.devapps@gmail.com). We respond within
**30 days**.

**For a study space's students:** these requests go to the space that holds your records. See §15.

## 11. Deleting your account and your data

Full instructions, including what is destroyed and what survives, are on
[Delete your account](delete-account.md).

You can request deletion of your account and its data at any time:

- **On the web:** <https://shubhamkrdev.github.io/Study-Spaces/delete-account/>, without installing or opening
  the app
- **By email:** [shubhamkr.devapps@gmail.com](mailto:shubhamkr.devapps@gmail.com)

**What is deleted:** your account and sign-in identity; your profile (name, email, phone, address);
**every space you own and all of its records** — members, payments, receipts, shifts, expenses,
financial totals and device registrations; and your access to spaces owned by other people.

**If you are a space owner, deleting your account destroys your students' records too.** You are the
Data Fiduciary for that data, so deleting your account is your instruction to us to delete it. The
app tells you how many records will go, and asks you to type `DELETE`, before doing anything.

**Export first.** Reports offers CSV export. Once deletion runs we cannot recover anything — including
fee history you may need for your own tax records. The 8-year retention in §9 applies to records we
hold; it does not survive your instruction to delete them.

**Spaces owned by someone else are untouched.** You are removed from them; their records belong to
that owner.

**Deleting student data without deleting your account:** an owner or authorised staff member can
erase an individual student from within the app. The erase action clears the student's name, phone,
email, address, guardian details, date of birth, blood group, ID proof, seat, organisation and
notes, and archives the record. It is **irreversible**, and the fee history remains for the
retention period in §9.

**Timing.** Deletion completes within **30 days**. Copies may persist in the
7-day recovery window described in §8 and in routine backups for a short period after that.

## 12. Security

- All traffic between the app and our services uses TLS.
- Access control is enforced on the server, in database security rules and in server-side functions
   — not in the app, which can be modified by anyone holding the device.
- Financial visibility and administrative rights are per-space permissions granted by the owner.

We do not claim the on-device copy is encrypted beyond Android's own app-data protection — see §8.
No system is perfectly secure; we do not promise otherwise.

## 13. Children's data

Study Spaces is a business tool. It is **not directed at children**, and account holders must be 18
or older.

A study space may enrol students under 18, and the app provides guardian name and phone fields for
that. Where a student is a child, the **space owner** is responsible for obtaining verifiable
consent from a parent or legal guardian before entering the child's details, as the DPDP Act
requires. We do not knowingly process a child's data other than on an owner's instruction.

## 14. Messages and marketing

**We never message your students, and our servers send nothing to anyone.** Dues and expiry
reminders are generated locally on your own device and shown only to you. There are no
server-initiated push notifications.

**You can send a student a fee reminder yourself.** The app composes the message text on your device
and hands it to WhatsApp or your share sheet, pre-addressed to the number you stored. It is sent from
your own account, by you, only when you press send — we are not in that path and keep no record of
it. Because the message comes from you, obtaining any consent your students need for that contact is
your responsibility as their Data Fiduciary.

**We send no marketing** to you or to your students.

## 15. If you are a student at a study space

Your details were entered into Study Spaces by the space you attend. That space decides what to
collect and how long to keep it — it is the Data Fiduciary; we only store and process the data for
them.

**Please direct requests to access, correct or erase your data to the study space itself.** If they
do not respond, you may contact us at [shubhamkr.devapps@gmail.com](mailto:shubhamkr.devapps@gmail.com) and we will assist the
space in responding, but we cannot act on their data without their instruction.

## 16. Changes to this policy

We will update this policy when what the app does changes. Material changes will be notified in the
app before they take effect. The "last updated" date at the top always reflects the current version.

## 17. Contact and grievances

**Grievance contact** (DPDP Act, 2023):

- Email: [shubhamkr.devapps@gmail.com](mailto:shubhamkr.devapps@gmail.com)
- Address: `[PLACEHOLDER — registered address]`
- Responsible person: `[PLACEHOLDER — grievance contact, name or role]`

The Act requires a *Significant* Data Fiduciary to appoint and publish a named Data Protection
Officer. An ordinary Data Fiduciary must publish the business contact of a person able to answer
questions on its behalf, which a monitored role address satisfies. We are not a Significant Data
Fiduciary. Note also that for **student** data the space owner is the Data Fiduciary, so that
grievance duty is theirs — ours covers account holders only.

**General privacy queries:** [shubhamkr.devapps@gmail.com](mailto:shubhamkr.devapps@gmail.com)

We acknowledge grievances within **7 days** and aim to resolve them within
**30 days**. If you are not satisfied, you may complain to the **Data Protection
Board of India**.
