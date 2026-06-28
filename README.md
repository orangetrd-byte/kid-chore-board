# Kid Chore Board PWA

Kid Chore Board is a simple mobile-first progressive web app that creates age-appropriate chore plans for children ages 2 through 18. It shows a complete Daily/Weekly/Monthly chore list for the selected age range, lets chores be assigned to one or more children, tracks each chore's status, and shows reward progress with a leaderboard.

## How to Run Locally

Use any static web server from this folder, then open the local URL in a browser.

```bash
python -m http.server 8000
```

## How to Install

Open the app in a browser that supports PWAs, then choose the browser's install option. The app includes a manifest and service worker so it can run in standalone mode and load offline after the first visit.

## Family Sync

The app syncs through Firebase Firestore. Use the same family code on every device. The app stores one document at `families/{family-code}` and keeps local storage as the offline fallback.

## File Structure

```text
index.html
manifest.json
service-worker.js
README.md
icon-192.png
icon-512.png
```

## Editing Chores

Chores live in the `chorePlans` object inside `index.html`. Update the `daily`, `weekly`, or `monthly` arrays for each range: `2-3`, `4-5`, `6-8`, `9-10`, `11-12`, `13-15`, or `16-18`. Each range also has a `note` for supervision and safety guidance. Daily chores are worth 1 point, weekly chores are worth 3 points, and monthly chores are worth 5 points.

## Replacing Icons

Replace `icon-192.png` and `icon-512.png` with new PNG files using the same names and dimensions. Keep the manifest icon paths unchanged unless the file names change.
