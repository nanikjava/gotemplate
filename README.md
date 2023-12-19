# VSCode Go Extension

Documentation for all the different configuration https://github.com/golang/vscode-go/wiki/settings#goformattool

# settings.json

The following uses the linter to format

```
{
 "editor.codeActionsOnSave": {
  "source.organizeImports": true,
  },
  "editor.formatOnSave": true,
  "go.testFlags": [
    "-failfast",
    "-v"
  ],
  "gopls": {
    "ui.semanticTokens": true
  },
  "go.lintOnSave": "file",
  "go.lintTool": "golangci-lint", 
  "go.lintFlags": [
    "--fix"
  ],
  "go.useLanguageServer": true,
  "[go]": {
    "editor.codeActionsOnSave": {
      "source.organizeImports": true
    }
  },
}

```

can also use `goimports` with `go.formatTool`

```
{
  ...
  "go.formatTool": "goimports",
  "go.formatFlags": [
    "-w"
  ],
  ...
}

````

from the doc

```
goimports: Organizes imports and formats the file with gofmt. (not applicable when the language server is enabled)
```
