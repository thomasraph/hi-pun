# Hi Pun

**Version 1.0.0 · October 25, 2026**

Hi Pun is a personal English ⇄ Hindi ⇄ Punjabi translator for iPhone. Type a phrase in any of the three languages, including romanized text, Hinglish/Punglish and slang. Hi Pun works out which language it is and gives you **casual**, **formal** and **texting** versions in both Hindi and Punjabi. Every version has a "learn more" breakdown, and a Word of the Day for each language helps you build vocabulary.

---

## Contents

1. [Features](#features)
2. [Setup](#setup)
3. [Using Hi Pun](#using-hi-pun)
4. [Costs and the credit meter](#costs-and-the-credit-meter)
5. [Privacy](#privacy)
6. [Updating the app](#updating-the-app)
7. [Troubleshooting](#troubleshooting)
8. [Known limitations](#known-limitations)
9. [Files in this folder](#files-in-this-folder)
10. [Release notes](#release-notes)

---

## Features

| Area | What it does |
|---|---|
| Language detection | Shows the language live as you type. Recognizes Devanagari (Hindi), Gurmukhi (Punjabi), English, and romanized Hindi or Punjabi such as "kya scene hai" or "ki haal aa". |
| Three registers | **Casual** (friends, people your age), **Formal** (elders, strangers, work) and **Texting** (how people actually type on WhatsApp/Instagram). |
| Modern speech | Understands slang and shorthand (lowkey, ngl, no cap, wyd), emoji and code-mixing, and explains each slang term it finds. |
| Sikh Punjabi | Punjabi is always Gurmukhi and follows Sikh usage: Sat Sri Akal, Waheguru-based expressions, *ji* and Sikh kinship terms. Other religions' greetings are never used. |
| Male speaker | Every first-person sentence uses masculine forms (*main ja raha hoon*, *maiṃ jā rihā hāṃ*). The listener is masculine unless the phrase says otherwise. |
| Learn more | A book icon on each Casual, Formal and Texting card opens a breakdown of that version only: word by word, grammar, pronunciation, when to use it, and alternatives. On Texting cards it decodes the shorthand. |
| Word of the Day | One Hindi and one Punjabi word each day, with an example sentence, romanization and tip. There are 40 words per language, including 10 everyday verbs. |
| Verb tenses | Learn more on a verb shows 11 forms built on the same sentence: present, present continuous, habitual past, past, past continuous, present perfect, future, can, want to, and casual and polite commands. |
| Common uses | Learn more on any word lists 4–6 real expressions with notes, plus related words and a tip. |
| Listen | Reads Hindi or Punjabi aloud when your phone has a voice for that language. |
| Recent | Your last 8 phrases, saved on the phone and free to reopen. |
| Credit meter | An estimate of the Anthropic credit you have left, shown at the top. |
| Works offline | Word of the Day and Recent open without internet. Translating needs a connection. |
| Light and dark mode | Follows your iPhone's appearance setting. |

---

## Setup

### 1. Claude API key

1. Sign in at **console.anthropic.com**.
2. Under **Billing**, add some credit (for example, $5).
3. Under **Limits**, set a monthly spend limit.
4. Under **API Keys**, create a key and copy it. It starts with `sk-ant-`.

### 2. Put the app online (GitHub Pages, free)

1. Create a **public** repository named `hi-pun` on github.com.
2. Upload **all** the files from this folder: open the repository, choose **Add file → Upload files**, drag the files in and commit.
3. Go to **Settings → Pages** and set the source to *Deploy from a branch*, branch **main**, folder **/ (root)**. Save.
4. After about a minute the app is live at **https://thomasraph.github.io/hi-pun/**.

Your API key is not in any of these files, so a public repository is safe.

### 3. Install on iPhone

1. Open the link in **Safari**.
2. Tap **Share** (the square with an arrow), then **Add to Home Screen**, then **Add**. Hi Pun shows this tip at the top until it's installed.
3. From now on, open Hi Pun from its home-screen icon. It runs full screen, without Safari's bar.

### 4. First launch

1. Tap **Add key** and paste your `sk-ant-` key.
2. Enter your current **credit balance** from the Anthropic console's Billing page.
3. Tap **Save**. You're ready.

---

## Using Hi Pun

- **Translate:** type or paste a phrase and tap **Translate** (or the **Go** key). Hi Pun opens on the tab for the language you typed in.
- **Switch languages:** use the **Hindi / Punjabi** tabs.
- **Copy:** use the copy icon on any card.
- **Listen:** use the speaker icon (only shown when your phone has the voice).
- **Learn more:** tap the **book icon** on a card. Tap it again to close. Breakdowns stay open when you switch tabs.
- **Word of the Day:** tap the **book icon** for tenses (verbs), forms, common uses and related words. **Break down this sentence** sends the example into the translator.
- **Recent:** tap a phrase to reopen it at no cost.
- **Settings:** the gear icon, or tap the credit meter.

---

## Costs and the credit meter

Each of these sends one request to Claude (model: `claude-sonnet-5-5`) and uses your API credit:

| Action | Approximate cost* |
|---|---|
| Translate | ~1–2¢ |
| Learn more on a card | ~1–2¢ |
| Learn more on Word of the Day | ~2¢ the first time that day, then free (saved on the phone) |
| Reopening Recent, Word of the Day, Listen, Copy | Free |

\*These estimates use $2 per million input tokens and $10 per million output tokens, a price taken from a third-party pricing site. Check console.anthropic.com for current prices, and change them in **Settings → Model prices** if they differ.

**How the meter works:** Anthropic doesn't let apps read your real balance. Hi Pun starts from the balance you enter and subtracts the cost of each request, using the token counts Claude reports. The meter turns **gold below $1** and **red below $0.25**. It only counts Hi Pun's own usage, so re-enter your real balance after topping up or now and then to re-sync.

---

## Privacy

- Your API key, credit figures, Recent phrases and saved Word of the Day breakdowns are stored **only on your iPhone**, inside the app.
- Phrases you translate are sent directly from your phone to Anthropic's API. Nothing passes through any other server.
- **Settings → Remove key** deletes the key from the phone.

---

## Updating the app

Upload the new files to the same `hi-pun` GitHub repository, replacing the old ones. The installed app picks up the update the next time it opens with internet. If it still looks old, close it fully and open it again.

---

## Troubleshooting

| Message or problem | What to do |
|---|---|
| "Add your Claude API key in Settings" | Tap the gear and paste your key. |
| "That API key didn't work" | Copy the full key again from console.anthropic.com. Make sure it wasn't deleted. |
| "Your Anthropic account is out of credit" | Add credit under Billing, then update your balance in Settings. |
| "Too many requests right now" | Wait a minute and try again. |
| "You're offline" | Connect to the internet. Word of the Day and Recent still work offline. |
| No Listen button | Your iPhone has no voice for that language. Hindi voices are common; Punjabi voices often aren't available. |
| Credit meter looks wrong | Re-enter your real balance from the console in Settings. |
| App looks out of date after an update | Close Hi Pun from the app switcher and reopen it with internet. |

---

## Known limitations

- The credit meter is an estimate, not your real balance.
- Translations are generated by Claude and can occasionally be imperfect, especially rare slang or regional idioms.
- Each **learn more** breakdown on a translation card is kept only until you translate something else or close the app.
- Punjabi text-to-speech depends on iOS and may not be available.
- Model prices are entered by hand and don't update automatically.

---

## Files in this folder

| File | Purpose |
|---|---|
| `index.html` | The app |
| `manifest.webmanifest` | App name, icon and colours for the home screen |
| `sw.js` | Offline support and caching |
| `apple-touch-icon.png` | iPhone home-screen icon |
| `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` | Other icon sizes |
| `README.md` | This document |

---

## Release notes

### 1.0.0 — October 25, 2026
**First release.**

**Translation**
- Detects English, Hindi or Punjabi as you type, including romanized Hindi and Punjabi ("kya scene hai", "ki haal aa") and Hinglish/Punglish.
- Gives **Casual**, **Formal** and **Texting** versions in both Hindi and Punjabi, each with script, romanization and when to use it.
- Shows the English meaning when the input is Hindi or Punjabi.
- Understands slang, shorthand and emoji (lowkey, ngl, no cap, wyd, 🔥) and explains each one it finds.
- Notes anything a learner should know, such as phrases with no direct equivalent.

**Language rules**
- **Sikh Punjabi:** Gurmukhi only; Sat Sri Akal and Waheguru-based expressions; *ji* and Sikh kinship terms (ਪਾਜੀ, ਭੈਣ ਜੀ, ਬਾਬਾ ਜੀ); native Punjabi words over Hindi or Urdu loanwords; never other religions' greetings.
- **Male speaker:** all first-person Hindi and Punjabi uses masculine forms. The listener is masculine unless the phrase indicates a woman.

**Learn more**
- A book icon on each Casual, Formal and Texting card opens a breakdown of that version only: word by word, grammar, pronunciation, when to use it, and other ways to say it.
- Texting breakdowns decode the shorthand and explain how to read it aloud.
- Open breakdowns stay open when you switch between the Hindi and Punjabi tabs.

**Word of the Day**
- One Hindi and one Punjabi word each day, with romanization, meaning, an example sentence and a tip. Words change at midnight, local time.
- 40 words per language, including 10 everyday verbs. Punjabi words include Sikh concepts (ਚੜ੍ਹਦੀ ਕਲਾ, ਸੇਵਾ, ਲੰਗਰ, ਮਿਹਰ).
- The book icon shows an 11-row tense table for verbs, forms for other words, 4–6 common uses, related words and a tip. These breakdowns are saved on the phone, so reopening them is free.
- **Break down this sentence** sends the example into the translator.

**App and iPhone**
- Installs on the iPhone home screen and runs full screen. Safari shows an "Add to Home Screen" tip until the app is installed.
- Talks to Claude directly with your own API key, which is stored only on the phone. Settings lets you add or remove it.
- Credit meter estimating your remaining Anthropic credit: gold below $1, red below $0.25. Settings shows usage stats and editable model prices.
- Recent phrases (last 8), Listen, Copy, suggested phrases, and light and dark mode.
- Word of the Day and Recent work offline.
- iPhone details: no zooming when you tap a text box, a **Go** key that translates, no tap flash, and layout clear of the notch and home bar.
- Clear messages for a missing or bad key, no credit, rate limits and being offline.
