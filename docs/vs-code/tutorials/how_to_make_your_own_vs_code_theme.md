<!-- markdownlint-disable MD026 -->

# How to make your own VS Code theme!

<!-- markdownlint-enable MD026 -->

> **Source**: Coder Coder's "[How to make your own VS Code theme!](https://youtu.be/pGzssFNtWXw)" tutorial.

- Two color categories:
  - Application colors.
  - Token colors (syntax highlighting).
- [VS Code Extension generator](https://www.npmjs.com/package/generator-code) (CLI).
- Preview and debug:
  - `Run` > `Start Debugging`.
  - `View` > `Command Palette...` > `Developer: Inspect Editor Tokens and Scopes` (just for syntax highlighting).
- [Documentation](https://code.visualstudio.com/api/references/theme-color).
- The `publish` field in the `package.json` file must match the publisher ID (Visual Studio Code Marketplace).
- `vsce`:
  - CLI for packaging, publishing, and managing VS Code extensions.
  - `npm install -g vsce`.
- [VS Code Theme Color Generator](https://coder-coder.com/vs-code-theme-color-generator/).
