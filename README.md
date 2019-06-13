# Cloudflare Workers Types

**Install**

```bash
npm install --save-dev @cloudflare/workers-types
-- Or
yarn add -D @cloudflare/workers-types
```

**Usage**

Just supply an empty import in one of your source files to receive the workers types

```typescript
import {} from '@cloudflare/workers-types'
```

### Using a KV namespace

It's recommended that you create an ambient type file for your KV namespace bindings. Create a file named `types.d.ts` in your src directory:

**`types.d.ts`**

```typescript
import { KVNamespace } from '@cloudflare/workers-types'

declare global {
  const myKVNamespace: KVNamespace
}
```

Now `myKVNamespace` is available to all of your source files.
