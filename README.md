# @tradecrush/typescript-config

Shared TypeScript configurations for Tradecrush projects.

## Features

- Strict type checking
- Modern module resolution
- ES2022 language features
- JSX support
- Path aliases
- Optimized configurations for different project types
- Sensible defaults for code quality

## Installation

```bash
npm install --save-dev @tradecrush/typescript-config
```

## Requirements

- TypeScript 5.0.0 or higher

## Usage

### Next.js Projects

In your `tsconfig.json`:

```json
{
  "extends": "@tradecrush/typescript-config/configs/nextjs-ts-config.json",
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules"]
}
```

### Base Configuration

In your `tsconfig.json`:

```json
{
  "extends": "@tradecrush/typescript-config/configs/base-ts-config.json",
  "include": ["src/**/*.ts", "src/**/*.tsx"],
  "exclude": ["node_modules"]
}
```

## Extending Configurations

You can extend the base configurations to add your own settings:

```json
{
  "extends": "@tradecrush/typescript-config/configs/base-ts-config.json",
  "compilerOptions": {
    "outDir": "dist",
    "paths": {
      "@/*": ["./src/*"]
    }
  },
  "include": ["src/**/*.ts", "src/**/*.tsx"],
  "exclude": ["node_modules"]
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT