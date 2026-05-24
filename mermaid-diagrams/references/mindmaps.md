# Mindmaps

Mindmaps visually organize information into a hierarchy, showing relationships among pieces of a whole around a single central concept.

## Basic Syntax

```mermaid
mindmap
  root((MindMap))
    Origins
      Long history
      Popularisation
    Research
      On effect on productivity
    Tools
      Intuitive
```

## Root Node

The center of the mindmap can use different shapes:

### Default Root

```mermaid
mindmap
  root(Main Topic)
    Subtopic 1
    Subtopic 2
```

### Circular Root

```mermaid
mindmap
  root((Central Idea))
    Branch A
    Branch B
```

## Node Shapes

### Different Node Types

```mermaid
mindmap
  root((Project))
    Planning
      Requirements["Detailed Specs"]
      Timeline
    Development
      Backend{{API Design}}
      Frontend[/UI Components/]
    Testing
      Unit Tests
      E2E Tests
```

## Hierarchical Levels

Add depth with indentation:

```mermaid
mindmap
  root(Software Development)
    Requirements
      Functional
        User Stories
        Use Cases
      Non-functional
        Performance
        Security
    Design
      Architecture
        Microservices
        Monolith
      Database
        Relational
        NoSQL
    Implementation
      Frontend
        React
        Vue
      Backend
        Node.js
        Python
```

## Comprehensive Example

```mermaid
mindmap
  root((Product Strategy))
    Market Analysis
      Competitors
        Direct Competitors
        Indirect Competitors
      Target Audience
        Demographics
        Pain Points
      Market Size
        TAM
        SAM
        SOM
    Product Definition
      Core Features
        MVP Features
        Roadmap Items
      User Experience
        User Flows
        Wireframes
      Technical Architecture
        Frontend Stack
        Backend Stack
        Infrastructure
    Go-to-Market
      Pricing Strategy
        Freemium
        Enterprise
      Marketing Channels
        Content Marketing
        Social Media
        Partnerships
      Sales Strategy
        Self-service
        Sales-led
```

## Best Practices

1. **Start with a central concept** - Clear, focused root node
2. **Use hierarchical structure** - Group related ideas together
3. **Keep it balanced** - Don't let one branch dominate
4. **Use keywords** - Short phrases work better than long sentences
5. **Add visual variety** - Use different node shapes for different types

## Common Use Cases

- Brainstorming sessions
- Meeting notes
- Project planning
- Knowledge organization
- Concept mapping
