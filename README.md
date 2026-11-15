# Employee of the Quarter: Online Voting Demo

An interactive demo of a secure online voting system for **Ignite Media Group (IMG)**, so every staff member can vote from anywhere, once.

Powered by: **ABK Technologies** - [www.abkarikari23.tech](https://www.abkarikari23.tech)

> **This is a demo only.** It uses sample data, nothing is sent to staff, and no votes are stored on a server. Nominee photos and names come from the last results graphic. Achievements, vote counts and staff numbers are sample text.

---

## The problem it solves

- Staff who are not in the office at voting time can't vote.
- Our earlier online attempt allowed over-voting.

## What the system does

- **Vote from anywhere:** works on any phone or computer with a browser.
- **One person, one vote:** each staff member is identified from the HR staff list, and a second attempt is blocked.
- **Registered staff only:** login uses the email or phone number HR has on file.
- **One-time code (OTP):** sent by email or SMS, valid for 10 minutes, usable once.
- **Anonymous ballot:** the system records *who has voted*, never *who they voted for*.
- **Merit-based voting:** each nominee has a profile with the quarter's achievements.
- **Nominees can vote,** including for themselves.
- **HR admin view:** turnout, list of staff who have not voted, results locked until voting closes, export to PDF and Excel.

## Try the demo

1. Open the demo link.
2. On the login screen, enter one of the demo contacts:

   | Demo user | Email | Phone |
   |---|---|---|
   | Demo user 1 | `ama@example.com` | `0241234567` |
   | Demo user 2 | `kwame@example.com` | `0207654321` |

   Any other contact is rejected, like in the live system.
3. Choose to receive your code by **email** or **SMS** (a sample message is shown).
4. Enter the demo code: **`123456`**
5. Read the nominees' achievements, select one, review, and submit.
6. Log in again with the same contact. You will see **"You have already voted"**, which is the over-voting protection.
7. Switch to **HR admin view** (top right) to see turnout and close voting to reveal results.
8. Use **Reset demo** in the admin view to start over.

The demo remembers a vote only in your own browser. The real system enforces it in the database for everyone.

## Files in this repo

```
index.html                 the demo page
ignite-logo.jpeg           Ignite Media Group logo
abk-logo.jpeg              ABK Technologies logo
nominee photos (*.jpg)     nominee photos (7 images, in this folder)
README.md                  this file
```

Keep all files in the same folder structure or the logos and photos won't load.

## Hosting on GitHub Pages

The demo is published at [https://abkarikari23.github.io/IMG_Voting_System-Demo/](https://abkarikari23.github.io/IMG_Voting_System-Demo/) from the root of the `master` branch.

Note: GitHub Pages sites are public. Get management's approval before sharing a link that shows staff photos and names.

## Planned live system (after approval)

| Area | Plan |
|---|---|
| Address | `vote.abkarikari23.tech` (subdomain, separate from the main website) |
| Build | Laravel (PHP) with MySQL on the existing Hostinger Business plan |
| Login | Staff list uploaded by HR (name, department, email, phone), plus email or SMS OTP |
| One vote rule | Database constraint: one vote per staff member per quarter, written together with the anonymous ballot in a single transaction |
| Security | HTTPS, hashed codes, limits on code requests and wrong attempts, audit log, no admin access to edit votes |
| Admin | Nominee and achievement approval, turnout tracking, locked results, exports |
| Branding | IMG logo as the header, "Powered by ABK Technologies" on every page and in emails and exports |

Not included for now: USSD voting.

## Data and privacy

- Only the data needed for voting is collected: name, department, email, phone and staff ID if available.
- No passwords, ID numbers, addresses or other personal details are needed.
- The data is used only for the vote, and is archived or deleted at an agreed time after results are confirmed.

## Contact

**ABK Technologies**
[www.abkarikari23.tech](https://www.abkarikari23.tech)
