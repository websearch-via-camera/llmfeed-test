# LLMFeed Test Repository

This repository is a test setup for validating the [LLMFeed GitHub Action](https://github.com/kiarashplusplus/webmcp-tooling-suite/tree/main/packages/github-action) (`@25xcodes/llmfeed-action`).

## Purpose

This repo demonstrates how to:
- Set up an LLMFeed JSON file in the `.well-known/` directory
- Configure a GitHub Actions workflow to automatically validate the feed on every push

## Structure

```
.
├── .well-known/
│   └── mcp.llmfeed.json    # Sample unsigned LLMFeed
├── .github/
│   └── workflows/
│       └── validate-feed.yml   # Validation workflow
└── README.md
```

## Workflow

The GitHub Action automatically runs on:
- **Push**: When any `*.llmfeed.json` file is modified
- **Pull Request**: When any `*.llmfeed.json` file is modified

### Configuration

The workflow uses `skip-signature: 'true'` since this is a test feed without cryptographic signatures.

## License

MIT
