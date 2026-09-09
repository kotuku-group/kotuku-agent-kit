# Kōtuku API documentation

The generated XML documentation is downloaded on demand from the source declared in `kotuku-api-source.json`. The
same fetch command refreshes the shared wiki under `../../tiri-programming/references/wiki`. Both downloads record
their exact revisions in `.source.json` files within their cache directories.

- `docs/xml/modules/*.xml`: module-level functions, constants, structures, and concepts.
- `docs/xml/modules/classes/*.xml`: object classes, fields, actions, and methods.

Search recursively by the exact API identifier and read only the narrowest matching files.
