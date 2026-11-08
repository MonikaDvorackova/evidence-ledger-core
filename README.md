# Evidence Ledger Core

Rust CLI for an append-only evidence log. Records contain sequence, previous digest, hex-encoded event bytes, and SHA-256 digest. Every append verifies the existing chain first.

Run `cargo run -- append evidence.log "evaluation=passed"`, then `cargo run -- verify evidence.log`. Tamper with a byte and verification fails. Use as a local evidence primitive, not as a signed, timestamped, replicated ledger.
