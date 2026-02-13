# Ever Gauzy TypeScript SDK

Official TypeScript SDK for the [Ever Gauzy](https://gauzy.co) API, auto-generated using [Microsoft Kiota](https://learn.microsoft.com/en-us/openapi/kiota/).

## Installation

```bash
npm install @ever-co/ever-gauzy-sdk
```

## Quick Start

```typescript
import { EverGauzyApiClient } from '@ever-co/ever-gauzy-sdk';
import { FetchRequestAdapter } from '@microsoft/kiota-http-fetchlibrary';
import { AnonymousAuthenticationProvider } from '@microsoft/kiota-abstractions';

// Create the API client
const authProvider = new AnonymousAuthenticationProvider();
const adapter = new FetchRequestAdapter(authProvider);
adapter.baseUrl = 'https://api.gauzy.co';

const client = new EverGauzyApiClient(adapter);

// Example: List employees
const employees = await client.api.employee.get();
console.log(employees);
```

## Authentication

The Gauzy API supports multiple authentication methods:

- **Bearer Token (JWT)**: For user-authenticated requests
- **API Key**: Via `X-API-Key` header
- **OAuth2**: Authorization code flow

## API Documentation

- **Swagger UI**: https://api.gauzy.co/swg
- **Scalar Docs**: https://api.gauzy.co/docs
- **OpenAPI Spec**: https://api.gauzy.co/swg-json

## Development

```bash
git clone https://github.com/ever-co/ever-gauzy-sdk-typescript.git
cd ever-gauzy-sdk-typescript
npm install
npm run build
npm test
```

## SDK Generation

This SDK is auto-generated from the Ever Gauzy OpenAPI specification using Microsoft Kiota.
To regenerate, trigger the "Generate SDK" GitHub Action workflow.

## License

This SDK is licensed under the [MIT](LICENSE) license.

## Links

- [Ever Gauzy](https://gauzy.co)
- [API Documentation](https://docs.gauzy.co)
- [GitHub](https://github.com/ever-co/ever-gauzy)
