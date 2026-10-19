# id.chrisheuer.com

The [AAuth](https://github.com/dickhardt/AAuth) agent provider for AI agents that act for Chris Heuer, built with the AIOS.

Served by GitHub Pages at `https://id.chrisheuer.com`:

- `/.well-known/aauth-agent.json`: agent provider metadata
- `/.well-known/jwks.json`: the public key that signs agent tokens

Identifiers like `aauth:bob@id.chrisheuer.com` name software agents, not people.

## Security

- **Public keys only.** No private key is ever in this repository. The signing key is in a device's Secure Enclave and can't leave it.
- **Who can publish keys controls the agents.** Changes to `.well-known/` are reviewed by Chris before they're pushed.
- **Key rotation.** Add the new key, keep the old one until outstanding tokens expire (24 hours at most), then remove it.
- **Report a problem:** open an issue, or contact Chris Heuer.
