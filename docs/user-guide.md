# CalAstro user guide

## Getting started
1. Click the CalAstro icon in Chrome's toolbar. The popup shows:
   - today's date in your chosen calendars;
   - the Sun's times and the next event;
   - the Moon's phase.
   On first use, CalAstro downloads its astronomical data once (about 223 MB, for 1 CE – 3000 CE)
   and shows the progress. The first time you look up a date before 1 CE or after 3000 CE, it
   downloads the data for 5001 BCE – 5000 CE (about 516 MB more), also once. Gregorian, Julian and tabular Islamic dates work at once; Sun, Moon and the
   astronomical calendars appear when the download finishes. After that, CalAstro works offline.
2. Click **Open CalAstro** for the full page. It has five tabs: **Today**, **Convert**,
   **Sun & Moon**, **Prayer times** and **Settings & methods**.
3. In **Settings & methods**, set your location in any of three ways:
   - search for a city (34,000 places, available offline);
   - click **Use my location**;
   - type the latitude, longitude, elevation and time zone.

## Converting dates
On **Convert**:
1. Choose the calendar you are converting from.
2. Enter the day, month and year. For Gregorian, Julian, tabular Islamic and Hebrew, choose the
   era: CE or BCE, AH or BH, AM or BAM. Hebrew leap years list Adar I and Adar II. Years are counted as in the calendars themselves, with no year zero: 1 BCE is
   followed by 1 CE, and 1 BH by 1 AH.
3. Press **Convert**. **Today** resets the form to today's date in the selected calendar.

The same day is shown in every calendar, each with its weekday in that calendar's own names
(for example Yekshanbeh in Solar Hijri, al-Ahad in Islamic, Sunday in Gregorian), and with its
Julian Day Number. Each result
has a copy button.
- A **±1** badge on a Solar Hijri date means the year boundary is too close to call (see the
  [methods](methods.md)).
- **Islamic (predicted)** follows the policy chosen in Settings:
  - the Umm al-Qura rule (default);
  - Odeh or Yallop crescent visibility, at Makkah or at your location.
- **Islamic (tabular)** follows the arithmetic variant chosen in Settings.

## Sun and Moon
**Sun & Moon** shows the events of the local day, from 00:00 to 24:00 in your location's time
zone:
- astronomical, nautical and civil dawn;
- sunrise, solar noon and sunset;
- the dusks;
- moonrise, moonset and the Moon's meridian transit;
- the Moon's phase at local midday.

When the Sun or Moon does not rise or set that day, CalAstro says so.

## Prayer times
**Prayer times** shows the start of each prayer period for the chosen date:
- **Calculation method:** by default it follows your location's country. Every method lists
  its sources and whether they are primary.
- **Options:** the Asr school, the high-latitude rule and Ramadan timetables can be changed.
- **Qibla:** the bearing is measured from true north along the WGS84 geodesic.
- Sunrise is shown because it ends the Fajr period; it is not a prayer time. Mosque iqamah
  times are set locally.

## Language and display
- English or Persian, with Latin or Persian numerals in either language.
- Light, dark or system theme.
- A 24-hour or 12-hour clock.
- Which calendars to show.

## Data updates
In **Settings & methods → Data updates**, **Enable automatic updates** lets CalAstro download
the latest Earth-orientation data (IERS) and leap-second list. Chrome asks for permission for
the two sites involved. Updates are checked weekly. Downloaded files are validated before use,
and the data packaged with the extension remains the fallback.

## Backup
**Back up settings** saves a JSON file; **Restore settings** loads one.
