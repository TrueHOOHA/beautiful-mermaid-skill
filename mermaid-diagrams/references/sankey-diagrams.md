# Sankey Diagrams

Sankey diagrams visualize flows from one set of values to another, where the width of each link is proportional to the flow value. They're ideal for showing energy, material, or budget flows.

## Basic Syntax

```mermaid
sankey-beta
    Agricultural "waste",Bio-conversion,124.729
    Bio-conversion,Liquid,0.597
    Bio-conversion,Losses,26.862
```

## Nodes and Flows

Each line defines a flow: `Source,Target,Value`

```mermaid
sankey-beta
    Income,Salary,5000
    Income,Freelance,1500
    Salary,Rent,1500
    Salary,Food,800
    Salary,Savings,2000
    Salary,Utilities,700
    Freelance,Savings,1500
```

## Multiple Sources and Targets

Nodes can have multiple incoming and outgoing flows:

```mermaid
sankey-beta
    Source A,Process,100
    Source B,Process,80
    Process,Output 1,120
    Process,Output 2,40
    Process,Loss,20
```

## Comprehensive Example: Budget Flow

```mermaid
sankey-beta
    Total Budget,Development,45000
    Total Budget,Marketing,25000
    Total Budget,Operations,20000
    Total Budget,Infrastructure,15000
    Development,Salaries,35000
    Development,Tools,6000
    Development,Training,4000
    Marketing,Ads,15000
    Marketing,Events,6000
    Marketing,Content,4000
    Operations,Office,12000
    Operations,Legal,5000
    Operations,Accounting,3000
    Infrastructure,Cloud,10000
    Infrastructure,Security,5000
```

## Energy Flow Example

```mermaid
sankey-beta
    Coal,Power Plant,35
    Natural Gas,Power Plant,25
    Nuclear,Power Plant,20
    Renewables,Power Plant,15
    Power Plant,Residential,45
    Power Plant,Industrial,30
    Power Plant,Commercial,15
    Power Plant,Losses,10
```

## Best Practices

1. **Consistent units** - All values should use the same unit
2. **Balance the diagram** - Total inputs should equal total outputs
3. **Use descriptive node names** - Clear labels help understanding
4. **Order logically** - Flow left-to-right or top-to-bottom
5. **Limit complexity** - Too many nodes make diagrams hard to read

## Common Use Cases

- Budget allocation flows
- Energy consumption analysis
- Material flow analysis
- User journey funnels
- Supply chain visualization
