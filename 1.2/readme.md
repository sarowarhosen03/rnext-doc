# 1.2 - React Installation & Development Environment Setup

Required Application for React

1. Node JS Insatll in local pc

[Node.js](https://nodejs.org)

1. Visual Stdio Code Install

[](https://code.visualstudio.com/)

1. Vite frontend tool

[Vite](https://vitejs.dev/)

Here is the code for the VS Code snippets as well.

```jsx
{
    "React component": {
        "prefix": "rfc",
        "body": [
            "export default function $1(){",
            "    return (",
            "        $2",
            "    );",
            "}"
        ],
        "description": "React functional component"
    }
}
```

VS Code Settings

```jsx
{
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": "explicit",
        "source.fixAll.tslint": "explicit",
        "source.organizeImports": "explicit"
    },
    "eslint.run": "onSave",
    "emmet.includeLanguages": {
        "javascript": "javascriptreact"
    },
    "path-autocomplete.extensionOnImport": true,
    "path-autocomplete.excludedItems": {
        "*/.js": {
            "when": "**"
        },
        "*/.jsx": {
            "when": "**"
        }
    },
    "javascript.validate.enable": false,
    "typescript.validate.enable": false
}
```

## React Install by Vite

```jsx
npm create-vite-app@latest foledername
npm install
npm run dev
```
