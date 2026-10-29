MARIKINA FIRE HYDRANT LOCATOR — UPDATED PACKAGE

Contents:
- index.html: updated GitHub Pages application with the latest workbook inventory embedded
- hydrant_inventory.csv: all 255 source inventory records
- coordinate_review.csv: records not plotted because coordinate values are missing, malformed, or outside the Marikina validation bounds
- source_workbook.xlsx: original uploaded inventory workbook

Update steps:
1. Download and extract this ZIP.
2. In your GitHub repository marikinacfs/marikina-hydrant-locator, replace the existing root index.html with this package's index.html.
3. Commit the change to the branch/folder used by GitHub Pages.
4. After deployment, refresh the website with Ctrl+F5 (or clear cache) to avoid an older cached page.
5. For a quick visual check, search a location and verify the marker shapes; search/filter for JUAN LUNA ST. COR TANDANG SORA ST. in the embedded inventory.

Data caveats:
- The workbook has 255 address records. This build accepted 233 coordinate pairs for mapping; 22 are in coordinate_review.csv.
- Coordinates are parsed from the workbook, including DMS formats. Coordinate acceptance is a syntax/range check, not independent field verification.
- Status labels reflect the spreadsheet only. The website does not establish current physical hydrant condition.
- Nearby ordering uses straight-line distance, not road routing.
- Online map tiles and geocoding require internet connectivity.
