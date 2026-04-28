# te-fixture-iframe

Parent page that embeds an iframe carrying GTM. Parent itself has no GTM. Tests whether Discovery looks inside iframes.

**Live URL (parent):** `https://cpaynejz.github.io/te-fixture-iframe/`
**Live URL (embedded):** `https://cpaynejz.github.io/te-fixture-iframe/embedded.html`

## Test plan scenarios served

- TC-3.1.5 site loads GTM in an iframe — documents detection behavior

## How to configure

Paste the GTM snippet into `embedded.html` (NOT `index.html`). Commit and push.

## Expected vs likely-actual behavior

- Run Discovery against the parent URL: should report no GTM evidence (Discovery does not enumerate iframe documents).
- Run Discovery against the embedded URL directly: should detect GTM normally — useful as a sanity check that the snippet is correct.

This fixture documents a Discovery limitation rather than a happy path. Capture both findings.
