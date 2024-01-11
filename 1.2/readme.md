# 1.2 - React Installation & Development Environment Setup

Required Application for React

1. Install [Node.js](https://nodejs.org) on a local PC 

2. React install by using [Vite](https://vitejs.dev/)
   ## React Install by Vite

```jsx
npm create-vite-app@latest foledername
npm install
npm run dev
```

### Setup Visual Studio Code

- **Setup Visual Studio**
    - Some code for VS Code `settings.json`
    
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
    
    - Some code for VS Code snippets as well:
    
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
    

The video for learning snippets is: https://www.youtube.com/watch?v=N-U6AVcIPy4

### Keyboard Shortcut

1. `code .`  for visualising root files in VS code.
2.  `Ctrl+,` for bring setting.
3. `Ctrl+Shift+p` for bringing Command Platte.
