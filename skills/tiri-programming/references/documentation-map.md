# Tiri documentation map

The Tiri reference manual is downloaded on demand from the source declared in `tiri-reference-source.json`. The
focused wiki guides are refreshed by the same fetch command through the shared kit helper. Both downloads record
their exact revisions in `.source.json` files within their cache directories.

- `tiri-reference/index.adoc` and `tiri-reference/book.adoc`: reference manual entry points.
- `tiri-reference/ch*.adoc`: detailed language, runtime, tooling, and Origo chapters.
- `tiri-reference/appendix_*.adoc`: migration, operators, errors, reserved words, and standard-library summaries.
- `wiki/Tiri-*.md`: focused legacy API guides where the reference manual does not yet contain equivalent coverage.
- `../../kotuku-api/references/docs/xml/modules`: generated module and object API documentation.

Search by the exact construct or API name first. Read only the matching chapter and any directly linked prerequisite
material rather than loading the entire manual.
