MARIKINA CITY FIRE HYDRANT LOCATOR — EASY NAVIGATION VERSION

Source workbook: UPDATED HYDRANT STATUS MARIKINA CFS New(1).xlsx
Records imported: 255
Coordinates accepted for mapping: 232
Records needing coordinate review: 23
Operational as recorded in source: 230
Non-operational as recorded in source: 21
Status not recorded: 4

INTERFACE
- One search bar only, used for incident location and inventory search.
- Search a street/address/landmark/barangay, then nearby mappable hydrants are ranked by straight-line distance.
- Press Enter or click Search nearby hydrants.
- If online geocoding fails, use the same field to filter inventory or click the map to set the incident point.
- Clear resets the search and map.
- Custom SVG hydrant-shaped map markers indicate source status.

DATA AND SAFETY
- Coordinates are parsed from the workbook only; no missing coordinates are guessed.
- Only coordinates that parse and fall within broad Marikina-area bounds are mapped. Other rows remain in the inventory and coordinate_review.csv.
- Field verification is pending; source status is not independent proof of current physical condition. Confirm status with dispatch/field personnel before relying on a hydrant.
- Distances are straight-line estimates, not road routes or travel time.
- Map tiles and online address search require internet access.

PUBLISH
1. Download and extract this ZIP.
2. Open your GitHub repository: https://github.com/MarikinaCFS/marikina-hydrant-locator
3. Replace the existing index.html in the repository root with this package's index.html.
4. Commit the change. GitHub Pages will publish the update after its build completes.
5. Keep the CSVs and workbook as reference/support files; the webpage embeds its inventory and does not require fetching the CSV.
