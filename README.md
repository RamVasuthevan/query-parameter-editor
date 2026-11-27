# URL Query Parameter Editor

A single-page tool for editing a URL's parameters as tables. Open `index.html` in a browser; there's no build step or dependencies.

1. Paste a URL. It's split into a base URL (scheme, credentials, host and path), its query parameters (after `?`) and its fragment parameters (after `#`).
2. Edit, add or remove parameters in either section, or change the base URL. Untick a row's **On** box to leave it out of the URL without deleting it; tick it again to put it back. The URL field and the output update as you type.
3. Copy the result.

Single-page apps often keep their state in the fragment, e.g. `#company=Affirm&location=Toronto`. Hash-router URLs like `#/jobs?company=Affirm` work too: `/jobs` goes in the fragment section's "Route or anchor" field and `company` in its table. A plain anchor such as `#section` also lives in that field.

Parameters you don't touch keep their order, duplicates, valueless keys like `?flag` and existing encoding. The browser's URL parser normalizes a few characters when you paste (for example a literal space becomes `%20`), so those come out in that normalized form. A parameter you edit is re-encoded with `encodeURIComponent`. In the editor, `+` is shown as a space.
