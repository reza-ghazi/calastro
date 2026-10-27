# Release notes

## 1.0.0 — unreleased
First public release.
- Calendar conversion:
  - Gregorian and Julian, 999,999 BCE – 999,999 CE;
  - astronomical Solar Hijri and Shahanshahi;
  - tabular Islamic (types I–IV), including years before the Hijra (BH);
  - predicted Islamic (Umm al-Qura rule; Yallop or Odeh crescent visibility).
- Sun and Moon:
  - rise, set, transit and the three twilights for the local day, with polar states;
  - Moon phase and age.
- Prayer times: 18 source-documented methods and the WGS84 Qibla bearing.
- English and Persian with right-to-left layout and a choice of numerals; light and dark
  themes.
- Convert has a **Today** button that resets the form to today's date.
- Every date shows its weekday in the calendar's own names (e.g. Yekshanbeh for Solar Hijri,
  al-Ahad for Islamic); years are calendrical, with no year zero (1 BCE is followed by 1 CE).
- JPL DE442/DE441 ephemeris for 1 CE – 3000 CE, downloaded once on first use (about 223 MB,
  checksum-verified), then everything works offline. Optional updates of Earth-orientation
  and leap-second data.
