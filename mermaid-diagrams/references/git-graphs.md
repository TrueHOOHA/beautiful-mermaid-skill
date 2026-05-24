# Git Graphs

Git graphs visualize version control history, including commits, branches, merges, and tags. They're ideal for documenting branching strategies and explaining git workflows.

## Basic Syntax

```mermaid
gitGraph
    commit
    commit
```

## Branches

### Creating Branches

```mermaid
gitGraph
    commit
    branch develop
    checkout develop
    commit
    commit
```

### Merging Branches

```mermaid
gitGraph
    commit
    branch feature
    checkout feature
    commit
    commit
    checkout main
    merge feature
    commit
```

## Commits

### Basic Commits

```mermaid
gitGraph
    commit id: "Initial commit"
    commit id: "Add README"
    commit id: "Setup project"
```

### Commits with Tags

```mermaid
gitGraph
    commit id: "v1.0.0" tag: "v1.0.0"
    commit id: "Add feature"
    commit id: "v1.1.0" tag: "v1.1.0"
```

### Commits with Types

```mermaid
gitGraph
    commit id: "feat: add login"
    commit id: "fix: resolve auth bug" type: HIGHLIGHT
    commit id: "docs: update README"
```

## Comprehensive Example: GitFlow Workflow

```mermaid
gitGraph
    commit id: "Initial commit"
    branch develop
    checkout develop
    commit id: "Setup dev environment"
    
    branch feature/login
    checkout feature/login
    commit id: "Add login form"
    commit id: "Add auth logic"
    checkout develop
    merge feature/login id: "Merge login feature"
    
    branch feature/dashboard
    checkout feature/dashboard
    commit id: "Create dashboard"
    commit id: "Add widgets"
    checkout develop
    merge feature/dashboard id: "Merge dashboard"
    
    branch release/v1.0
    checkout release/v1.0
    commit id: "Bump version"
    commit id: "Update changelog"
    checkout main
    merge release/v1.0 id: "Release v1.0" tag: "v1.0.0"
    checkout develop
    merge main id: "Sync release"
    
    branch hotfix/critical
    checkout hotfix/critical
    commit id: "Fix critical bug"
    checkout main
    merge hotfix/critical id: "Apply hotfix" tag: "v1.0.1"
    checkout develop
    merge main id: "Sync hotfix"
```

## Feature Branch Workflow

```mermaid
gitGraph
    commit id: "Initial"
    branch feature/api
    checkout feature/api
    commit id: "Add endpoints"
    commit id: "Add tests"
    checkout main
    merge feature/api id: "Merge API feature"
    
    branch feature/ui
    checkout feature/ui
    commit id: "Add components"
    commit id: "Add styling"
    checkout main
    merge feature/ui id: "Merge UI feature"
    commit id: "Deploy to prod" tag: "v1.0"
```

## Best Practices

1. **Use conventional commit messages** - `feat:`, `fix:`, `docs:` prefixes
2. **Tag releases** - Mark version points with `tag: "vX.Y.Z"`
3. **Show merge commits** - Document integration points
4. **Use meaningful branch names** - `feature/`, `bugfix/`, `hotfix/` prefixes
5. **Keep diagrams focused** - Show one workflow per diagram
6. **Highlight important commits** - Use `type: HIGHLIGHT` for critical changes

## Common Branching Strategies

### Trunk-Based Development
```mermaid
gitGraph
    commit
    commit
    branch feature-short
    checkout feature-short
    commit
    checkout main
    merge feature-short
    commit
```

### Release Branching
```mermaid
gitGraph
    commit id: "v2.0" tag: "v2.0"
    branch release/2.1
    checkout release/2.1
    commit id: "Cherry-pick fixes"
    commit id: "v2.1" tag: "v2.1"
    checkout main
    merge release/2.1
```
