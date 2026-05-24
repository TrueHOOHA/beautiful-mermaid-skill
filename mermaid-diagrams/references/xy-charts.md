# XY Charts

XY charts provide comprehensive charting capabilities including bar charts and line charts using both x-axis and y-axis for data representation.

## Basic Syntax

```mermaid
xychart-beta
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500]
```

## Bar Charts

### Simple Bar Chart

```mermaid
xychart-beta
    title "Monthly Visitors"
    x-axis [Jan, Feb, Mar, Apr, May]
    y-axis "Visitors (thousands)" 0 --> 100
    bar [45, 52, 38, 65, 78]
```

### Multiple Bar Series

```mermaid
xychart-beta
    title "Product Sales Comparison"
    x-axis [Q1, Q2, Q3, Q4]
    y-axis "Sales (units)" 0 --> 500
    bar [200, 250, 300, 450]
    bar [150, 180, 220, 280]
```

## Line Charts

### Simple Line Chart

```mermaid
xychart-beta
    title "Temperature Trends"
    x-axis [Mon, Tue, Wed, Thu, Fri]
    y-axis "Temperature (°C)" 0 --> 40
    line [22, 25, 28, 24, 26]
```

### Multiple Line Series

```mermaid
xychart-beta
    title "Performance Comparison"
    x-axis [Jan, Feb, Mar, Apr, May, Jun]
    y-axis "Score" 0 --> 100
    line [65, 70, 75, 72, 80, 85]
    line [50, 55, 60, 68, 72, 78]
```

## Combined Bar and Line

```mermaid
xychart-beta
    title "Revenue vs Profit"
    x-axis [Q1, Q2, Q3, Q4]
    y-axis "Amount ($)" 0 --> 50000
    bar [30000, 35000, 42000, 48000]
    line [5000, 8000, 12000, 15000]
```

## Axis Configuration

### Custom X-Axis Labels

```mermaid
xychart-beta
    title "Website Metrics"
    x-axis [Week 1, Week 2, Week 3, Week 4]
    y-axis "Count" 0 --> 1000
    bar [500, 650, 720, 850]
```

### Y-Axis Range

```mermaid
xychart-beta
    title "Stock Price"
    x-axis [Mon, Tue, Wed, Thu, Fri]
    y-axis "Price ($)" 100 --> 200
    line [120, 135, 128, 150, 165]
```

## Comprehensive Example: Annual Report

```mermaid
xychart-beta
    title "Company Annual Performance"
    x-axis [Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec]
    y-axis "Revenue (millions)" 0 --> 15
    bar [5.2, 6.1, 7.3, 6.8, 8.2, 9.5, 8.9, 10.2, 11.5, 10.8, 12.3, 13.5]
    line [5.0, 5.5, 6.5, 7.0, 7.8, 8.5, 9.0, 9.8, 10.5, 11.0, 12.0, 13.0]
```

## Best Practices

1. **Choose the right chart type** - Bars for discrete comparisons, lines for trends
2. **Label axes clearly** - Include units and descriptive names
3. **Set appropriate ranges** - Y-axis should fit data with some padding
4. **Limit series** - Too many lines/bars become hard to read
5. **Use consistent colors** - Match colors in legends to data

## Common Use Cases

- Financial reporting
- Performance metrics
- Sales tracking
- Website analytics
- Scientific data visualization
