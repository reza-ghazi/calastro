# Validation summary

CalAstro is tested on every release against independent references. All figures are the
maximum differences measured.

| Area | Reference | Sample | Result |
|---|---|---|---|
| Ephemeris reader | NASA NAIF CSPICE on the full DE442 and DE441 kernels | 1117 epochs × 4 bodies, 10 BCE – 3007 CE, incl. record, chunk and hand-over boundaries | 3 × 10⁻⁸ km |
| Far-from-present apparent places | JPL Horizons (DE441), geocentric, TT | 8 epochs 1 CE – 3000 CE | Sun–Moon separation within 0.4 mas; absolute RA/Dec within 3.5″ (Horizons' IAU 1976/80 equinox frame) |
| Topocentric Sun and Moon az/el | CSPICE `azlcpo`, ITRF93 high-precision Earth orientation | 1000 epochs, 4 sites, 1985–2026 | 0.009″ |
| Leap seconds (TAI−UTC) | IAU SOFA `eraDat` | 1961–2029 | exact |
| TDB−TT | IAU SOFA `eraDtdb` | 1550–2650 | 7.8 µs |
| Precession and nutation | IAU SOFA / ERFA | 80 epochs 1550–2650 | ≤ 3.4 × 10⁻¹⁹ rad (nutation) |
| Sun and Moon rise, set, transit and civil twilight | US Naval Observatory one-day data | 18 site-days, 126 events, incl. polar day and night, the date line and DST | every time rounds to USNO's minute; polar states match |
| Solar Hijri year starts | University of Tehran Calendar Center | 1206–1498 SH (293 years) | 293/293 |
| March equinox moments | University of Tehran Calendar Center | 1377–1405 SH | ≤ 2 s |
| Tabular Islamic | Fourmilab Calendar Converter (Reingold & Dershowitz) | 8 anchor dates | exact |
| Umm al-Qura months | KACST official table | 1423–1450 AH | 335/336 |
| Yallop criterion | NAO Technical Note 69 worked example | — | q = 0.578, category A, exact |
| Odeh criterion | Odeh (2004) worked example | — | V ≈ −0.96, matches |
| Prayer times, İstanbul | Diyanet official timetable | 403 days | Fajr, sunrise, Dhuhr and Asr within ±1 min; Maghrib and Isha within ±2 min |
| Qibla (WGS84 geodesic) | GeographicLib 2.0 (Karney) | 627 cases | 9 × 10⁻¹⁰° |

**Physical limits:**
- Displayed times are rounded to the minute.
- Real atmospheric refraction can shift sunrise and sunset by more than a minute, and more
  near the poles.
- Crescent visibility depends on weather and observer.
- Dates far in the future carry growing uncertainty from Earth's rotation, which CalAstro
  reports.
