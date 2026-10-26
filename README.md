# Muse System Files Reference

A generic reference to the folder hierarchy in a Muse instance's
System Files area, and what each folder and file is for.

This page is generic. It describes the standard folders and files any
Muse user may see, at pattern level for repeating folders. It does
not name any real person, group, project, goal, or chat, and it does
not contain any one user's file contents.

## How to use it

Open `index.html` in a browser. No server, database, or other
technology is required. The page is a single HTML file with all CSS
and JavaScript inline, and it makes no external requests.

- Search across paths, purposes, and expected contents.
- Filter by edit tier.
- Expand or collapse folders.
- Print with the browser's Print command; the print stylesheet
  expands all entries, with tier badges readable in black and white.

## Edit tiers

Every entry carries a tier badge, with colour plus shape plus text,
never colour alone:

- **Editable** — green, filled circle. You are the intended author
  or owner.
- **Edit via Muse** — amber, half-filled circle. Muse maintains the
  file; give corrections in conversation so they can be reconciled
  with background jobs and other records.
- **Do not edit** — red, filled square. Runtime-managed, generated,
  system-provided, or private. Hand-editing risks breaking a job,
  losing state, or exposing a secret.

A separate flag marks entries that are filesystem-only or that only
appear once the corresponding feature has been used.

## A note on scope

Your tree may be a subset of this reference. Folders appear as
features are used, and runtime folders may vary by deployment.
This reference is a snapshot, dated in the page itself, not a live
view of any one Muse instance.
