# Privacy Policy for AI Bluesky Scheduler

**Last updated:** June 17, 2025

## Overview

AI Bluesky Scheduler is a browser extension that helps you schedule and automatically post content to Bluesky (formerly X) using AI-assisted drafting. We take your privacy seriously and do **not** collect, store, or transmit any personal data to our own servers. This policy explains how your data is used, stored, and protected.

---

## Data You Provide

* **Bluesky Credentials** (identifier and app password)
* **OpenAI API Key**

You enter these values directly into the extension’s settings. They are used only to authenticate with external services (Bluesky, OpenAI) and are never shared or transmitted elsewhere.

---

## How Data Is Stored

### Secure Local Encryption

When you choose **Encrypted** mode, your credentials and API key are encrypted *in your browser* before being saved to Chrome’s local storage:

1. A key is derived from your machine fingerprint (browser user agent, language, screen size, timezone offset) using PBKDF2.
2. Data is encrypted with AES-GCM via SubtleCrypto and stored as ciphertext plus IV.
3. Decryption uses the same machine-derived key.

In **Session** mode, your key is held only in memory and is never persisted.

### No Remote Storage

All data stays on your device. We do **not** send your credentials or API key to any remote server under any circumstance.

---

## Use of External Services

* **Bluesky (bsky.social)**

  * We make authenticated API calls to post and retrieve your data. Bluesky receives only what you submit (post text, credentials for authentication).

* **OpenAI**

  * When AI-assisted drafting is enabled, your text prompt is sent to OpenAI’s API (`api.openai.com`). OpenAI may use your prompt and generated output according to their own [privacy policy](https://openai.com/policies/privacy-policy).
  * We do not log, store, or forward any responses beyond what’s necessary to display in the UI.

---

## No Analytics or Tracking

AI Bluesky Scheduler does **not** use any analytics, telemetry, or tracking services. We do not collect usage statistics, crash reports, or behavioral data.

---

## Permissions

* \`\`: to save your settings and encrypted credentials locally.
* \`\`: to schedule future posts.
* \`\`: to open the full-view editor in a new tab.
* \`\`: to inject UI elements or content scripts if needed.
* **Host permissions** for `https://api.bsky.app/*` and `https://bsky.social/*` to communicate with Bluesky’s APIs.

---

## Support and Contact

If you have any questions or concerns about this policy, please open an issue on our GitHub repository:

```
https://github.com/you/ai-bluesky-scheduler/issues
```

Thank you for using AI Bluesky Scheduler! Your privacy is our top priority.

---

## License

© 2025 AI Bluesky Scheduler. All rights reserved.
