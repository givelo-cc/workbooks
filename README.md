# Givelo Workbooks

Season workbooks for Givelo trade partners. Static site — no build step.

## Structure

```
index.html          Workbook directory (landing page)
2027/s1/index.html  Semester One 2027 workbook (self-contained, 8.6 MB)
```

## Adding a season

1. Export the workbook as a single self-contained HTML file.
2. Save it to `<year>/<semester>/index.html` — e.g. `2027/s2/index.html`.
3. Add a row to `index.html` pointing at the new path.

## Deploying

Any static host. Commit to the branch your hosting serves; each workbook is one
file with all images and scripts inlined, so it works offline and needs no
bundler, framework or asset pipeline.

## Notes

- Workbook files are large (~9 MB) because imagery is inlined. Git handles this
  fine, but consider Git LFS if the repo grows past a few seasons.
- Navigation inside each workbook is JavaScript-driven; serve over HTTP (not
  `file://`) for best results on mobile.
