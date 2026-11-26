# Repository audit

Audit date: 2026-11-26.

## Original structure

```text
PYQ/
  .git/
  7 CAO PDFs
  PYQs/ (nested Git checkout, tracked as a gitlink)
    .git/
    CAO/ (7 PDFs)
    DBMS/ (10 PDFs)
    TOC/ (10 PDFs, 2 saved HTML pages)
```

## Findings and preservation

- Inspected all 36 non-Git resource files: 34 PDFs and 2 HTML pages; 29 unique SHA-256 hashes.
- Seven duplicate groups, 14 participating files, 7 extra copies (715,251 bytes). No files deleted.
- All duplicates are root CAO papers paired with their nested CAO copies. Canonical copies now sit directly in CAO/year; retained duplicates sit in Additional-Copies.
- Similar TOC filenames with different course/branch names have distinct hashes and remain separate.
- Two HTML downloads are source webpages, not PDF papers. Preserved with honest, shorter source-page.html names. Their external assets and embedded papers may require internet access.
- No zero-byte files, temporary downloads, unrelated resources, images, or office documents found. Original subject directories were nonempty.
- All PDFs parsed with pdftotext without errors. Many are scans with no useful extracted text; full visual legibility and completeness are not certified.
- Subject, semester and year organization uses existing folders and filenames. CAO includes one combined architecture/operating-systems paper; retained in its existing subject context.
- Initial main and fetched origin/main both pointed to a6a3867; their histories already include the remote upload and merge. No active merge was present.
- Nested checkout had seven tracked deletions and untracked subject folders. All working resources were preserved. Its Git metadata is backed up locally under the outer .git/nested-PYQs-backup directory; the broken gitlink is replaced with ordinary tracked resources.

## Change manifest

See [resource inventory](resource-inventory.csv) for every original path, final path, byte size and SHA-256. See [duplicate report](duplicates.csv) for every member of each duplicate group.

## Validation

All 36 original resource instances must match their recorded final hashes and sizes. README local links, filenames, path lengths, final hierarchy and staged changes were checked before commit. No global Git or credential configuration was changed.
