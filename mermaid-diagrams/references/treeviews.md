# TreeViews

TreeViews represent hierarchical data in the form of a directory-like structure, using indentation to indicate nesting levels. They're ideal for file systems, org charts, and nested categories.

## Basic Syntax

```mermaid
treeView-beta
    "src"
        "components"
            "Button.tsx"
            "Card.tsx"
        "utils"
            "helpers.ts"
    "package.json"
    "README.md"
```

## Directory Structure

### Simple Project

```mermaid
treeView-beta
    "my-project"
        "src"
            "components"
            "hooks"
            "styles"
        "public"
        "tests"
        "package.json"
        "README.md"
```

### Deep Nesting

```mermaid
treeView-beta
    "root"
        "level-1"
            "level-2"
                "level-3"
                    "file.txt"
```

## File Organization

### Monorepo Structure

```mermaid
treeView-beta
    "monorepo"
        "apps"
            "web-app"
                "src"
                "package.json"
            "mobile-app"
                "src"
                "package.json"
            "admin-panel"
                "src"
                "package.json"
        "packages"
            "ui-library"
                "src"
                "package.json"
            "shared-utils"
                "src"
                "package.json"
            "api-client"
                "src"
                "package.json"
        "tools"
            "build-scripts"
        "package.json"
        "turbo.json"
```

## Comprehensive Example

```mermaid
treeView-beta
    "project-root"
        "src"
            "assets"
                "images"
                "fonts"
                "styles"
            "components"
                "common"
                    "Button"
                    "Input"
                    "Modal"
                "layout"
                    "Header"
                    "Sidebar"
                    "Footer"
                "features"
                    "UserProfile"
                    "Dashboard"
            "hooks"
                "useAuth"
                "useApi"
            "pages"
                "Home"
                "About"
                "Contact"
            "services"
                "api"
                "auth"
            "store"
                "slices"
                "middleware"
            "types"
            "utils"
        "tests"
            "unit"
            "e2e"
        "docs"
        "scripts"
        ".github"
            "workflows"
        ".vscode"
        "package.json"
        "tsconfig.json"
        "README.md"
```

## Best Practices

1. **Use clear names** - Files and folders should be self-documenting
2. **Group logically** - Organize by function or feature
3. **Limit depth** - Too many levels make navigation hard
4. **Use consistent structure** - Follow project conventions
5. **Show key files** - Include important configuration files

## Common Use Cases

- Project file structure
- Directory organization
- Package hierarchies
- Org charts (with adaptation)
- Category trees
