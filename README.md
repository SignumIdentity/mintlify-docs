# Signum Documentation

Official documentation for the Signum Identity Platform, hosted on [Mintlify](https://mintlify.com).

## Overview

Signum is an enterprise-grade Federated Identity Provider that bridges verified identities across blockchain networks. This documentation covers:

- **Authentication**: OAuth2/OIDC flows, tokens, and scopes
- **Multi-Chain Identity**: Solana, EVM, and Canton Network integration
- **KYC & Compliance**: Verification flows and attestations
- **API Reference**: Complete REST API documentation

## Development

### Prerequisites

- Node.js 18+
- npm or bun

### Local Preview

```bash
# Install Mintlify CLI
npm install -g mintlify

# Start local preview
mintlify dev
```

The documentation will be available at `http://localhost:3000`.

### Syncing from App Repository

The docs are maintained in the `signum-app` repository under `docs/`. To sync:

```bash
# From signum-repos/
cp -r app/docs/* mintlify-docs/
```

### OpenAPI Spec

The API reference is auto-generated from the OpenAPI spec exported from the Elysia app:

```bash
# In signum-app repo with dev server running
bun run docs:export
```

This exports the spec to `docs/api/openapi.json`.

## Structure

```
├── docs.json           # Mintlify configuration
├── introduction.mdx    # Landing page
├── quickstart.mdx      # Getting started guide
├── architecture.mdx    # System architecture
├── authentication/     # Auth guides
├── chains/             # Multi-chain integration
├── kyc/                # KYC documentation
├── api-reference/      # API endpoint docs
├── api/                # OpenAPI spec
└── logo/               # Signum logos
```

## Deployment

This repo is connected to Mintlify for automatic deployments. Push to `main` to deploy.

## License

MIT
