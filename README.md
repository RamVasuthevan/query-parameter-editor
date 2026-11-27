# URL Query Parameter Editor

A single-page tool for editing a URL's query parameters as a table. Open `index.html` in a browser; there's no build step or dependencies.

1. Paste a URL. Its base (scheme, credentials, host, path and `#fragment`) and its query parameters are split out.
2. Edit, add or remove parameters, or change the base URL. The pasted URL field and the output update as you type.
3. Copy the result.

Parameters you don't touch are kept byte-for-byte as they were in the original URL, including their order, duplicates, valueless keys like `?flag` and existing encoding. A parameter you edit is re-encoded with `encodeURIComponent`. In the editor, `+` is shown as a space.
