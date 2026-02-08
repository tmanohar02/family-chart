# Local CSV Demo

This demo renders a family chart from the CSV files in `data/templates/`.

## Regenerate data

```
node ../../scripts/csv-to-family-chart.mjs
```

This writes `data/derived/family-chart-data.json`.

## Encrypt data

```
node ../../scripts/encrypt-family-data.mjs <passphrase>
```

This writes `data.enc.json` in this folder. The demo no longer ships plaintext data.

## Run locally

Serve the repo over HTTP:

```
python3 -m http.server 8000
```

Then open:

```
http://localhost:8000/family-chart/examples/local-csv-demo/
```

Note: The demo currently loads the library and CSS from the unpkg CDN. If you want to use a local build instead, run `npm install && npm run build` in `family-chart/` and update `index.html` to point to `../dist/family-chart.esm.js` and `../dist/styles/family-chart.css`.
