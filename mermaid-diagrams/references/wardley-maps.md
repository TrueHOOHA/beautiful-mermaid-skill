# Wardley Maps

Wardley maps are visual representations of business strategy that map value chains and component evolution. They position components by visibility (Y-axis) and evolution maturity (X-axis).

## Basic Syntax

```mermaid
wardley-beta
    title "Simple Map"
    anchor User [0.9, 0.95]
    component API [0.6, 0.7]
    component Database [0.5, 0.6]
    User -> API
    API -> Database
```

## Components

### Anchor

The user or customer need at the top:

```mermaid
wardley-beta
    title "E-commerce Value Chain"
    anchor Customer [0.9, 0.95]
    component Website [0.7, 0.8]
    component Payment [0.5, 0.7]
    component Hosting [0.3, 0.4]
    Customer -> Website
    Website -> Payment
    Website -> Hosting
```

### Evolution Stages

X-axis stages (left to right):
- Genesis (0.0-0.2) - novel, uncertain
- Custom (0.2-0.5) - bespoke builds
- Product (0.5-0.8) - off-the-shelf products
- Commodity (0.8-1.0) - utilities, standardized

```mermaid
wardley-beta
    title "Evolution Example"
    anchor Business [0.95, 0.95]
    component AI [0.8, 0.9]
    component Cloud [0.4, 0.5]
    component Electricity [0.1, 0.1]
    Business -> AI
    Business -> Cloud
    Business -> Electricity
```

## Value Chain Links

Show dependencies between components:

```mermaid
wardley-beta
    title "Application Stack"
    anchor Users [0.9, 0.95]
    component WebApp [0.8, 0.85]
    component API [0.6, 0.7]
    component Auth [0.5, 0.65]
    component Database [0.4, 0.5]
    component Compute [0.2, 0.3]
    component Power [0.1, 0.1]
    
    Users -> WebApp
    WebApp -> API
    API -> Auth
    API -> Database
    API -> Compute
    Database -> Compute
    Compute -> Power
```

## Comprehensive Example

```mermaid
wardley-beta
    title "SaaS Platform Strategy"
    anchor Customers [0.95, 0.95]
    
    component Dashboard [0.8, 0.9]
    component Analytics [0.7, 0.8]
    component Reports [0.75, 0.85]
    
    component API [0.6, 0.7]
    component Auth [0.4, 0.6]
    component Notifications [0.5, 0.65]
    
    component Database [0.3, 0.4]
    component Cache [0.35, 0.5]
    component Queue [0.4, 0.55]
    
    component Compute [0.2, 0.3]
    component Storage [0.15, 0.25]
    component Network [0.1, 0.2]
    
    Customers -> Dashboard
    Customers -> Analytics
    Customers -> Reports
    Dashboard -> API
    Analytics -> API
    Reports -> API
    API -> Auth
    API -> Notifications
    API -> Database
    API -> Cache
    API -> Queue
    Database -> Compute
    Cache -> Compute
    Queue -> Compute
    Compute -> Storage
    Compute -> Network
```

## Best Practices

1. **Start with user needs** - Anchor represents the customer
2. **Map value chain** - Show how components deliver value
3. **Understand evolution** - Position components by maturity
4. **Identify strategic opportunities** - Find what to build vs. buy
5. **Iterate over time** - Evolution changes; maps should too

## Common Use Cases

- Business strategy planning
- Build vs. buy decisions
- Market analysis
- Service mapping
- Competitive positioning
