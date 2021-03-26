# Visual Studio (VS) Code

## Extensions

Kevin Powell's "[VS Code extensions that I can't live without!](https://youtu.be/plEwInSiqgw)" video:

- [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2).
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) (matches a start tag with its end tag in HTML, for example).
- [SVG Previewer](https://marketplace.visualstudio.com/items?itemName=vitaliymaz.vscode-svg-previewer).

## Themes

Coder Coder's "[How to make your own VS Code theme!](https://youtu.be/pGzssFNtWXw)" tutorial:

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
