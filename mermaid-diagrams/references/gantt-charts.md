# Gantt Charts

Gantt charts illustrate project schedules, showing start and finish dates of tasks, milestones, and dependencies between activities.

## Basic Syntax

```mermaid
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2014-01-01, 30d
    Another task     :after a1, 20d
```

## Date Formats

Common date formats:
- `YYYY-MM-DD` - 2024-01-15
- `DD-MM-YYYY` - 15-01-2024
- `MM-DD-YYYY` - 01-15-2024

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Project
    Start project :2024-01-01, 7d
    Research      :2024-01-08, 14d
```

## Tasks and Durations

### Fixed Dates

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Tasks
    Task A :2024-01-01, 10d
    Task B :2024-01-11, 15d
```

### Relative Dates

Use task IDs to create dependencies:

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Development
    Design    :a1, 2024-01-01, 10d
    Coding    :after a1, 20d
    Testing   :after a1, 15d
```

### Milestones

Mark important checkpoints:

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Milestones
    Project Start :milestone, 2024-01-01, 0d
    Design Complete :milestone, 2024-01-15, 0d
    Launch :milestone, 2024-03-01, 0d
```

## Sections

Group related tasks:

```mermaid
gantt
    dateFormat YYYY-MM-DD
    title Software Development Project
    
    section Planning
    Requirements    :2024-01-01, 14d
    Architecture    :2024-01-15, 10d
    
    section Development
    Backend API     :2024-01-25, 30d
    Frontend        :2024-02-01, 35d
    Integration     :2024-03-07, 14d
    
    section Testing
    Unit Tests      :2024-02-15, 20d
    E2E Tests       :2024-03-15, 14d
    UAT             :2024-03-25, 10d
    
    section Deployment
    Staging Deploy  :milestone, 2024-04-01, 0d
    Production      :milestone, 2024-04-05, 0d
```

## Task Status

Show task completion status:

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Sprint 1
    Completed task    :done, 2024-01-01, 10d
    Active task       :active, 2024-01-08, 12d
    Future task       :2024-01-15, 10d
    Critical path     :crit, 2024-01-20, 15d
```

## Dependencies

Link tasks together:

```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Build
    Foundation :a1, 2024-01-01, 14d
    Walls      :after a1, 21d
    Roof       :after a1, 14d
    Interior   :after a1, 28d
```

## Comprehensive Example: Product Launch

```mermaid
gantt
    dateFormat YYYY-MM-DD
    title Product Launch Timeline
    
    section Strategy
    Market Research    :done, 2024-01-01, 21d
    Competitive Analysis :done, 2024-01-15, 14d
    Define Strategy    :milestone, 2024-01-30, 0d
    
    section Design
    UX Research        :done, 2024-02-01, 14d
    Wireframes         :active, 2024-02-10, 14d
    Visual Design      :2024-02-20, 21d
    Prototype          :2024-03-05, 14d
    Design Review      :milestone, 2024-03-15, 0d
    
    section Development
    Setup Architecture :2024-02-15, 10d
    Core Features      :crit, 2024-02-20, 45d
    API Development    :2024-03-01, 35d
    Frontend           :2024-03-10, 30d
    Integration        :2024-04-10, 14d
    
    section Testing
    QA Planning        :2024-03-15, 10d
    Unit Testing       :2024-03-20, 25d
    Integration Tests  :2024-04-15, 14d
    Performance Tests  :2024-04-20, 10d
    Bug Fixes          :2024-04-25, 10d
    
    section Launch
    Beta Release       :milestone, 2024-05-01, 0d
    Marketing Campaign :2024-04-15, 20d
    Documentation      :2024-04-20, 15d
    Public Launch      :milestone, 2024-05-15, 0d
```

## Best Practices

1. **Use meaningful task names** - Clear descriptions help stakeholders understand
2. **Group by section** - Organize related tasks together
3. **Show dependencies** - Use `after` to link sequential tasks
4. **Mark milestones** - Highlight critical checkpoints with 0-day tasks
5. **Track progress** - Use `:done` and `:active` for status
6. **Identify critical path** - Use `:crit` for tasks that affect overall timeline

## Common Patterns

### Simple Sprint
```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Sprint 5
    Planning    :2024-01-01, 1d
    Development :2024-01-02, 8d
    Testing     :2024-01-10, 3d
    Review      :2024-01-13, 1d
```

### Parallel Workstreams
```mermaid
gantt
    dateFormat YYYY-MM-DD
    section Team A
    Backend     :2024-01-01, 30d
    
    section Team B
    Frontend    :2024-01-15, 25d
    
    section QA
    Testing     :2024-02-15, 14d
```
