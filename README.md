# TrailWatcher Secure Edition (v4.6.1)

## Overview

TrailWatcher Secure Edition is a Salesforce Setup Audit Trail viewer designed for Salesforce Administrators, Developers, Security Teams, and Compliance Auditors.

This version includes additional security controls to reduce unauthorized access from shared browser profiles and cached audit data.

---

# What's New in Secure Edition

### Security Enhancements

✅ PIN-protected access

✅ Auto-lock after inactivity

✅ Manual lock capability

✅ Cached audit data cleared on lock

✅ Local PIN reset option

✅ Reduced exposure of stored audit records

---

# Installation

## Step 1 – Extract the Package

Extract:

```text
trailwatcher-v4.6.1-secure-lock.zip
```

to a local folder.

Example:

```text
C:\Extensions\TrailWatcher
```

or

```text
~/Downloads/TrailWatcher
```

---

## Step 2 – Open Chrome Extensions

Open:

```text
chrome://extensions
```

---

## Step 3 – Enable Developer Mode

Enable:

```text
Developer Mode
```

located in the upper-right corner.

---

## Step 4 – Load the Extension

Click:

```text
Load unpacked
```

Select the extracted TrailWatcher folder.

---

## Step 5 – Verify Installation

Confirm the extension appears in the Chrome extensions list.

Optionally pin the extension to the toolbar.

---

# First-Time Setup

When opening TrailWatcher for the first time:

1. Create a local PIN.
2. Store the PIN securely.
3. Use the PIN whenever the extension is locked.

The PIN is stored locally within your browser profile and is never sent to Salesforce.

---

# Requirements

The user must:

* Be logged into Salesforce
* Have API access enabled
* Have Setup Audit Trail visibility
* Use Chrome or Chromium-based browsers

---

# How It Works

TrailWatcher:

1. Detects the active Salesforce organization.
2. Reads the authenticated Salesforce session.
3. Uses Salesforce APIs to retrieve Setup Audit Trail records.
4. Displays audit information within the extension.
5. Stores temporary audit data locally for performance.

---

# Security Features

## PIN Protection

A local PIN protects access to:

* Cached audit records
* Extension functionality
* Salesforce audit history

The extension remains locked until the correct PIN is entered.

---

## Auto Lock

The extension automatically locks after:

```text
10 minutes of inactivity
```

When auto-lock occurs:

* Cached audit data is cleared
* Access is restricted
* Re-authentication is required

---

## Manual Lock

Users can lock the extension at any time.

Recommended when:

* Leaving your workstation
* Attending meetings
* Working in shared environments

---

## Reset Lock

If required:

```text
Reset Local Lock
```

will:

* Remove the stored PIN
* Clear cached audit data
* Return the extension to first-time setup mode

---

# Permissions Used

| Permission                  | Purpose                            |
| --------------------------- | ---------------------------------- |
| cookies                     | Access active Salesforce session   |
| storage                     | Store settings and temporary cache |
| tabs                        | Detect Salesforce tabs             |
| scripting                   | Interact with Salesforce pages     |
| Salesforce host permissions | Access Salesforce APIs             |

These permissions are required for core functionality.

---

# Important Security Notes

## Salesforce Session Usage

TrailWatcher uses the currently authenticated Salesforce session.

This means:

```text
Extension access = Logged-in user's Salesforce permissions
```

The extension cannot access data beyond the permissions granted to the authenticated Salesforce user.

---

## Shared Computers

Do not use TrailWatcher on:

* Public computers
* Shared kiosks
* Untrusted workstations

If a shared device must be used:

* Lock the extension
* Log out of Salesforce
* Close Chrome after use

---

## Browser Security

Recommended:

✅ Device encryption

✅ OS password protection

✅ Screen lock

✅ Corporate endpoint security

✅ Separate browser profiles for admin access

---

# Best Practices

### Use Dedicated Admin Profiles

Maintain a dedicated Chrome profile for Salesforce administration.

Example:

```text
Chrome Profile: Salesforce Admin
```

instead of:

```text
Chrome Profile: Personal Use
```

---

### Log Out When Finished

After completing administrative work:

1. Lock TrailWatcher
2. Log out of Salesforce
3. Close browser tabs

---

### Review New Versions

Before installing updates:

* Review release notes
* Validate source code
* Test in a Salesforce sandbox
* Obtain internal approval if required

---

# Troubleshooting

## PIN Forgotten

Use:

```text
Reset Local Lock
```

Then create a new PIN.

Note:

```text
Cached audit data will be removed.
```

---

## No Audit Data Appears

Verify:

* Salesforce login is active
* User has Setup Audit Trail access
* API access is enabled
* Salesforce tab is open

---

## Extension Remains Locked

Try:

1. Enter correct PIN
2. Reset local lock
3. Reload extension
4. Restart Chrome

---

# Privacy Statement

TrailWatcher Secure Edition retrieves audit trail information directly from Salesforce using the authenticated user's session.

No Salesforce credentials are stored by the extension.

The extension is intended for internal Salesforce administration and security auditing purposes.

---

# Recommended Deployment

Before organization-wide deployment:

* Perform code review
* Conduct security assessment
* Validate in Sandbox environments
* Maintain version-controlled releases
* Restrict installation to approved administrators

---

**Version:** 4.6.1 Secure Edition
**Platform:** Chrome / Chromium Browsers
**Supported Orgs:** Salesforce Production, Sandbox, Developer Editions
**Security Features:** PIN Lock, Auto-Lock, Cache Clearing, Manual Lock 🔐🚀
