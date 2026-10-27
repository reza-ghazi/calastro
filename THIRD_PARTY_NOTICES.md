# Third-party data and notices

CalAstro's runtime code is original or derived from the owner's Astrolibs library. It contains
no third-party runtime code. The extension bundles the following third-party **data**:

| Data | Source | Terms | Use in CalAstro |
|---|---|---|---|
| JPL planetary and lunar ephemerides DE442 (1549–2650) and DE441 (other years; parts 1 and 2), segments 3/0, 10/0, 301/3, 399/3, original coefficients | NASA JPL / NAIF, https://naif.jpl.nasa.gov/pub/naif/generic_kernels/spk/planets/ (de442.bsp, de441_part-1.bsp, de441_part-2.bsp) | Public release by NASA JPL; NAIF rules: https://naif.jpl.nasa.gov/naif/rules.html | Sun, Moon and Earth positions |
| Earth orientation parameters (finals2000A, Bulletin A) | IERS Rapid Service/Prediction Centre, via USNO (maia.usno.navy.mil) | Public IERS/USNO data products; acknowledgement: IERS | UT1−UTC and polar motion |
| Leap-second list | IERS, via IANA tzdb `leap-seconds.list` | Public domain (IANA tzdb) | UTC ↔ TAI |
| Place names, coordinates, elevations and time-zone identifiers | GeoNames (https://www.geonames.org), cities15000 and alternateNamesV2 | **CC BY 4.0**: "Place data © GeoNames" | City search |
| IAU 2000A nutation series coefficients | IERS Conventions (2010) / IAU SOFA tables, via Astrolibs | Published scientific constants | Earth orientation |
| ΔT model (Table S15) | Stephenson, Morrison & Hohenkerk (2016), Proc. R. Soc. A 472: 20160404, via Astrolibs | Published scientific data | Historical Earth rotation |

Time-zone rules come from the browser's built-in Intl (IANA tzdb) and are not bundled.

## Development-only tools (not shipped)
TypeScript, esbuild, Vitest, Playwright and ESLint are used under their open-source licenses.
Validation tooling uses spiceypy/CSPICE (NAIF), pyerfa (BSD-3; derived from IAU SOFA), GeographicLib (MIT), numpy,
JPL Horizons and the USNO Astronomical Applications API. None of these is included in the
extension.
