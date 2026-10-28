# 02 — Entra ID Basics

Goal: understand the identity service behind Microsoft 365 sign-ins by creating a test user and a group in Microsoft Entra ID (formerly Azure Active Directory).

## Key ideas first

- A **tenant** is your organisation's identity directory. A free/student subscription comes with a default tenant.
- **Users** sign in with an address like `name@yourtenant.onmicrosoft.com`.
- **Groups** collect users so access can be assigned once instead of person by person — the same idea as Active Directory security groups on-prem.

## Steps

1. Open **Microsoft Entra ID** in the Azure portal (or go to entra.microsoft.com).
2. **Create a test user** — Users > New user. Use an obviously fictional test name, set a password, and do not use a real person's details.
3. **Create a group** — Groups > New group. Type: Security. Name it something like `Lab - IT Support`. Add the test user as a member.
4. **Review sign-in basics** — Open the test user and note the fields a service desk analyst uses daily: display name, user principal name, account enabled/disabled state, and the "Reset password" and "Revoke sessions" actions.
5. **Check it worked** — Sign out, then sign in to entra.microsoft.com as the test user in a private browser window. A successful sign-in proves the account and password work; group membership is visible under Groups in the portal (view-only for a standard user).

## How this connects to helpdesk work

Most "I cannot sign in" tickets are identity problems: a locked account, an expired password, or a user missing from a group that grants access. Practising user and group basics here is the cloud version of the Active Directory checks done at Tier 1.

## Cleanup note

Delete the test user and group when finished so the tenant stays tidy and no test accounts are left active.
