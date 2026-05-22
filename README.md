# ⚡ Low Watt Labs — n8n Community Nodes

Premium n8n community nodes built by Low Watt Labs. Each node provides a free tier for basic operations and a premium tier for advanced features.

## Nodes

| Node | Package | Free Tier | Premium |
|------|---------|-----------|---------|
| **ClamAV** | `@lowwattlabs/n8n-nodes-clamav` | Scan, List Signatures | Batch Scan, Real-time Monitor |
| **Uptime Kuma** | `@lowwattlabs/n8n-nodes-uptime-kuma` | Status Check, List Monitors | Create/Update Monitor, Push Metrics |
| **Cal.com** | `@lowwattlabs/n8n-nodes-calcom` | List Bookings, Get Booking | Create Booking, Cancel Booking, Webhooks |

## Why These Nodes?

The n8n community has 200K+ users but many requested integrations don't exist or the existing ones are broken/outdated:

- **ClamAV**: No n8n node existed for malware scanning. Zero competition.
- **Uptime Kuma**: Existing community node (v0.0.1) is broken — crashes on start, no auth support. Ours is a full rewrite with API v2 support.
- **Cal.com**: No n8n node existed for Cal.com's v2 API. Completely new integration.

## Monetization

- **Free**: Basic operations (list, get, check) — drives adoption
- **Premium**: $15/mo per node — batch operations, webhooks, custom fields, priority support
- **Bundle**: $39/mo for all three nodes with premium features

## Development Status

| Component | Status |
|-----------|--------|
| ClamAV node | In development |
| Uptime Kuma node | In development |
| Cal.com node | In development |
| Premium licensing system | Planned |
| npm publication | Planned |

## Building

```bash
# Install dependencies
npm install

# Build all nodes
npm run build

# Run tests
npm test

# Link locally for n8n testing
npm run link
```

## License

MIT — Free tier code is open source. Premium features require a license key.