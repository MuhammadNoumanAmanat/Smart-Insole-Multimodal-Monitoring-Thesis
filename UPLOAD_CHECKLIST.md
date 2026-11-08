# Publication checklist and file layout

This repository documents a jointly authored bachelor’s thesis. Do not publish confidential research data, identifiable participant records, or unapproved documents.

## Suggested repository structure

```text
.
├── README.md
├── .gitignore
├── docs/
│   ├── bachelors_thesis.pdf
│   └── thesis_poster.pdf
├── images/
│   ├── prototype-overview.jpg
│   ├── electronics-assembly.jpg
│   ├── confusion-matrix.png
│   └── training-accuracy.png
├── src/
│   ├── python/
│   ├── matlab/
│   └── embedded/
└── hardware/
    ├── stl/
    └── cad/
```

Only add directories for materials you are actually publishing. The names above are recommended destinations, **not** files that already exist.

## Priority 1 — thesis and poster

1. Ask the supervisor or university whether the full final thesis and poster may be released publicly. Confirm that the PDF is the **approved final dissertation**, not an earlier proposal.
2. Inspect the PDF for editing placeholders, signatures, student IDs, private participant information, and third-party material that should not be republished.
3. Upload the authorized thesis as `docs/bachelors_thesis.pdf` and the poster as `docs/thesis_poster.pdf` using GitHub **Add file → Upload files**.
4. After upload, change the repository README status from “Pending” to links pointing to those files. Verify the PDF opens in a private browsing window.
5. For university forms asking for a thesis document, use the direct file link, not just the repository homepage. Follow any university rules requiring an institutional upload or official document.

## Priority 2 — project evidence

- Select 2–4 clear photos of the prototype and enclosure from `FYP_Results`. Avoid faces or get explicit consent.
- Add the confusion matrix, accuracy plot, and sensor visualization, with captions, source/evaluation details and labels.
- Upload select demo recordings **only if** the individuals shown consented to public release.
- Where applicable, include STL files and CAD export previews rather than every working version and temporary artifact.

## Priority 3 — source code and reproducibility

- Review `train_model.py`, `predict_user_input.py`, `predict_from_serial.py`, `requirements.txt`, and relevant MATLAB / embedded files.
- Remove passwords, API keys, absolute local file paths, participant metadata and identifiable data.
- Add a simple run guide: environment, input schema, training command, inference command, tested versions, and model provenance.
- Avoid uploading `*.pyc`, large redundant `*.h5` checkpoints, personal CSV collections or unreviewed binaries.
- Document evaluation split methodology and class definitions. Avoid claiming clinical effectiveness.

## Publication notes

- Link the IEEE INMIC paper to its DOI: https://doi.org/10.1109/INMIC65900.2025.11348422. Do not upload the publisher-formatted PDF unless you have distribution rights.
- Credit both authors and supervisors.
- **No open-source license** is appropriate until rights and permissions are settled. Without a license, visitors generally cannot reuse the repository content under an open-source grant.
