# Marikina Fire Hydrant Locator — Prototype v2

## What is included
- `index.html`: responsive browser-based locator with street/barangay/address search, map click incident placement, GPS option, distance ranking, and Google Maps directions.
- `hydrants.json`: extracted inventory data for review/integration.
- `coordinate_review.csv`: source rows that need coordinate correction before they can be mapped.
- `inventory_review.xlsx`: cleaned review copy with parsed coordinates and data-quality flags.

## Important operational limitations
- The source workbook is labeled “Consolidated Status of Fire Hydrant — as of September 2026.”
- This prototype has not independently verified any hydrant in the field. Every imported record is marked `Pending field verification`.
- Strict mode only returns records with an authorized `Verified` flag. As none are independently verified in this prototype, strict mode intentionally returns zero results.
- “Planning preview” displays only records the spreadsheet lists as operational and whose coordinates passed validation. These are explicitly marked planning-only and must not be treated as confirmed available water sources.
- 37 of the 255 address records have missing or invalid coordinates and are omitted from the map. See `coordinate_review.csv`.
- The file has no shared database, user accounts, audit log, or cross-device syncing. Changes in a browser do not sync to other computers.
- Search uses the free OpenStreetMap Nominatim geocoder and OpenStreetMap map tiles; internet access is required and the geocoder has usage limits. Do not use it for bulk geocoding. Attribution and service policies apply.
- Distances are straight-line distances, not drive times or road routes. Confirm road access, condition, pressure/flow, and actual availability on scene.

## Test locally
1. Extract the ZIP file.
2. Open `index.html` in a modern browser while connected to the internet.
3. Enter a street name, landmark, or barangay and select **Find nearest hydrants**.
4. Confirm the incident pin is actually at the fire scene.
5. Strict mode starts with no verified results. Select **Planning preview** to inspect source-listed operational records, with warnings.
6. Use the map click or GPS control as an alternative to text search.

Some browsers restrict network requests from local files. If geocoding fails, use the map-click option or publish the static files to a free HTTPS static host.

## Recommended free deployment
- For a static pilot, publish `index.html` through GitHub Pages. The inventory is embedded in the HTML, so the prototype can be served as a static website.
- This is not yet suitable as a shared operational dispatch system. For shared edits and authoritative verification, use a managed database with authentication, role-based permissions, audit logging, backups, and a tested update procedure. A free database tier may have usage/inactivity limits.
- Do not put sensitive incident details or private credentials in this static prototype.

## Source data quality summary
- 255 address records extracted.
- 218 records have coordinates that parse and fall within a broad Marikina plausibility range.
- 230 rows are marked operational in the spreadsheet; 199 of these have valid coordinates.
- 21 records are marked unavailable or have issue remarks.
- 4 records have unclear status.
- All 255 records are pending independent field verification in this prototype.
