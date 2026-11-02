# Whisper House

A party game for friends and family: clues, doors, a knock in the dark, and one Mimic hiding in plain sight.

- Tablet / foldable mode: one shared screen, pass it around (works offline).
- Phone mode: the table device hosts and shows a game code. Players open the game on their phones, enter the code and pick a seat to see their private card.

## Run locally
    npx serve www

## Package for Android / iOS (Capacitor)
    npm install @capacitor/core @capacitor/cli @capacitor/android @capacitor/ios
    npx cap add android      # and/or: npx cap add ios
    npx cap sync
    npx cap open android     # opens Android Studio -> Build -> Generate Signed Bundle (AAB)

Change `appId` in capacitor.config.json to your own reverse-domain id before the first build. It cannot be changed after publishing.

## Notes
- The in-page language translation uses Claude and only works when hosted on claude.ai. For your own hosting, ship translated strings or add your own translation backend.
- Ads (AdMob) and "Remove ads" purchases are added in the native app, not in this web page.
- Never commit signing keys (.jks / .keystore). They are in .gitignore.
