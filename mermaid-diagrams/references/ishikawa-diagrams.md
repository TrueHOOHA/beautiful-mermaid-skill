# Ishikawa Diagrams

Ishikawa diagrams (also known as fishbone or cause-and-effect diagrams) are used to represent causes of a specific event or problem, with the main issue at the head and causes branching off the spine.

## Basic Syntax

```mermaid
ishikawa-beta
    title "Website Downtime"
    root "Website Unavailable"
        "Server"
            "Hardware Failure"
            "OS Crash"
        "Network"
            "DNS Issue"
            "CDN Down"
        "Application"
            "Bug"
            "Memory Leak"
```

## Categories and Causes

### Major Categories

Common categories (6 M's):
- Machine (equipment)
- Method (process)
- Material (resources)
- Man (people)
- Measurement (data)
- Milieu/Mother Nature (environment)

```mermaid
ishikawa-beta
    title "Software Bug"
    root "Application Error"
        "Code"
            "Logic Error"
            "Missing Validation"
        "Environment"
            "Config Issue"
            "Wrong Version"
        "Data"
            "Invalid Input"
            "Corrupted Record"
        "Process"
            "Skipped Testing"
            "Bad Merge"
```

## Multiple Sub-causes

Add depth to analysis:

```mermaid
ishikawa-beta
    title "Slow Performance"
    root "Page Load > 3s"
        "Frontend"
            "Large Images"
            "Unoptimized JS"
            "No Caching"
        "Backend"
            "Slow Queries"
            "Missing Indexes"
            "N+1 Problem"
        "Infrastructure"
            "Low Memory"
            "CPU Throttling"
            "Network Latency"
```

## Comprehensive Example

```mermaid
ishikawa-beta
    title "Low User Engagement"
    root "Users Leave After 30s"
        "Product"
            "Confusing Navigation"
            "Missing Features"
            "Poor Mobile Experience"
        "Content"
            "Irrelevant Information"
            "Outdated Data"
            "Poor Quality"
        "Performance"
            "Slow Loading"
            "Frequent Errors"
            "API Timeouts"
        "Marketing"
            "Wrong Audience"
            "Misleading Ads"
            "Wrong Channel"
        "Onboarding"
            "Complex Registration"
            "No Tutorial"
            "Unclear Value Prop"
```

## Best Practices

1. **Define the problem clearly** - Be specific about the effect
2. **Use major categories** - Group causes logically
3. **Go deep enough** - Ask "why?" 3-5 times for root cause
4. **Involve the team** - Different perspectives find more causes
5. **Prioritize causes** - Focus on the most impactful ones

## Common Use Cases

- Root cause analysis
- Quality improvement
- Problem diagnosis
- Process analysis
- Defect investigation
