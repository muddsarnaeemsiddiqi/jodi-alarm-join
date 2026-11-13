# Jodi Alarm — Join Page

Public landing page + join redirect for the **Jodi Alarm** Android app.

- **Live page:** https://muddsarnaeemsiddiqi.github.io/jodi-alarm-join/
- **App repo (private):** https://github.com/muddsarnaeemsiddiqi/jodi-alarm
- **Latest APK:** https://github.com/muddsarnaeemsiddiqi/jodi-alarm-join/releases/latest

## What is Jodi Alarm?

Jodi Alarm is a free Android app to **share alarms** with friends, family or your partner.

- No account, no subscription, no ads, no tracking.
- Send an alarm from your phone and it rings on every phone in the group.
- When they snooze or dismiss it, you get a status notification back.

## Features

- **Multiple groups** — a separate group, code and alarms for each friend or family member.
- **Send to one person or everyone** — pick a contact chip or the whole group.
- **Scheduled alarms** with an optional message, plus **Ring now** for instant ringing.
- **Delivery confirmation** — see who received your alarm.
- **Delete options** — delete for yourself, for others, or everywhere.
- **Member list** — see everyone who joined a group.
- Alarm tone, volume, vibration, loop, snooze (5/10/15/20 min).
- Full-screen alarm that rings even if the app is closed.
- Zero tracking, zero analytics, zero ads.

## How it works

A group is one shared code. The code derives an ntfy.sh topic and an AES-GCM encryption key. Messages are encrypted on your phone and decrypted on the receiver's phone. The receiver sets an exact alarm via AlarmManager; when it fires, a foreground service plays the tone and opens the alarm screen. Internet is needed only when sending; alarms ring offline.

## Releases & changelog

### v1.2.26 — report cleanup
- "Clear delivered" and "Clear all" buttons in the sent messages report.

### v1.2.25 — update check fix
- Update check now tolerates a BOM/whitespace in latest.json.
- GitHub Pages serves files raw (.nojekyll) to avoid encoding changes.

### v1.2.24 — message delivery reports
- "Sent messages" screen shows pending / received-by status for each custom message.
- Delivery confirmations arrive automatically.

### v1.2.23 — custom messages + reliability
- Custom group messages: send a text to everyone or one member; arrives as a notification with a beep (no alarm screen).
- Duplicate alarms after reconnects are ignored.
- Local alarms and missed repeating alarms restored after reboot.
- One-off alarms can be set for a specific future date.
- "Test alarm sound" button in Settings.
- New message notification channel with its own sound.

### v1.2.22 — startup permission setup
- Permission screen opens automatically at app start and walks through every needed permission.
- "Allow all permissions" button added in Settings.

### v1.2.21 — edit, delete and repeat days
- Tap an alarm to edit time, message and repeat days; Delete button on every card.
- Frequency: Once, Daily, Weekdays, Weekends or custom Mon–Sun days.
- Repeating alarms reschedule automatically after ringing.

### v1.2.20 — update check fixed
- "Check for updates" no longer fails with HTTP 403; it reads `latest.json` from GitHub Pages (no rate limit).

### v1.2.19 — previous colour scheme restored
- Same new layout as v1.2.18, but the original Material dark colours are back (lavender accents, solid cards, no gradient).

### v1.2.18 — new UI design
- Whole app UI redesigned to match the new mockup.
- One pill-style Local/Group switcher (no more duplicate tab row); counts always match the list.
- Bottom navigation: Alarms, Groups, Settings. Settings is an icon in the top bar.
- Round + button above the bottom bar for a new local alarm.
- Alarm cards with big 24-hour time, label, meta line and purple toggle; disabled alarms fade to 50%. Delete is long-press.
- Group tab: group chips, purple group card with monospace code and Select / Share / Copy / Rename / Delete, "UPCOMING (GROUP)" section, green/amber delivery status, compact Send and Ring buttons.
- Dark purple gradient theme, cleaner 16dp spacing, scrollable lists with room for the FAB and bottom bar.

### v1.2.10 — in-app update download
- Update now downloads inside the app via DownloadManager (no Chrome / browser).

### v1.2.9 — group list fix
- Delete button no longer wraps to a second line in the group list.

### v1.2.8 — auto-fill group name
- Joining via a shared link now auto-fills the group name.

### v1.2.7 — update check fixed
- In-app update check uses the public channel, works without GitHub login (fixes HTTP 404).

### v1.2.6 — check for updates
- Settings → Check for update queries GitHub and offers a one-tap download.
- Share text now includes the group name.

### v1.2.5 — contacts & sender name
- Send to one person or everyone via a contact chip list.
- Sender name shown on the alarm screen and notification.

### v1.2.4 — delete options
- Sender can delete for themselves, for others, or everywhere.
- Receivers can only delete their own copy.

### v1.2.3 — member list & delivery confirmation
- Group card lists all joined members.
- Delivery confirmation: see who received your alarm.

### v1.2.2 — English UI & no double sound
- Whole app in English.
- Ring now no longer rings on your own phone unless "Also ring on my phone" is on.
- No overlapping sound: notification channel is silent, only the ring service plays.
- WhatsApp share sends a clickable https link.

## Install

1. Download the latest APK.
2. Install it (allow unknown sources).
3. Open the app → enter your name → Create a new group or Join with a code.
4. Share the code with the Share button (WhatsApp / email).
5. Allow: Exact alarm, Full-screen alarm, Display over other apps, Notifications, Battery optimization off.

Updates install over the old version; your data stays.

## Links

- Download latest APK: https://github.com/muddsarnaeemsiddiqi/jodi-alarm-join/releases/latest
- Source code: https://github.com/muddsarnaeemsiddiqi/jodi-alarm
- Join page: https://muddsarnaeemsiddiqi.github.io/jodi-alarm-join/
