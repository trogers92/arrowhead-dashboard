# Arrowhead dashboard (public viewer)

This repo hosts **only** the static dashboard viewer and an **AES-256-GCM
encrypted, sanitized** status snapshot of the Arrowhead Trading Engine.

* No source code, no trading logic.
* No brokerage account number, OAuth tokens, API keys, or the state key.
* Order / execution ids are truncated.

Without `DASHBOARD_PASSPHRASE` the snapshot is an opaque blob. Decryption
happens entirely in your browser (WebCrypto); the passphrase is never sent
anywhere. Updated automatically after each cloud trading/scan cycle.
