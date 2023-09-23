# Vite config + Native ESM + TypeScript = Bug

```ts
import react from '@vitejs/plugin-react'
import { defineConfig } from 'vite'

export default defineConfig({
	plugins: [
		react(), // <-- typescript error here
	],
})
```

The error is:

```
This expression is not callable.
  Type 'typeof import("/Users/kentcdodds/Desktop/vite-plugin-react-types-issue/node_modules/@vitejs/plugin-react/dist/index")' has no call signatures.
```

Note the use of `"type": "module"` in the package.json