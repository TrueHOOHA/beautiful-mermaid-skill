# Quadrant Charts

Quadrant charts divide a two-dimensional grid into four sections, used to plot data points and identify patterns, trends, and priorities.

## Basic Syntax

```mermaid
quadrantChart
    title Reach and engagement of campaigns
    x-axis Low Reach --> High Reach
    y-axis Low Engagement --> High Engagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A: [0.3, 0.6]
    Campaign B: [0.45, 0.23]
    Campaign C: [0.57, 0.69]
    Campaign D: [0.78, 0.34]
```

## Axis Configuration

Define axis labels with ranges:

```mermaid
quadrantChart
    title Risk Assessment Matrix
    x-axis Low Impact --> High Impact
    y-axis Low Probability --> High Probability
    quadrant-1 High Priority
    quadrant-2 Monitor Closely
    quadrant-3 Low Priority
    quadrant-4 Maintain
```

## Quadrant Labels

Name each of the four quadrants:

```mermaid
quadrantChart
    title Feature Prioritization
    x-axis Low Value --> High Value
    y-axis Low Effort --> High Effort
    quadrant-1 Quick Wins
    quadrant-2 Major Projects
    quadrant-3 Fill-ins
    quadrant-4 Thankless Tasks
```

## Data Points

Plot items with [x, y] coordinates (0-1 scale):

```mermaid
quadrantChart
    title Team Skills Assessment
    x-axis Technical --> Business
    y-axis Junior --> Senior
    quadrant-1 Senior Business
    quadrant-2 Senior Technical
    quadrant-3 Junior Technical
    quadrant-4 Junior Business
    "Alice - PM" : [0.7, 0.8]
    "Bob - Dev" : [0.2, 0.9]
    "Carol - Designer" : [0.5, 0.6]
    "Dave - Analyst" : [0.8, 0.4]
    "Eve - Junior Dev" : [0.3, 0.2]
```

## Comprehensive Example: Product Portfolio

```mermaid
quadrantChart
    title Product Portfolio Analysis
    x-axis Low Market Growth --> High Market Growth
    y-axis Low Market Share --> High Market Share
    quadrant-1 Stars (Invest)
    quadrant-2 Question Marks (Evaluate)
    quadrant-3 Cash Cows (Maintain)
    quadrant-4 Dogs (Divest)
    
    "Product Alpha" : [0.8, 0.75]
    "Product Beta" : [0.6, 0.85]
    "Product Gamma" : [0.3, 0.2]
    "Product Delta" : [0.85, 0.15]
    "Product Epsilon" : [0.45, 0.55]
    "New Venture" : [0.75, 0.3]
    "Legacy System" : [0.15, 0.8]
```

## Best Practices

1. **Define clear axes** - Axis labels should be opposites (Low/High)
2. **Name quadrants meaningfully** - Each quadrant should suggest an action
3. **Use consistent scale** - Coordinates range from 0 to 1
4. **Limit data points** - Too many items make the chart hard to read
5. **Label points clearly** - Use descriptive names for each point

## Common Use Cases

- Risk assessment matrices
- Feature prioritization
- Skills assessment
- Market positioning
- Strategic planning (BCG matrix)
