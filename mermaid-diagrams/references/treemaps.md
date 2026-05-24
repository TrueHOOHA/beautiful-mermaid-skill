# Treemaps

Treemaps display hierarchical data as a set of nested rectangles, where the area of each rectangle is proportional to the value it represents.

## Basic Syntax

```mermaid
treemap-beta
    "Root"
        "Section A"
            "Item A1": 30
            "Item A2": 20
        "Section B"
            "Item B1": 25
            "Item B2": 25
```

## Hierarchical Data

### Simple Hierarchy

```mermaid
treemap-beta
    "Budget"
        "Development"
            "Salaries": 50
            "Tools": 10
        "Marketing"
            "Ads": 20
            "Events": 10
        "Operations"
            "Office": 7
            "Legal": 3
```

### Deep Nesting

```mermaid
treemap-beta
    "Company"
        "Engineering"
            "Frontend"
                "React Team": 15
                "Vue Team": 10
            "Backend"
                "API Team": 20
                "Data Team": 12
        "Product"
            "Design": 8
            "Management": 5
        "Sales"
            "Enterprise": 18
            "SMB": 12
```

## Value Assignment

Use `: value` to assign numeric values:

```mermaid
treemap-beta
    "Disk Usage"
        "System": 20
        "Users"
            "Documents": 45
            "Downloads": 30
            "Pictures": 60
            "Videos": 80
        "Applications": 40
        "Cache": 15
```

## Comprehensive Example

```mermaid
treemap-beta
    "Revenue by Region"
        "North America"
            "Enterprise": 120
            "Mid-Market": 80
            "SMB": 40
        "Europe"
            "Enterprise": 90
            "Mid-Market": 60
            "SMB": 30
        "Asia Pacific"
            "Enterprise": 70
            "Mid-Market": 50
            "SMB": 25
        "Latin America"
            "Enterprise": 30
            "Mid-Market": 20
            "SMB": 15
```

## Best Practices

1. **Use meaningful names** - Labels should clearly identify each item
2. **Ensure values are positive** - Treemaps require positive numeric values
3. **Balance hierarchy depth** - Too deep makes visualization complex
4. **Group logically** - Organize related items under common parents
5. **Use consistent units** - All values should use the same scale

## Common Use Cases

- Disk space usage
- Budget allocation breakdown
- Market share by category
- Portfolio composition
- Website traffic by section
