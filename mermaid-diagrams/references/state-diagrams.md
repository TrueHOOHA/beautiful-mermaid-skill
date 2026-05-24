# State Diagrams

State diagrams model the behavior of systems with a finite number of states, showing how an object transitions from one state to another in response to events.

## Basic Syntax

```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]
```

## States and Transitions

### Simple States

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Processing : start
    Processing --> Completed : finish
    Completed --> [*]
```

### State with Description

```mermaid
stateDiagram-v2
    [*] --> Active
    Active --> Inactive : deactivate
    Inactive --> Active : activate
    Inactive --> [*]
```

## Composite States

Group related states together:

```mermaid
stateDiagram-v2
    [*] --> First
    First --> Second
    Second --> Third
    Third --> [*]

    state First {
        [*] --> inner1
        inner1 --> inner2
    }

    state Second {
        [*] --> innerA
        innerA --> innerB
    }
```

## Forks and Joins

Split into parallel states or join them back:

```mermaid
stateDiagram-v2
    state fork_state <<fork>>
    [*] --> fork_state
    fork_state --> State1
    fork_state --> State2

    state join_state <<join>>
    State1 --> join_state
    State2 --> join_state
    join_state --> [*]
```

## Notes

Add explanatory notes to states:

```mermaid
stateDiagram-v2
    [*] --> Active
    Active --> Inactive
    Note right of Active : System is processing
    Note left of Inactive : System is idle
```

## Choice (Conditional)

Diamond-shaped decision points:

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> ChoiceState
    ChoiceState --> Processing : [condition A]
    ChoiceState --> Error : [condition B]
    Processing --> [*]
    Error --> Idle : retry
```

## Comprehensive Example: Order Lifecycle

```mermaid
stateDiagram-v2
    [*] --> Draft
    
    Draft --> Submitted : submit order
    Submitted --> Validating : validate
    
    state Validating {
        [*] --> CheckInventory
        CheckInventory --> CheckPayment : in stock
        CheckInventory --> OutOfStock : no stock
        CheckPayment --> Valid : payment ok
        CheckPayment --> PaymentFailed : declined
    }
    
    Validating --> Confirmed : validation passed
    Validating --> Rejected : validation failed
    
    Rejected --> Draft : edit and resubmit
    
    Confirmed --> Processing : start fulfillment
    
    state Processing {
        [*] --> Picking
        Picking --> Packing
        Packing --> Shipping
    }
    
    Processing --> Shipped : dispatched
    Shipped --> Delivered : delivered
    Delivered --> [*]
    
    Shipped --> Cancelled : cancel request
    Confirmed --> Cancelled : cancel request
    Cancelled --> [*]
```

## Best Practices

1. **Use descriptive state names** - Clear names make diagrams self-documenting
2. **Show all transitions** - Document how the system moves between states
3. **Include start and end states** - Use `[*]` for initial and final states
4. **Group related states** - Use composite states for complex hierarchies
5. **Label transitions** - Event names on arrows clarify what triggers changes
6. **Handle errors** - Include error states and recovery paths

## Common Patterns

### Simple Toggle
```mermaid
stateDiagram-v2
    [*] --> Off
    Off --> On : turn on
    On --> Off : turn off
```

### Three-State System
```mermaid
stateDiagram-v2
    [*] --> Pending
    Pending --> Approved : approve
    Pending --> Rejected : reject
    Rejected --> Pending : resubmit
    Approved --> [*]
```

### Loop with Exit
```mermaid
stateDiagram-v2
    [*] --> Waiting
    Waiting --> Processing : event received
    Processing --> Waiting : done
    Waiting --> Shutdown : shutdown signal
    Shutdown --> [*]
```
