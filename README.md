# GS1 / FO Barcode Scanner Validation Utility

This repository contains a lightweight, production-quality standalone utility for validating barcode scanner behavior before a Dynamics 365 FO GS1 pilot.

## Main deliverable

- `barcode_scanner_test_page_pro.html` (single self-contained HTML file, no backend, no frameworks)

## How to run locally

1. Download or clone this repository.
2. Open `barcode_scanner_test_page_pro.html` in a modern browser (Chrome, Edge, or Firefox).
3. Click into the **Live Scanner Capture** box (it auto-focuses on load).
4. Scan using your scanner in keyboard-wedge mode.

## What the page validates

- Raw scanner output behavior
- AIM/symbology prefixes (`]C1`, `]d2`, `]Q3`)
- Group separator handling (ASCII 29 / `~` mapping)
- GS1 AI parsing for: `01`, `17`, `10`, `21`, `30`, `37`
- FO-oriented suitability verdict:
  - Suitable
  - Suitable with configuration
  - Not suitable

## Additional features

- Built-in realistic sample scans (good + malformed)
- Character-level inspection table (index, char, code, meaning)
- Session log and export (TXT, JSON)
- Integrated scanner type + popular device family guidance with cautious wording for pilot planning

## Important note

This utility supports practical pre-pilot diagnostics. Final suitability should always be verified in real Dynamics 365 FO test scenarios with the intended scanner configuration profile.
