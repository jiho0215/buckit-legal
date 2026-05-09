---
layout: default
title: Privacy Policy
permalink: /privacy
---

# Buckitrek Privacy Policy

**Effective date:** 2026-05-09
**Version:** 1.0
**Contact:** ianjiholee@gmail.com

This Privacy Policy describes how Buckitrek ("we", "us", or "Buckitrek")
collects, uses, stores, shares, and protects the information of users
("you" or "user") of the Buckitrek mobile application and related
services. We are a personal-finance budgeting platform that aggregates
the user's own bank account data and helps the user organize spending
into budget categories ("buckets").

We aim to be a small, low-data app: we collect what we need to run the
budgeting features and nothing more.

## 1. Information We Collect

### 1.1 Information you provide

- **Identity**: when you sign in with Google, we receive your Google
  account display name and email address. We do not receive your
  Google password.
- **Account-deletion / support contact**: any email you send us at the
  contact address above.

### 1.2 Information from connected bank accounts (via Plaid)

When you connect a bank account through Plaid Link, we receive from
Plaid the data Plaid is authorized to share with us, which can include:

- Account ownership information (name on account, account type).
- Account balances and the last four digits of account numbers.
- Transaction history (amount, date, merchant, category as classified
  by Plaid).
- An access token issued by Plaid that lets us refresh the data above
  on your behalf.

We do **not** receive your bank login credentials. Those are entered
inside Plaid Link and never leave Plaid's hands.

### 1.3 Information collected automatically

- Application telemetry: request paths, durations, error stack
  traces, and device-type information, captured by Microsoft Azure
  Application Insights for the purpose of operating and improving the
  service.
- Audit trail: state-change events on your data records (creating,
  editing, deleting buckets, transactions, account links) so we can
  reconstruct what happened in case of an incident.

We do not use marketing analytics, advertising trackers, or
fingerprinting libraries.

## 2. How We Use Information

We use the information for the following purposes only:

- **Provide the service**: show you your account balances, transactions,
  budgets, and AI-suggested categorization.
- **Authenticate you**: issue a session token after Google sign-in.
- **Operate the platform**: detect outages, debug errors, prevent abuse.
- **Communicate with you**: respond to support requests, send security
  notifications when required.
- **Comply with legal obligations**: respond to lawful requests, comply
  with retention rules where applicable.

We do **not** sell your data to anyone. We do **not** share your
financial data or identifying information with advertisers.

## 3. AI Assistance (Anthropic)

Some features in the app use Anthropic's Claude language model to help
categorize transactions or summarize budgets. When we make a Claude
request on your behalf, we send only the minimum data needed for that
specific request (typically a transaction description or a small
summary of recent activity), and we do not include your name, email,
account numbers, or full transaction history. Anthropic's processing
of API requests is governed by Anthropic's own policies.

## 4. How We Share Information

We share information only with the following categories of recipients,
each of which is contractually bound to use the data only as needed to
provide its service to us:

- **Microsoft Azure** — hosting platform (App Service, SQL Database,
  Key Vault, Application Insights).
- **Plaid** — bank-data aggregation. Data flows both ways with Plaid:
  we send Plaid an item identifier, Plaid sends back the bank data
  you authorized.
- **Google** — identity provider only. Google sees that you signed in
  to Buckitrek; Google does not receive your Buckitrek data.
- **Anthropic** — AI assistance, scoped per Section 3 above.
- **GitHub** — source-code hosting and CI/CD. GitHub does not see your
  user data; it sees the code that processes it.

We may also disclose information when legally required (subpoena,
court order, or to investigate suspected fraud or violation of our
Terms).

## 5. How We Store and Protect Information

- All connections between your device, our backend, and our service
  providers run over TLS 1.2 or higher.
- Our database (Azure SQL) has Transparent Data Encryption enabled at
  rest. Plaid access tokens are additionally encrypted at the
  application layer with .NET Data Protection so a database backup
  alone does not expose unwrapped Plaid credentials.
- Authentication to our backend and to our cloud services uses Azure
  Active Directory and Managed Identity; secrets live in Azure Key
  Vault, never in source control.
- A full description of our security controls is maintained at
  `docs/security/INFORMATION_SECURITY_POLICY.md` in the Buckitrek
  repository and is updated whenever a control changes.

No system can guarantee absolute security. If we learn of a breach
that exposed your information, we will notify you by email within 72
hours of confirming the scope.

## 6. How Long We Keep Information

- Active accounts: we keep your data as long as your account is active,
  to provide historical budgeting analytics.
- Account deletion: when you delete your Buckitrek account (see
  Section 7), we revoke your Plaid items via Plaid's API and remove
  your personal information and bank-linked data from our production
  database within 30 days. Backups retained per Azure SQL's default
  policy will age out automatically.
- Operational telemetry (App Insights): retained for 90 days by
  default and then aged out.

## 7. Your Rights and Choices

Depending on your jurisdiction, you may have the following rights:

- **Access**: request a copy of the personal data we have about you.
- **Correction**: ask us to correct inaccurate information.
- **Deletion ("right to erasure")**: ask us to delete your account
  and personal data. We support this through:
  - the in-app account deletion flow when available, or
  - email request to the contact address above; we will process the
    request within 30 days.
- **Withdrawal of consent**: you may revoke your consent at any time;
  doing so disables the connected bank features and starts the
  deletion process described above.
- **Data portability**: where required by law, we will export your
  Buckitrek data in a portable format on request.

You can exercise any of these rights by emailing the contact address
above. We do not require an account to receive a deletion request.

## 8. Children's Privacy

Buckitrek is not directed to children under 13. We do not knowingly
collect personal data from children under 13. If we discover that we
have collected such information, we will delete it.

## 9. International Users

Buckitrek is operated from the United States. By using Buckitrek you
agree that your information may be transferred to and processed in
the United States. We rely on standard contractual clauses where
required for international transfers from regions with stricter data-
transfer rules (e.g. the EU/EEA).

## 10. Changes to This Policy

We will update this policy when our practices change. The current
version, effective date, and a change history are kept at
`docs/legal/PRIVACY_POLICY.md` in our repository. When the change is
material, we will notify active users by email and (where applicable)
require fresh acceptance in the app.

## 11. Contact

Questions or requests about this policy:

**Email:** ianjiholee@gmail.com

We will respond within 30 days.
