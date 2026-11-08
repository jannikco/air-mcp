# Air MCP setup and connection checker

Generate Air MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect air

[Create or sign in to PipMCP](https://pipmcp.com/register?app=air&utm_source=github&utm_campaign=github-air-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=air&utm_source=github&utm_campaign=github-air-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: 78258f9abc61745d740f9f1a5f9f4d296bf0a959380415d93ef87664fef8faee. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "custom_headers",
  "requiredCredentialFields": [
    "provider_header_credentials"
  ],
  "requiredHeaderNames": [
    "x-api-key",
    "x-air-workspace-id"
  ],
  "helpUrl": "https://developer.air.inc/docs/getting-started",
  "tenantRequired": false,
  "accountParameterNames": []
}
```

Provider documentation: https://developer.air.inc/llms.txt
Provider website: https://air.inc/
