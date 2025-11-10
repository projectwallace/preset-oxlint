# Oxlint preset

## Installation

```sh
npm i --save-dev oxlint @projectwallace/preset-oxlint
```

## Usage

In `package.json`:

```jsonc
{
  "scripts": {
    "lint": "oxlint --config .oxlintrc.json"
  }
}
```

Create an `.oxlintrc.json`:

```jsonc
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "extends": ["@projectwallace/preset-oxlint"],
	"env": [
		"node": true, // or false, but be explicit
		"browser": true, // or false, but be explicit
	],
	"rules": {}, // override what you need for the whole project
	"overrides": {} // override per file type, per folder, etc.
}
```
