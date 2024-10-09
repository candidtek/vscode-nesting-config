<h1>File Nesting Config<sup><em> for VS Code</em></sup></h1>

![](https://user-images.githubusercontent.com/11247099/157142238-b00deecb-8d56-424f-9b20-ef6a6f5ddf99.png)

> Requires VS Code v1.67

This is a config snippet making your file tree cleaner with the [file nesting feature](https://code.visualstudio.com/updates/v1_67#_explorer-file-nesting) of VS Code.

## Use it

### VS Code Extension

We now have a new VS Code extension to handle the updates automatically for you.

[Check the readme for instructions](https://github.com/antfu/vscode-file-nesting-config/tree/main/extension).

### Update Manually

Open your VS Code, bring up your `settings.json`, copy-n-paste the snippet below, and you are good to go :)

<!-- eslint-skip -->

```jsonc
  // updated 2024-09-09 00:23
  // https://github.com/candidtek/vscode-nesting-config
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.expand": false,
  "explorer.fileNesting.patterns": {
    ".gitignore": ".gitattributes, .gitmodules, .easignore",
    "package.json": ".npmrc, .nvmrc, .ncurc.json, pnpm-workspace.yaml, turbo.json",
    ".prettierrc.*": ".prettierignore",
    "eslint.config.*": "eslint.rules.json, eslint.abbrs.json",
    "jest.config.*": ".jestignore",
    "tsconfig.json": "tsconfig.*.json, tsconfig-*.json, tsup.config.*",
    "README.md": "todo.txt, CODEOWNERS, typedoc.json",
	".env": ".env.*, env.js",
	"app.config.*": "babel.config.*, metro.config.*, eas.json, eas-setup.cmd, tailwind.config.js"
  },
```

## License

MIT
