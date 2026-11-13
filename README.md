# Alkady Breast Cancer Advisor — stage edition

Treatment decision support for metastatic breast cancer, designed for teaching and conference demonstration.
Patient criteria sit on the left, the treatment decision on the right; pressing a biomarker changes the decision immediately.

**Live pages**

| Subtype | Page |
|---|---|
| Landing page | https://drmohammadsabryelkady1-hub.github.io/alkady-advisor/ |
| HR+/HER2− | https://drmohammadsabryelkady1-hub.github.io/alkady-advisor/hr.html |
| HER2+ | https://drmohammadsabryelkady1-hub.github.io/alkady-advisor/her2.html |
| Triple-negative | https://drmohammadsabryelkady1-hub.github.io/alkady-advisor/tn.html |
| Atlas download: Gastric & Esophageal Cancer Management 2026 | https://drmohammadsabryelkady1-hub.github.io/alkady-advisor/ge-atlas.html |

## How a decision is built

1. **ECOG first.** Performance status sets the intensity: ECOG 0–1 shows the full evidence-ranked list; ECOG 2 shows de-escalated choices first; ECOG 3–4 makes best supportive care the recommendation.
2. **Best supportive care is always option 0.**
3. **Options ranked by evidence**, Level I first, with the NCCN category and ESMO 2026 updates on each card.
4. **Red flags travel with the drug**: HbA1c, QTc, prior ILD, LVEF, brain metastases and ECOG outside the trial population.
5. **Trial criteria one tap away**: each option opens its pivotal trial’s inclusion and exclusion criteria, checked against the patient.

## Sources

NCCN Clinical Practice Guidelines in Oncology, Breast Cancer v8.2026; ESMO metastatic breast cancer living guideline (2026) and ESMO Congress 2026 data; FDA prescribing information as of October 2026; pivotal-trial publications cited on each card.

## Publishing

GitHub Pages serves the site from the `gh-pages` branch (root folder). After changing a page on `main`, push the same commit to `gh-pages`:

```
git push origin main:gh-pages
```

The QR codes in the conference deck point to the four addresses above, so they keep working after every update.

## Atlas download page

`ge-atlas.html` is the page behind the download QR code of the atlas *Gastric & Esophageal Cancer Management 2026*
(3D illustrated edition, 43 pages). It offers the PDF `ge-atlas-2026.pdf`; the `ge-atlas-*.jpg` files are its cover and page previews.
To publish a new edition, replace `ge-atlas-2026.pdf` under the same name and push as described above: the QR code and the link stay valid.
The PDF is locked against editing; its source is kept privately by the author.

## Privacy

Each page is a single self-contained HTML file that runs in the browser. Nothing entered is stored or sent; the only network requests load fonts and the React library.

## Disclaimer

Decision support for clinicians. It does not replace the multidisciplinary team, clinical judgement or the prescribing information.

Designed & prepared by Prof. Dr. Mohammad Sabry Alkady · © 2026
