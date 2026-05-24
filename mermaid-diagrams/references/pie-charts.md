# Pie Charts

Pie charts display data as circular statistical graphics divided into slices, where the arc length of each slice is proportional to the quantity it represents.

## Basic Syntax

```mermaid
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
```

## Show Data Values

Display percentages alongside labels:

```mermaid
pie showData
    title Project Budget Allocation
    "Development" : 40
    "Design" : 20
    "Marketing" : 15
    "Operations" : 15
    "Contingency" : 10
```

## Multiple Data Sets

```mermaid
pie
    title Market Share 2024
    "Company A" : 35
    "Company B" : 28
    "Company C" : 20
    "Others" : 17
```

## Comprehensive Example

```mermaid
pie showData
    title Time Distribution in Sprint
    "Development" : 45
    "Meetings" : 15
    "Code Review" : 10
    "Testing" : 15
    "Documentation" : 8
    "Learning" : 7
```

## Best Practices

1. **Limit slices** - Keep to 5-7 categories for readability
2. **Use percentages or values** - Either works; pick one consistently
3. **Sort by size** - Order slices from largest to smallest
4. **Label clearly** - Use descriptive names with quotes
5. **Use `showData`** - Display values for clarity

## Common Use Cases

- Budget allocation visualization
- Market share analysis
- Time tracking summaries
- Survey result distribution
- Resource utilization
