# DocCoach — Real-Time Meeting Assistant

A browser-based meeting coach for iPhone. Listens to conversations in real-time, matches what's being said to your uploaded documents/guides, and tells you **when to stay quiet** and **what key points to make** when you should speak.

---

## Setup (2 minutes)

### 1. Get API Keys (both free to start)

**Deepgram** (speech-to-text — 12,000 min/year free):
1. Sign up at https://console.deepgram.com
2. Create a new API key → copy it

**Anthropic** (AI coaching):
1. Sign up at https://console.anthropic.com
2. Create an API key → copy it
3. Add a small credit ($5 goes a long way with claude-haiku at ~$0.20/hour of meetings)

### 2. Host for Free

**Option A — GitHub Pages** (recommended if repo is public):
1. Push this repo to GitHub
2. Go to repo Settings → Pages → Source: `main` branch, `/ (root)` → Save
3. Access at `https://YOUR-USERNAME.github.io/REPO-NAME/`

**Option B — Netlify** (works with private repos):
1. Drag-and-drop `index.html` to https://netlify.com/drop
2. Get an instant HTTPS URL

**Option C — Local**:
- Open `index.html` directly in Safari (mic may require HTTPS for Deepgram)

### 3. First Launch
1. Open the URL on your iPhone in Safari
2. Enter a password (protects the app on the device)
3. Enter your Deepgram and Anthropic API keys
4. Tap **Get Started**

---

## Using the App

### Add Documents
1. Tap **Docs** tab → **+ Add Document**
2. Upload a file (PDF, DOCX, PPTX, XLSX, MD, TXT) — tapping opens Files app on iPhone
3. Or paste text directly
4. Tap **Save Document**

Repeat for all your guides, sales playbooks, FAQs, etc.

### Meeting Mode
1. Tap **Meeting** tab
2. Tap the **🎤 microphone button** — grant mic permission when asked
3. The app starts listening and transcribing in real-time
4. Every 10 seconds (adjustable), it analyzes the conversation against your documents
5. The guidance card shows:
   - 🔴 **STAY QUIET** — conversation is in flow, let it play out
   - 💬 **SPEAK NOW** — relevant moment, here are your talking points

### Transcript History
- Each session is auto-saved every 10 seconds
- After stopping, tap **Download Transcript (.txt)** to save to Files app
- View/download/delete past sessions in the **History** tab

---

## Tips for Best Results
- Keep documents focused — shorter, sharper guides give better key points
- The app listens to **all room audio** including others speaking — this is intentional so it can tell you when a natural break is coming
- Adjust the analysis interval (5–30s) in the meeting screen — faster = more real-time, more API calls
- Add your iPhone to home screen (Share → Add to Home Screen) for app-like experience

---

## Privacy
- All documents and transcripts are stored **only on your device** (localStorage)
- API keys are encrypted with your password using AES-256-GCM
- Audio is streamed to Deepgram for transcription (see their privacy policy)
- Transcripts are sent to Anthropic Claude for analysis (see their privacy policy)
- No data is stored on any other server
