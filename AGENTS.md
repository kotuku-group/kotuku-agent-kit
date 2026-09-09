# Repository guidance

- Skills are authored in this repository and must never be synchronized from the Kōtuku SDK.
- Treat `skills/tiri-programming/references/wiki/` as an ignored, on-demand cache refreshed by either skill's
  `scripts/fetch_reference.tiri` helper through `scripts/wiki_reference.tiri`.
- Treat `skills/tiri-programming/references/tiri-reference/` as an ignored, on-demand cache managed by the skill's
  `scripts/fetch_reference.tiri` helper.
- Treat `skills/kotuku-api/references/docs/` as an ignored, on-demand cache managed by the skill's
  `scripts/fetch_reference.tiri` helper.
- Keep skills concise and route detailed material through their `references/` directories.
- Run both the skill and plugin validators after changing skill or manifest metadata.
- Increment the plugin version for published changes. Downloaded caches record their own provenance.
- Use the `tiri-programming` skill before changing or testing the utilities under `scripts/`.
