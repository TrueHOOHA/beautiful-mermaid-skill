# Radar Charts

Radar charts (also known as spider or star charts) plot multi-dimensional data in a circular format, useful for comparing multiple entities across multiple dimensions.

## Basic Syntax

```mermaid
radar-beta
    title "Skills Assessment"
    axis Communication, Teamwork, Problem Solving, Leadership, Technical
    curve c1{"Employee A"}{3, 4, 5, 2, 4}
    curve c2{"Employee B"}{4, 3, 4, 4, 3}
```

## Defining Axes

List the dimensions to evaluate:

```mermaid
radar-beta
    title "Product Comparison"
    axis Performance, Usability, Security, Scalability, Cost
    curve c1{"Product X"}{4, 5, 3, 4, 5}
    curve c2{"Product Y"}{5, 3, 5, 5, 2}
```

## Multiple Curves

Compare multiple entities:

```mermaid
radar-beta
    title "Team Skills"
    axis Coding, Testing, DevOps, Design, Communication
    curve c1{"Senior Dev"}{5, 4, 3, 2, 4}
    curve c2{"Junior Dev"}{3, 3, 2, 1, 3}
    curve c3{"Tech Lead"}{5, 5, 5, 3, 5}
```

## Comprehensive Example

```mermaid
radar-beta
    title "Framework Evaluation"
    axis Performance, Learning Curve, Community, Flexibility, Documentation, Security
    curve c1{"React"}{5, 3, 5, 5, 5, 4}
    curve c2{"Vue"}{4, 5, 4, 4, 5, 4}
    curve c3{"Angular"}{4, 2, 5, 3, 5, 5}
```

## Best Practices

1. **Limit dimensions** - Keep to 5-8 axes for readability
2. **Use consistent scales** - Typically 1-5 or 1-10
3. **Limit curves** - 2-4 curves work best; more becomes cluttered
4. **Choose meaningful axes** - Dimensions should be relevant to comparison
5. **Label clearly** - Name each curve descriptively

## Common Use Cases

- Skills assessment
- Product comparison
- Performance evaluation
- Feature analysis
- Risk assessment
