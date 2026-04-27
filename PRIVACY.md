# Privacy Policy

**Last updated:** April 19, 2026
**Effective date:** April 19, 2026

This Privacy Policy explains how Kinetic ("we", "us", "our") collects, uses, shares, and protects your information when you use the Kinetic iOS app (the "App"). Kinetic analyzes barbell exercise form using on-device 3D pose estimation and AI coaching.

If you do not agree with this Policy, please do not use the App.

---

## 1. Information We Collect

### 1.1 Information you provide
- **Account information.** When you create an account, we collect your email address (for email sign-in) or the authentication token provided by Apple Sign-In or Google Sign-In. If you sign in with Apple and use Hide My Email, we only receive the relay address Apple provides.
- **Training profile.** During onboarding you may provide your age, biological sex, height, lifting experience, and training goal. This is used to tailor coaching feedback.

### 1.2 Information collected automatically
- **Authentication metadata.** Firebase Authentication stores your user ID, provider, account creation date, and last-sign-in timestamp.
- **Subscription state.** If you subscribe, we receive subscription events (purchase, renewal, cancellation, expiration) from RevenueCat and store your tier, remaining analyses, and period start date.
- **Usage quota.** We track how many analyses you have remaining in the current billing period.

### 1.3 Information you create in the App
- **Videos.** Videos you record in-app or import from your photo library are processed **on your device**. They are **not uploaded to our servers**. They are stored in the App's private Application Support directory and are removed when you delete a session or your account.
- **Analysis sessions.** Pose data, rep counts, form-check results, and scores are stored locally on your device as JSON files in the App's private storage.
- **Coaching-request payload.** When you request AI coaching feedback for a workout, the App extracts **three still images** from the video (setup, bottom, lockout positions), plus a structured summary of the rep counts and form-check results and your training profile, and sends them to our Cloud Function, which forwards them to Anthropic's API (see §3.3).

### 1.4 Information we do not collect
- We do not collect precise location.
- We do not track you across apps or websites.
- We do not sell personal information.
- Kinetic does not place advertising in the App.

---

## 2. How We Use Your Information

We use the information described above to:
- Authenticate you and keep your account secure
- Sync your training profile and subscription state across sign-ins on new devices
- Enforce your analysis quota
- Generate personalized AI coaching feedback
- Provide customer support
- Comply with legal obligations

---

## 3. How We Share Your Information

We share information only with the service providers below, and only for the purposes described.

### 3.1 Firebase (Google LLC)
Firebase Authentication, Cloud Firestore, and Cloud Functions host your account, training profile, and usage record. See the [Firebase Privacy and Security](https://firebase.google.com/support/privacy) page for details.

### 3.2 RevenueCat, Inc.
RevenueCat manages our App Store subscription infrastructure. When you subscribe, your anonymized Apple subscription ID and product identifier are processed by RevenueCat, which writes your tier and quota into Firestore via an authenticated webhook. See the [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy).

### 3.3 Anthropic PBC
When you tap "Get AI Coaching," we send three still frames from your video and the heuristic summary described in §1.3 to our Firebase Cloud Function, which forwards the request to Anthropic's Claude API. The function adds a server-managed API key; your request does not include your name or email. Anthropic processes the request under their [Commercial Terms](https://www.anthropic.com/legal/commercial-terms) and does not train models on inputs sent through the API (see [Anthropic's Data Usage Policy](https://www.anthropic.com/legal/aup)).

### 3.4 Apple, Inc. and Google LLC (sign-in providers)
If you sign in with Apple or Google, the respective provider authenticates you and returns an ID token. We receive the information described in §1.1 from them.

### 3.5 Legal disclosures
We may disclose information if required by law, subpoena, or court order, or to protect the rights, safety, or property of Kinetic or its users.

---

## 4. Data Retention

- **Account data** (profile, usage record) is retained while your account exists.
- **Local videos and session data** are stored only on your device until you delete them in the History tab or delete your account.
- **Coaching request payloads** are not persisted by Kinetic after the request completes. Anthropic's retention for API requests is governed by their Commercial Terms (typically 30 days for abuse monitoring, then deletion).
- **Subscription events** are retained by RevenueCat per their own policy.

---

## 5. Your Rights and Choices

### 5.1 Account deletion
You can delete your account from **Profile → Delete Account** in the App. This permanently removes:
- Your Firebase Authentication record
- Your training profile and usage quota document
- Session JSON and video files stored locally on the current device

If you have an active Apple subscription, **you must cancel it separately** in iOS Settings → Apple ID → Subscriptions. Deleting your Kinetic account does not instruct Apple to stop billing you.

### 5.2 Access, correction, portability
You can view and edit your training profile in **Profile → Edit Profile**. To request a machine-readable export of your data or to correct information, email us at the address in §10.

### 5.3 California (CCPA), EU/UK (GDPR), and other jurisdictions
Residents of California and jurisdictions subject to GDPR/UK GDPR have specific rights, including access, deletion, correction, portability, restriction, and objection to processing. To exercise any of these rights, use the in-app deletion flow or contact us. We do not sell personal information, so no opt-out of sale is required.

Our legal basis for processing is (a) performance of a contract (to provide the App and coaching features) and (b) our legitimate interest in securing and improving the service. You may withdraw consent at any time by deleting your account.

### 5.4 Children
The App is not directed to children under 13 (or under 16 in the EEA). We do not knowingly collect information from children. If you believe a child has provided us information, contact us and we will delete it.

---

## 6. Security

We use industry-standard practices including:
- TLS in transit for all network requests
- Firebase security rules that restrict every user to their own documents
- A Firebase Cloud Function with a server-side Anthropic API key stored in Firebase Secret Manager — the key never touches your device

No system is perfectly secure. If you believe your account has been compromised, contact us immediately.

---

## 7. International Transfers

Firebase, RevenueCat, and Anthropic primarily process data in the United States. If you are outside the US, your data will be transferred to and processed in the US or other jurisdictions where these providers operate. We rely on the contractual commitments of our processors to protect transferred data.

---

## 8. Camera and Photo Library Permissions

- **Camera:** Used only when you record a video in-app. Live preview and recording occur on-device and are not streamed anywhere.
- **Photo Library:** Used only when you pick a video to import. We access a single video you select via the iOS photo picker; we do not browse or index your library.

You can revoke either permission at any time in iOS Settings → Kinetic.

---

## 9. Changes to This Policy

We may update this Policy from time to time. The "Last updated" date at the top reflects the latest revision. Material changes will be announced in the App or by email. Continued use of the App after a change indicates acceptance of the revised Policy.

---

## 10. Contact

Questions, requests, or privacy concerns:

**Email:** support@kineticapp.co
**Mail:** Kinetic — Privacy, [your mailing address here]

---

*Kinetic is an independent app and is not affiliated with Anthropic, Google, Apple, or RevenueCat beyond the service-provider relationships described above.*
