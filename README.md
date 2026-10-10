# Vrinda for Android

A voice assistant you talk to. Tap the glowing ring, speak, and Vrinda answers out loud using Claude.
She follows the language you speak (English, Hindi, Telugu, Tamil and more).

## What you need

A Claude API key from https://console.anthropic.com. API usage is billed separately from the Claude app.
Paste the key into Settings the first time you open Vrinda. It is stored only on your phone.

## Get the app onto your phone

### Option A: Android Studio (works offline once set up)

1. Install Android Studio (free).
2. Choose File > Open and select this folder. Wait for Gradle to finish syncing.
3. Plug in your phone with USB debugging on, or start an emulator, then press Run.

### Option B: Build the APK on GitHub (nothing to install)

1. Create a new private repository on GitHub and upload everything in this folder, including the hidden `.github` folder.
2. Open the repository's Actions tab. The "Build Vrinda APK" run starts by itself.
3. When it finishes, open the run and download `vrinda-debug-apk` from Artifacts. Unzip it.
4. Send `app-debug.apk` to your phone and open it. Allow "install unknown apps" when Android asks.

## What she can do

- Listen and reply by voice, with the ring showing listening, thinking and speaking.
- Keep a conversation going (she remembers the last 20 turns until you close the app).
- Set timers in your phone's clock app ("set a 10 minute timer").
- Keep listening after each reply if you turn on the hands-free switch in Settings.

## What she cannot do yet

- Wake up when you say her name. Android only allows that for dedicated wake-word engines.
- Call, message or change phone settings.
- Remember anything after the app closes.

## Files

- `app/src/main/java/com/vrinda/assistant/MainActivity.kt`: listening, speaking, conversation, settings
- `Claude.kt`: the call to the Claude API
- `OrbView.kt`: the animated ring
