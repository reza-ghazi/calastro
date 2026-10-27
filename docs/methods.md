# Methods

CalAstro computes everything on your device. The JPL ephemeris data (about 223 MB) is downloaded
once on first use from this project's website and checked against SHA-256 checksums packaged with
the extension; all other data is packaged.

## Ephemeris and reference frames
- **Positions:** original Chebyshev coefficients for the Sun, the Earth–Moon barycentre, the
  Moon and the Earth.
  - JPL DE442 from 1549-12-31 to 2650-01-25; JPL DE441 for other years.
  - The bundled data spans about 10 BCE – 3007 CE; the features cover 1 CE – 3000 CE.
  - At the two hand-overs the Moon steps by at most 0.38″ (DE441 vs DE442).
- **Far-from-present dates:** positions stay accurate (DE441), but local clock times inherit
  the uncertainty of Earth's rotation (ΔT), about ±4 min at 1 CE and ±30 min at 3000 CE (1σ).
  CalAstro shows a note when this exceeds a minute.
- **Apparent places:**
  - light time;
  - solar gravitational light deflection (not applied to the Sun itself);
  - relativistic aberration;
  - IAU 2000 frame bias;
  - IAU 2006 precession and IAU 2006/2000A nutation;
  - Greenwich apparent sidereal time including the IERS 2010 complementary terms;
  - IERS polar motion.
- **Observer:** a point on the WGS84 ellipsoid at the given height.

## Time
- **UTC** follows the IERS leap-second list. Before 1961, civil time is treated as UT.
- **UT1** comes from IERS Earth-orientation data (finals2000A) where available.
- **ΔT** outside that data:
  - earlier dates: Stephenson, Morrison & Hohenkerk (2016), joined continuously to the IERS
    values;
  - later dates: extrapolated with stated uncertainty (Morrison & Stephenson 2004 historically,
    Huber 2000 for the future).

## Rise, set, transit and twilight
- **Sunrise and sunset:** the Sun's upper limb on the horizon with 34′ of standard refraction,
  i.e. its centre at −0°50′. The horizon is at sea level.
- **Moonrise and moonset:** the Moon's upper limb at −34′, i.e. its centre at −34′ minus the
  Moon's topocentric semidiameter.
- **Twilight:** the Sun's centre at −6° (civil), −12° (nautical) or −18° (astronomical).
- **Meridian transit:** the topocentric apparent hour angle equals zero.
- Events are searched within the local civil day. Polar days and nights are reported as
  states.

## Moon phase
- All quantities are geocentric.
- **Illuminated fraction:** k = (1 + cos i)/2, where i is the Sun–Moon–Earth angle at the
  Moon.
- **Waxing:** the Moon's apparent ecliptic longitude minus the Sun's is less than 180°.
- **Named phases:** eight 45° bins of that difference.
- **Lunar age:** time since the last geocentric conjunction in ecliptic longitude.

## Calendars
- **Gregorian and Julian:** proleptic, with exact integer arithmetic, from 999,999 BCE to
  999,999 CE.
  - Years are shown and entered as in each calendar, with no year zero: 1 BCE is followed by
    1 CE, and 1 BH by 1 AH (or 1 SH).
  - Julian calendar dates are different from Julian Day Numbers.
- **Solar Hijri (astronomical):**
  - The year starts on the day of the March equinox if the equinox occurs before true
    (apparent) solar noon on the 52.5°E meridian; otherwise it starts on the next day. This is
    the University of Tehran Calendar Center rule.
  - Days are counted in Iran Standard Time.
  - Leap years follow from consecutive year starts.
  - When the equinox is within three standard deviations of the ΔT uncertainty from noon, the
    year start is marked as undecidable.
- **Shahanshahi (Imperial):** Solar Hijri months and days with year + 1180, in official use
  from 1355 to 1357 SH.
- **Tabular Islamic:** 30-year cycles of van Gent's types I–IV, with the Friday (civil) or
  Thursday (astronomical) epoch of 1 Muharram AH 1.
  - Years before AH 1 are counted BH (before Hijra), proleptically.
  - Days are counted from midnight; the religious day begins at sunset.
- **Predicted Islamic:**
  - **Umm al-Qura rule (default):** at Makkah on the 29th, if the conjunction precedes sunset
    and the Moon sets after the Sun, the next day begins the month.
  - **Crescent visibility:** the Yallop (1997) or Odeh (2004) criterion at Makkah or at your
    location, evaluated at the best time (sunset + 4/9 of the lag).
  - Months not begun by the third evening complete 30 days.
  - These are calculations, not announcements.

## Prayer times
- **Fajr and Isha:** solar depression angles or intervals, per the chosen authority.
- **Dhuhr:** follows the solar transit, plus any offset the authority specifies.
- **Asr:** shadow length = noon shadow + 1 × (or, Hanafi, 2 ×) the object's height.
- **Maghrib:** sunset, or a depression angle for Shia methods.
- **Midnight:** halfway from sunset to sunrise, or to Fajr in the Jaʿfari convention.
- **High latitudes:** the middle-of-night, one-seventh and angle-based rules act as limits and
  are marked when used.
- **Sources:** each method lists its sources and their quality.

## Data sources
- JPL/NAIF DE442.
- IERS Bulletin A via USNO.
- The IERS leap-second list via IANA.
- GeographicLib-equivalent WGS84 geodesics (CalAstro's own implementation).
- GeoNames place data (CC BY 4.0).
- Methods and constants from the IAU SOFA/IERS Conventions, the University of Tehran Calendar
  Center, NAO Technical Note 69 (Yallop) and Odeh (2004).
