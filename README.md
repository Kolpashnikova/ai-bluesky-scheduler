# AI Bluesky Scheduler

**Last updated:** June 18, 2025

## Overview

Bluesky Post Scheduler is a browser extension that helps you schedule and automatically post content to Bluesky using AI-assisted content generation. We take your privacy seriously and do **not** collect, store, or transmit any personal data to our own servers. This policy explains how your data is used, stored, and protected.

---

## Data You Provide

- **Bluesky Credentials** (identifier and app password)
- **OpenAI API Key** (optional, for AI features)
- **Post Content** (text you want to schedule)
- **Scheduling Preferences** (dates, times, style settings)

You enter these values directly into the extension's interface. They are used only to authenticate with external services (Bluesky, OpenAI) and are never shared or transmitted elsewhere.

---

## How Data Is Stored

### Secure Local Storage Options

**Encrypted Mode (Default):**
When you choose **Encrypted** mode, your credentials and API key are encrypted *in your browser* before being saved to Chrome's local storage:
1. A key is derived from your machine fingerprint (browser user agent, language, screen size, timezone offset) using PBKDF2
2. Data is encrypted with AES-GCM via SubtleCrypto and stored as ciphertext plus IV
3. Decryption uses the same machine-derived key
4. Data persists until you manually clear it or uninstall the extension

**Session-Only Mode:**
In **Session** mode, your API key is stored only in Chrome's session storage and automatically deleted when you close your browser. Your Bluesky credentials remain encrypted in local storage for convenience.

### Scheduled Posts Storage
Your scheduled posts (content, dates, times) are stored locally in Chrome's storage and never transmitted to external servers except when being posted to Bluesky at the scheduled time.

### No Remote Storage
All data stays on your device. We do **not** send your credentials, API keys, or personal data to any remote server under any circumstance.

---

## Use of External Services

### Bluesky Services
**bsky.social & api.bsky.app**
- **bsky.social**: Used for Bluesky authentication and account verification
- **api.bsky.app**: Used for posting scheduled content and retrieving account data
- We make authenticated API calls only when you schedule posts or verify your account
- Bluesky receives only what you explicitly schedule to post (post text, media) and your authentication credentials
- Communication occurs only at scheduled posting times or when you manually authenticate
- Your data is subject to Bluesky's [Privacy Policy](https://bsky.social/about/privacy) and [Terms of Service](https://bsky.social/about/terms)

### OpenAI Services  
**api.openai.com**
- When AI-assisted content generation is enabled and you have provided an API key, your text prompts are sent to OpenAI's API
- OpenAI may use your prompts and generated content according to their [Privacy Policy](https://openai.com/policies/privacy-policy)
- We do not log, store, or forward any AI responses beyond displaying them in the extension interface
- AI features are entirely optional and can be disabled
- You are responsible for all OpenAI API usage costs

### Data Transmission Summary
- **To Bluesky**: Authentication credentials, scheduled post content
- **To OpenAI**: Text prompts for content generation (optional)
- **To Our Servers**: Nothing - we have no backend servers

---

## Chrome Extension Permissions

AI Bluesky Scheduler requires the following permissions to function:

- **storage**: Store your scheduling data, preferences, and encrypted credentials locally in your browser
- **alarms**: Schedule and trigger posts at specified dates and times using Chrome's alarm system  
- **tabs**: Open the full-view calendar interface in a separate browser tab
- **Host permissions for**:
  - `https://bsky.social/*` - For Bluesky authentication and account access
  - `https://api.bsky.app/*` - For Bluesky data operations and posting
  - `https://api.openai.com/*` - For optional AI content generation (only when API key provided)

These permissions are used solely for the extension's core functionality. No data is collected or transmitted beyond the services explicitly mentioned above.

---

## No Analytics or Tracking

Bluesky Post Scheduler does **not** use any analytics, telemetry, or tracking services. We do not:
- Collect usage statistics
- Monitor user behavior
- Send crash reports
- Use cookies or tracking pixels
- Collect device information beyond what's needed for encryption

---

## Data Security

- All sensitive data is encrypted using industry-standard AES-GCM encryption
- Encryption keys are derived from your device's unique characteristics and never transmitted
- No passwords or API keys are stored in plain text
- All external communications use HTTPS encryption
- The extension operates entirely client-side with no backend servers

---

## Data Retention and Deletion

- **Scheduled Posts**: Stored until you delete them or they are successfully posted
- **Settings**: Persist until you change them or uninstall the extension
- **Credentials**: Stored until you manually clear them or uninstall the extension
- **Session Data**: Automatically cleared when browser is closed (in session-only mode)

To delete all data:
1. Use the "Clear API Key" button in settings
2. Disconnect from Bluesky in the authentication section
3. Uninstall the extension to remove all stored data

---

## Single-Purpose Declaration

Bluesky Post Scheduler is designed **exclusively** to:
- Schedule posts for future publishing on Bluesky
- Generate content using AI (when enabled)
- Manage your scheduled post calendar

It does not perform any other data collection, analysis, or transmission beyond these core functions.

---

## Changes to This Policy

We may update this privacy policy to reflect changes in our practices or applicable law. Any changes will be posted with an updated "Last updated" date. Continued use of the extension after changes indicates acceptance of the updated policy.

---

## Contact Information

If you have questions or concerns about this privacy policy or our data practices, please contact us:

- **GitHub Issues**: [https://github.com/Kolpashnikova/ai-bluesky-scheduler/issues](https://github.com/Kolpashnikova/ai-bluesky-scheduler/issues)

---

## Compliance

This extension and privacy policy comply with:
- Chrome Web Store Developer Program Policies
- General Data Protection Regulation (GDPR)
- California Consumer Privacy Act (CCPA)
- Chrome Extension Manifest V3 requirements

---

**© 2025 AI Bluesky Scheduler. All rights reserved.**