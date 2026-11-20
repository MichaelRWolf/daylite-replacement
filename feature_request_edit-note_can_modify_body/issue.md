# Feature request: edit note body via MCP

## Summary

The Daylite Local MCP Server can read a note's body (the `details` field) but cannot set it. `create-note` and `edit-note` have no writable `details` input, so a note created through MCP is always created without body text.

## Requested change

- Add a writable `details` input to `create-note`.
- Add a writable `details` input to `edit-note`.

## Current workaround

Create the note through MCP, then add the body by hand in Daylite.

## Context

- Source: Daylite support ticket, closed by Daylite support (Muhaimin, The Daylite Team), 2026-11-20.
- Support confirmed the gap and said note content is the main reason to create a note, so a writable `details` input makes sense.
- The Local MCP Server is in Early Access. Support asked that the request be posted to the Daylite community: https://community.daylite.app/
- Support said the write-up can be pasted into the community post as is.

## Impact

- The `conference-followup` skill (`~/repos/claude-tools/skills/conference-followup/SKILL.md`, step 6) creates one `<event> notes` Daylite note per person through `create-note`. Each note is created empty and its body must be added by hand in Daylite until this request ships.
- Once `details` is writable, step 6 can write the notes text directly and the skill's manual step goes away.

## Status

- [ ] Post to Daylite community
