<!-- file: README.md -->
<!-- version: 1.0.0 -->
<!-- guid: 8581a6be-69ad-484b-9fc1-7de3ffc937d3 -->
<!-- last-edited: 2026-07-05 -->

# falkcorp/claude-plugins

Single Claude Code marketplace for every falkcorp plugin. Add this repo once
and every falkcorp plugin shows up grouped under one marketplace, instead of
adding each plugin's repo as its own separate marketplace.

## Usage

```
/plugin marketplace add falkcorp/claude-plugins
/plugin install plan-op@falkcorp
/plugin install audiobook-organizer@falkcorp
```

If you previously added `falkcorp/plan-op` or `falkcorp/audiobook-organizer`
directly as their own marketplaces, remove those first
(`/plugin marketplace remove plan-op`, `/plugin marketplace remove
audiobook-organizer`) to avoid listing the same plugin twice.

## Adding a new plugin

This repo holds no plugin code — it only lists plugins that live in their own
repos. To add one, append an entry to
[`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json) pointing
`source.url` at the plugin's repo (the repo's own `.claude-plugin/plugin.json`
is the actual manifest; this file just points at it). Plugins are floated on
their default branch — no version pinning here, so every install always pulls
latest.
