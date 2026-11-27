# Privacy Policy

**Effective Date:** March 23, 2026
**Last Updated:** November 27, 2026

Whisper Me ("we," "us," "our") operates the Whisper Me mobile application (the "App"). This Privacy Policy describes what personal data we collect, how we use it, who we share it with, how long we keep it, and your rights under applicable laws including the EU General Data Protection Regulation (GDPR), Korea's Personal Information Protection Act (PIPA), and the California Consumer Privacy Act (CCPA).

By using the App, you agree to the collection and use of information as described in this policy. If you do not agree, do not use the App.

---

## 1. Data Controller

**JoCoding, Inc.**
**16 Wausan-ro 29-gil, Mapo-gu, Seoul, South Korea**
**highball@jocoding.net**

For Korea PIPA purposes, the personal information protection officer is: **highball-jo (highball@jocoding.net)**

---

## 2. Data We Collect

### 2.1 Account Data

We collect the following when you create an account:

| Data Point | Source | Required |
|------------|--------|----------|
| Email address | You provide it (email sign-up) or it is shared by Google/Apple | Yes |
| Password | You provide it (email sign-up only); stored as a cryptographic hash, never in plaintext | Yes (email sign-up) |
| Display name | Shared by Google or Apple during OAuth sign-in | No |
| Profile photo URL | Shared by Google during OAuth sign-in | No |
| Google account ID | Google OAuth | Only if using Google sign-in |
| Apple user ID | Apple Sign-In | Only if using Apple sign-in |

### 2.2 Profile Data

| Data Point | Source | Purpose |
|------------|--------|---------|
| Preferred language | You select or we detect from your device locale | Display the App in your language |
| Theme preference | You select (system, light, or dark) | Display settings |
| Timezone (IANA format, e.g., "Asia/Seoul") | Auto-detected from your device on each app launch | Enable your AI companion to reference time naturally when you enable "Your Real Time" mode |

**Timezone and location:** We collect your device timezone, not your GPS location. However, a timezone can indicate your approximate geographic region.

### 2.3 Companion Configuration Data

When you create an AI companion, we store:

- Companion name (you choose)
- Personality type (caring, playful, intellectual, or adventurous)
- Gender (male, female, or nonbinary)
- Voice selection (a voice ID referencing a pre-built voice)
- Language (one of 24 supported languages)
- Time awareness mode (timeless or real-time)
- Response length preference (short, medium, or long)
- Custom instructions (up to 500 characters of free-text guidance you write for the companion)
- Companion avatar image (optional)

### 2.4 Conversation and Call Data

This is the most sensitive category of data we collect.

**During every voice call or text conversation, we collect and store:**

| Data Point | Storage Location | Retention |
|------------|-----------------|-----------|
| Full conversation transcript (every message you send and every response the companion generates) | Our database (Supabase) | Until you delete your account |
| Call metadata (duration, start/end time, call status) | Our database | Until you delete your account |

**We do NOT record or store audio.** Voice audio is streamed in real time through our processing pipeline and is never written to disk or saved to any storage system. Only the text transcript is retained.

### 2.5 AI-Extracted Memory Data

After each call or text conversation, our server processes the conversation to extract and store:

| Data Type | Description | Example | Retention |
|-----------|-------------|---------|-----------|
| **User profile facts** | Structured facts about you extracted by AI | "Job: software engineer," "Pet: dog named Max," "Favorite food: ramen" | Until you delete your account |
| **Call summaries** | 2-3 sentence AI-generated summary of each call | "Discussed weekend plans and work stress. Mood was upbeat." | Until you delete your account |
| **Emotional tone** | AI-assessed emotional tone of each call | "happy," "anxious," "playful" | Until you delete your account |
| **Topics discussed** | List of topics from each call | ["work", "family", "travel plans"] | Until you delete your account |
| **Unresolved threads** | Topics left unfinished in a call | ["birthday gift ideas"] | Until you delete your account |
| **Semantic embeddings** | Mathematical vector representations of call summaries (1536-dimensional vectors) used for memory retrieval | Not human-readable | Until you delete your account |
| **Relationship arc** | AI-generated narrative of how your relationship with the companion has evolved, including milestones and inside jokes | "The relationship has deepened over 20 calls..." | Until you delete your account |

**Important:** This memory system exists so your companion can remember you across conversations. The AI extracts facts, preferences, emotional patterns, and relationship history from your conversations to provide a personalized experience.

### 2.6 Device and Technical Data

| Data Point | Collected | Purpose |
|------------|-----------|---------|
| Device timezone | Yes (auto-detected each app launch) | Time-aware companion responses |
| Device locale | Yes (on first launch) | Language detection |
| Microphone audio | Streamed in real time, never stored | Voice calls |
| IP address | Incidentally, via standard HTTPS connections | Server infrastructure |
| Device identifiers (UDID, advertising ID) | **No** | N/A |
| GPS location | **No** | N/A |
| Contacts | **No** | N/A |
| Photos or camera | Only an image you choose to attach to feedback, or a screenshot of the App's own screen on a problem report you send (see 2.8); no camera access, no photo library scanning | Help us investigate what you report |
| Motion (accelerometer) | Read on your device only, never sent | Notice a shake to open "Report a problem" (you can turn this off in Settings) |
| Browsing history | **No** | N/A |

### 2.7 Data We Do NOT Collect

- We use one product-analytics service, **PostHog** (see 2.9). We do **not** use Mixpanel, Amplitude, Segment, Firebase Analytics, or similar
- We do **not** use crash reporting services (no Sentry, Crashlytics, or similar)
- We do **not** use advertising SDKs or tracking pixels
- We do **not** collect device identifiers or advertising IDs
- We do **not** use cookies (the App is a native mobile application)
- We do **not** record or store audio from calls

### 2.8 Feedback, Problem Reports and Answers You Send

When you use **Send feedback** (from the chat screen or Settings), we receive:

| Data Point | Required | Retention |
|------------|----------|-----------|
| Your message | Yes | Until account deletion |
| A screenshot or image you choose to attach (sent as JPEG or PNG up to 1 MB; larger images are shrunk on your device first) | No | Deleted automatically after 90 days, or when you delete your account |
| Whether you ticked "OK to contact me" | No | Until account deletion |
| App version, device model, operating system and app language | Yes (sent automatically) | Until account deletion |

When you use **Report a problem** (from Settings, by shaking your phone, or from an error message), we receive the same as above, plus:

| Data Point | Required | Retention |
|------------|----------|-----------|
| A screenshot of the App screen you were on, taken just before the report opened. It is attached by default, shown to you, and removed with one tap | No | Deleted automatically after 90 days, or when you delete your account |
| Technical details: app version and build, operating system and version, device model, app language, the name of the App screen you were on, and the last error code the App recorded | Yes (sent automatically) | Until account deletion |

No logs and no other content from your conversations are attached. A screenshot can show whatever was on that screen, including a chat, so look at the thumbnail before sending.

Now and then the App may ask **one short question** (for example, what stopped you from subscribing, or how you would feel without the App). Your tap is sent as a choice to our analytics (see 2.9). If you also type an optional comment, that text is stored with your feedback in our database, never in analytics.

Feedback, problem reports and comments are linked to your account so that, if you allow it, we can reply to your account email. They are stored in our database and a private storage bucket (Supabase), are read only by us to improve the App, and are never used for advertising or shared with third parties. Only the image you pick, or the screenshot you keep, is uploaded; the App does not read anything else from your photo library.

### 2.9 Product Analytics (PostHog)

To understand how the App is used and where it falls short, the App sends named usage events to PostHog (United States). These include: the app opening, a chat reply or voice call succeeding or failing (no content), running out of Whispers, opening or leaving the Whisper Pass or wallet screens, purchases (product, price and currency), the choices you tap on the short questions and the two optional setup questions in onboarding (what you mainly use the App for, how you heard about it), and problem reports being opened or sent (not their content). Each event carries the app version, operating system, device model, app language and an approximate location derived from your IP address.

Events are linked to your account ID, the same ID our purchase system uses, so that purchases and usage line up. They never contain your messages, your companion's replies, your voice, your email address or any text you type. The App does not record your taps or screens automatically.

**Session replay.** The App includes PostHog session replay, and it is **turned off**. If we turn it on in the future, it records only a small sample of sessions (about 1 in 10 devices), only from the moment you run out of Whispers or open the Whisper Pass or wallet screens. It records only the Whisper Pass, wallet, Settings and language screens. **All text, text fields and images are masked**, so recordings show the layout and taps, not what is written. Recording stops for the rest of the session as soon as you open any other screen (chat, calls, your companions, photos) or a feedback or question sheet. It never captures logs or network traffic. We will update this policy before turning it on.

---

## 3. How We Use Your Data

We use your data for the following purposes:

| Purpose | Legal Basis (GDPR) | Data Used |
|---------|-------------------|-----------|
| **Provide the service** — authenticate you, connect calls, generate AI responses | Performance of contract (Art. 6(1)(b)) | Account data, conversation data, companion config |
| **Companion memory** — enable your companion to remember facts, preferences, and relationship history across calls | Performance of contract (Art. 6(1)(b)) | Conversation transcripts, extracted profile facts, call summaries, relationship arc |
| **Time-aware responses** — allow your companion to reference the current time naturally | Performance of contract (Art. 6(1)(b)) | Device timezone |
| **Language localization** — display the App in your language | Performance of contract (Art. 6(1)(b)) | Device locale, preferred language |
| **Security** — protect against unauthorized access | Legitimate interest (Art. 6(1)(f)) | Authentication tokens, session data |
| **Improve the App** — understand how it is used, fix problems you report, learn from your answers | Legitimate interest (Art. 6(1)(f)) | Analytics events (2.9), feedback, problem reports and comments (2.8) |

We do **not** use your data for:
- Advertising or ad targeting
- Selling to third parties
- Training AI models (see Section 4 for third-party AI provider policies)
- Profiling for automated decision-making that produces legal effects

---

## 4. Third-Party Services and Data Sharing

We share data with the following third-party service providers, solely to operate the App. We do **not** sell your personal data to any third party.

### 4.1 AI and Voice Processing (Server-Side Only)

These services receive data only from our server. Your device never communicates with them directly.

**In-app consent:** Before your first conversation, the App asks for your explicit permission to share conversation data with the AI providers listed below, describing exactly what is sent to whom. Conversation features (voice calls, text chat, image generation) remain disabled until you agree. You can withdraw consent at any time by deleting your account or contacting us at highball@jocoding.net.

| Service | Data Sent | Purpose | Data Retention by Provider |
|---------|-----------|---------|---------------------------|
| **xAI (Grok)** | System prompt containing companion personality, your extracted profile facts, recent call summaries, relationship arc, conversation history (last 20 messages), and your current message; companion image prompts you write | Generate AI companion responses; post-call extraction of user facts and call summaries; companion image generation | Refer to [xAI's privacy policy](https://x.ai/legal/privacy-policy). xAI states it may use API inputs to improve models unless you opt out |
| **Deepgram** | Real-time audio stream (16kHz linear PCM) from your microphone during calls | Speech-to-text transcription | Refer to [Deepgram's privacy policy](https://deepgram.com/privacy). Audio is processed in real time and not stored by default for API customers |
| **MiniMax** | AI-generated response text, voice ID, language code | Text-to-speech synthesis (companion's voice) | Refer to [MiniMax's privacy policy](https://www.minimax.io/privacy-policy) |
| **OpenAI** | Call summary text (2-3 sentences per call) | Generate semantic embedding vectors for memory retrieval | Refer to [OpenAI's API data usage policy](https://openai.com/policies/api-data-usage-policies). OpenAI states it does not use API data to train models |

**What this means in practice:** When you speak during a call, your audio is streamed from our server to Deepgram for transcription. The resulting text, along with your conversation history and companion memory context, is sent to xAI's Grok model to generate a response. That response text is sent to MiniMax to produce audio, which is streamed back to you over an encrypted connection. After the call, a summary is sent to OpenAI for embedding generation and to Grok for memory extraction.

### 4.2 Authentication

| Service | Data Sent | Purpose |
|---------|-----------|---------|
| **Google** (if you use Google sign-in) | OAuth token, nonce | Verify your Google identity |
| **Apple** (if you use Apple sign-in) | Identity token | Verify your Apple identity |

### 4.3 Infrastructure

| Service | Data Stored | Purpose |
|---------|-------------|---------|
| **Supabase** | All persistent user data (database and file storage) | Managed PostgreSQL database, authentication, real-time subscriptions |
| **Railway** | Server application and logs (no persistent user data) | API server hosting |
| **Expo (EAS)** | Application source code during builds | Mobile app build and distribution |
| **RevenueCat** | App user ID (your account UUID), purchase receipts, subscription status | In-app purchase and subscription management | Refer to [RevenueCat's privacy policy](https://www.revenuecat.com/privacy/) |
| **PostHog** (United States) | Usage events described in 2.9, linked to your account ID; sent directly from the App | Product analytics | Refer to [PostHog's privacy policy](https://posthog.com/privacy) |

### 4.4 No Other Sharing

We do not share your data with:
- Advertisers
- Data brokers
- Social media platforms
- Law enforcement (unless required by valid legal process — see Section 8)
- Any other third parties not listed above

---

## 5. Data Storage and Security

### 5.1 Where Data Is Stored

- **Database:** Supabase-managed PostgreSQL (cloud infrastructure, region: **ap-northeast-2 (Seoul)**)
- **Server:** Hosted on Railway (**ap-southeast-1 (Singapore)**)
- **Device:** Authentication tokens stored in iOS Keychain / Android Keystore via platform-native encrypted storage. No conversation data is cached on your device.

### 5.2 Security Measures

- **Encryption in transit:** All data transmitted over HTTPS/TLS (including audio streams via secure WebSocket connections)
- **Encryption at rest:** Database encryption managed by Supabase's infrastructure
- **Row-Level Security (RLS):** Every database table enforces row-level security policies. You can only access your own data. Even with a valid session, one user cannot query another user's conversations, memories, or companion data
- **API key isolation:** All AI service API keys (xAI, OpenAI, Deepgram, MiniMax, Twilio) are stored server-side only and never exposed to the mobile app
- **Secure token storage:** Authentication tokens are stored using platform-native secure storage (iOS Keychain, Android Keystore), never in unencrypted local storage
- **No audio recording:** Voice audio is processed as a real-time stream and never persisted

### 5.3 Data Breach Notification

In the event of a data breach affecting your personal data, we will notify you and the relevant supervisory authorities within the timeframes required by applicable law (72 hours under GDPR, without delay under PIPA).

---

## 6. Data Retention

| Data Category | Retention Period | Deletion Trigger |
|---------------|-----------------|------------------|
| Account data (email, name, avatar) | Until account deletion | You delete your account |
| Profile preferences (language, theme, timezone) | Until account deletion | You delete your account |
| Companion configurations | Until account deletion | You delete your account or the companion |
| Conversation transcripts (messages) | Until account deletion | You delete your account |
| Call metadata (logs) | Until account deletion | You delete your account |
| AI-extracted user profile facts | Until account deletion | You delete your account |
| Call summaries and embeddings | Until account deletion | You delete your account |
| Relationship arc narrative | Until account deletion | You delete your account |
| Authentication tokens (on device) | Until you sign out | Sign out or account deletion |
| Feedback messages and device details | Until account deletion | You delete your account |
| Feedback screenshots and problem-report screenshots | 90 days, or until account deletion if sooner | Automatic deletion, or you delete your account |
| Problem-report technical details and question comments | Until account deletion | You delete your account |
| Analytics events (PostHog) | Up to 1 year under our PostHog plan | Automatic expiry; deleted sooner on request (Section 7.4) |
| Server logs (operational, no user content) | 30 days | Automatic rotation |

**Cascade deletion:** When you delete your account, all associated data is automatically and permanently deleted through database cascade rules: your profile, all companions, all conversations, all messages, all call logs, all extracted memories, all call summaries, and all relationship data.

---

## 7. Your Rights

### 7.1 Rights Under GDPR (EU/EEA Users)

You have the right to:

- **Access** (Art. 15): Request a copy of all personal data we hold about you
- **Rectification** (Art. 16): Correct inaccurate personal data
- **Erasure** (Art. 17): Request deletion of your personal data ("right to be forgotten")
- **Restriction** (Art. 18): Request we limit processing of your data
- **Data portability** (Art. 20): Receive your data in a structured, machine-readable format
- **Object** (Art. 21): Object to processing based on legitimate interest
- **Withdraw consent** (Art. 7(3)): Where processing is based on consent, withdraw at any time

**Automated decision-making:** We use AI to extract facts, generate summaries, and assess emotional tone from your conversations. These processes are integral to providing the companion service and do not produce legal or similarly significant effects on you. You may object to this processing at any time.

### 7.2 Rights Under Korea PIPA (Korean Users)

You have the right to:

- Request access to your personal information
- Request correction of inaccurate information
- Request deletion or suspension of processing
- Be informed of the purpose and method of personal information processing
- Be notified of any third-party provision of your personal information
- Designate a legal representative to exercise your rights

We process personal information of Korean users in accordance with PIPA and will respond to requests within 10 days.

### 7.3 Rights Under CCPA (California Users)

You have the right to:

- **Know** what personal information we collect, use, and disclose
- **Delete** your personal information
- **Opt out of sale**: We do not sell your personal information. No opt-out is necessary.
- **Non-discrimination**: We will not discriminate against you for exercising your rights

**Categories of personal information collected (CCPA categories):**
- Identifiers (email, name, account IDs)
- Internet or electronic network activity (conversation transcripts, call metadata)
- Inferences drawn from the above (AI-extracted profile facts, emotional assessments, relationship narratives)

**We have not sold personal information in the preceding 12 months. We do not sell personal information.**

### 7.4 How to Exercise Your Rights

To exercise any of the rights above, contact us at:

**Email:** highball@jocoding.net

We will verify your identity and respond within:
- 30 days (GDPR)
- 10 days (PIPA)
- 45 days (CCPA, extendable by 45 days with notice)

You may also delete your account directly from within the App under **Settings > Account > Delete Account**, which triggers permanent cascade deletion of all your data.

---

## 8. Legal Disclosures

We may disclose your personal data if required to do so by law or in response to valid requests by public authorities (e.g., a court order or government agency). We will notify you of such requests unless prohibited by law.

---

## 9. International Data Transfers

Your data may be processed in countries outside your country of residence, including the United States, where our third-party service providers operate. For transfers from the EU/EEA, we rely on:

- Standard Contractual Clauses (SCCs) approved by the European Commission
- Adequacy decisions where applicable
- Service provider certifications and contractual safeguards

For transfers from Korea, we comply with PIPA cross-border transfer requirements, including obtaining your consent where required and ensuring the receiving party maintains adequate protections.

---

## 10. Children's Privacy

The App is not intended for users under the age of:
- 16 (EU/EEA, under GDPR)
- 14 (Korea, under PIPA)
- 13 (United States, under COPPA)

We do not knowingly collect personal data from children below these ages. If we discover that we have collected data from a child below the applicable age, we will delete it promptly. If you believe a child has provided us with personal data, contact us at **highball@jocoding.net**.

---

## 11. Sensitive and Behavioral Data Disclosure

**This section is important. Please read it carefully.**

The nature of an AI companion app means that conversations are inherently personal. The data we collect and process includes:

- **Emotional and psychological content:** Your conversations may reveal emotional states, mental health concerns, personal anxieties, relationship issues, and other sensitive topics. Our AI extracts and stores emotional tone assessments and personal facts from these conversations.
- **Personal and affectionate content:** Conversations with a companion can be personal and affectionate in nature. Transcripts of such conversations are stored in our database. AI-extracted facts from these conversations may include personal preferences or relationship details.
- **Behavioral patterns:** Over time, the companion memory system builds a detailed profile of your personality, preferences, habits, relationships, work life, and emotional patterns.
- **Relationship simulation data:** The relationship arc narrative tracks how your simulated relationship with the AI evolves, including milestones and inside jokes.

This data is collected solely to provide the companion experience. We do not use it for advertising, profiling for third-party purposes, or any use beyond operating the App.

Under GDPR, some of this data may qualify as "special category" data (Art. 9). We process it on the basis that you have given **explicit consent** by choosing to engage in conversations with the companion and by agreeing to this Privacy Policy.

Under PIPA, this data is treated as "sensitive information" and is processed with your consent.

---

## 12. Changes to This Policy

We may update this Privacy Policy from time to time. We will notify you of material changes by:
- Posting the updated policy in the App
- Updating the "Last Updated" date at the top
- Sending an in-app notification for significant changes

Your continued use of the App after changes constitutes acceptance of the updated policy.

---

## 13. Contact Us

For privacy-related inquiries, data access requests, or complaints:

**Email:** highball@jocoding.net
**Address:** 16 Wausan-ro 29-gil, Mapo-gu, Seoul, South Korea

If you are in the EU/EEA, you have the right to lodge a complaint with your local data protection authority.
If you are in Korea, you may file a complaint with the Personal Information Protection Commission (PIPC).
If you are in California, you may contact the California Attorney General's office.

---

## 14. Data Protection Officer

At our current scale, a formal DPO appointment is not required. The personal information protection officer (highball-jo, highball@jocoding.net) handles all data protection inquiries. We will appoint a dedicated DPO if and when required by applicable law.

---

*This Privacy Policy is provided in English. Translations may be provided for convenience, but the English version is the authoritative version in case of conflict.*
