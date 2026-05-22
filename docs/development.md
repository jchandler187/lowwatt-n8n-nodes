# n8n Nodes Development Guide

## Architecture

Each node is a separate npm package under `nodes/@lowwattlabs/`. All three share the same monorepo structure:

```
lowwatt-n8n-nodes/
├── README.md                    # This file (project overview)
├── LICENSE                      # MIT
├── package.json                 # Workspace root
├── docs/                        # Documentation
│   ├── architecture.md          # Node architecture decisions
│   ├── premium-features.md       # Free vs Premium tier breakdown
│   └── publishing.md            # npm publishing guide
├── scripts/                     # Build/helper scripts
│   ├── build-all.sh
│   ├── test-all.sh
│   └── link-local.sh
└── nodes/
    └── @lowwattlabs/
        ├── n8n-nodes-clamav/     # ClamAV node
        │   ├── package.json
        │   ├── tsconfig.json
        │   ├── src/
        │   │   ├── credentials/
        │   │   │   └── ClamavApi.credentials.ts
        │   │   └── nodes/
        │   │       └── Clamav/
        │   │           ├── Clamav.node.ts
        │   │           ├── ClamavTrigger.node.ts
        │   │           └── types/
        │   └── dist/             # Compiled output
        ├── n8n-nodes-uptime-kuma/ # Uptime Kuma node
        │   └── (same structure)
        └── n8n-nodes-calcom/      # Cal.com node
            └── (same structure)
```

## Development Workflow

1. Create a feature branch from `main`
2. Implement in `src/`, compile to `dist/`
3. Test locally by linking into n8n
4. Submit PR

## Testing Locally

```bash
# From the node's directory
cd nodes/@lowwattlabs/n8n-nodes-clamav
npm run build
npm link

# In your n8n installation
npm link @lowwattlabs/n8n-nodes-clamav
n8n start
```

## Publishing

See [docs/publishing.md](docs/publishing.md) for the full release process.

## Free vs Premium

See [docs/premium-features.md](docs/premium-features.md) for the feature matrix.

Free tier operations drive installs and adoption. Premium operations require a license key which is validated against our license server.