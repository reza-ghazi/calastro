# CalAstro — Privacy Policy

_Last updated: October 27, 2026_

CalAstro is a Chrome extension for astronomical calendar conversion, Sun and Moon times, and
prayer times. This policy explains what data the extension handles and where it goes.

## Summary
- CalAstro has **no server, no account, no analytics and no advertising**. The publisher
  receives no data from you.
- All calculations run **on your device**.
- On first use, CalAstro downloads its astronomical data (about 223 MB, once) from the
  project's public website. Nothing about you is sent.
- The location you choose and your settings are stored **only in your browser**.
- Apart from that one-time download, the extension contacts the network only if you turn on
  **data updates**. It then downloads two public scientific files and sends nothing about you.

## Data the extension handles
| Data | Purpose | Where it is stored | Shared with |
|---|---|---|---|
| Location you choose (a city from the built-in list, coordinates you type, or your current position when you click "Use my location"), its time zone and elevation | Sun, Moon and prayer times for that place | Chrome extension storage on your device | No one |
| Settings (language, numerals, theme, calendars, calculation methods, saved places) | Remember your preferences | Chrome extension storage on your device | No one |
| Astronomical data downloaded once on first use (JPL ephemeris files) | Sun, Moon and calendar calculations | Extension storage (Cache Storage) on your device | No one |
| Downloaded Earth-orientation and leap-second data (only if updates are on) | Keep time calculations current | Chrome extension storage on your device | No one |

## Your location
CalAstro reads your current position **only when you click "Use my location"**. Chrome may ask
for your permission first. The position is matched to the nearest place in the extension's
built-in list (on your device) to choose a time zone. It is stored only in your browser and is
never sent anywhere. You can instead pick a city or type coordinates.

CalAstro has no access to your browsing, tabs, page contents, history, cookies or passwords, and
it runs no content scripts.

## One-time astronomical data download
The Sun and Moon calculations use NASA JPL's DE442 and DE441 ephemerides. To keep the extension
small, these public data files (about 223 MB) are not inside the extension package. When
CalAstro is first installed it downloads them once from the project's website,
`https://reza-ghazi.github.io/calastro/data/ephemeris/`, which is hosted by GitHub Pages. Each
file is checked against a SHA-256 checksum packaged with the extension before it is used, and
the files are kept on your device across updates, so they are not downloaded again.

These are plain downloads of fixed public files, made without cookies or credentials. As with
any web request, GitHub, which hosts the website, sees your IP address and the files requested.
Nothing else is sent, and the publisher does not receive this information. Until the download
finishes, the Gregorian, Julian and tabular Islamic calendars already work.

## Data updates (optional, off until you turn them on)
When you choose **Enable automatic updates** in Settings, Chrome asks you to allow access to
two websites. If you allow it, CalAstro downloads these files, at most about once a week:
- `https://maia.usno.navy.mil/ser7/finals2000A.all`: Earth-orientation parameters published
  by the IERS (via the U.S. Naval Observatory);
- `https://data.iana.org/time-zones/tzdb/leap-seconds.list`: the official leap-second list.

These are plain downloads of public files, made without cookies or credentials. As with any web
request, those servers see your IP address. Nothing else is sent. Downloaded files are checked
for validity before use, and you can turn updates off at any time; the data packaged with the
extension is then used.

## Retention and deletion
Your data stays in your browser until you change it. Uninstalling the extension deletes all of
its stored data. Settings backups you download are files you control.

## Limited use
CalAstro uses data only to provide its calendar, astronomy and prayer-time features. It does
not sell or transfer data to third parties, does not use or transfer data for advertising,
creditworthiness or any unrelated purpose, and allows no human access to your data. This
complies with the Chrome Web Store User Data Policy, including the Limited Use requirements.

## Changes
If CalAstro's data practices change, this policy will be updated before the new version is
published, and the date above will change.

## Contact
contact@brightarcadia.com
