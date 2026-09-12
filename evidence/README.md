# Evidence Register

Evidence files should make a defect easier to reproduce, not replace a clear written report.

## Naming convention

`BR-[number]/[short-description].[extension]`

Examples:

- `BR-001/cart-zero-quantity.png`
- `BR-002/stale-search-results.mp4`
- `BR-003/negative-page-response.json`

## Capture checklist

- Include the relevant application state and browser viewport.
- Record the build, environment and timestamp in the report.
- Crop unrelated desktop or account information.
- Remove passwords, tokens, cookies, personal data and internal URLs.
- Use screenshots for state and short videos for sequences.
- Keep request and response evidence as sanitized text when possible.
- Preserve original evidence; place retest evidence in a separate file.

The sample reports contain evidence capture instructions rather than fabricated screenshots. Actual files should be added only after the behaviour is reproduced and sensitive information is removed.
