# Event Modeling

Event modeling is a method of describing systems using examples of how information has changed within them over time, organized in swimlanes (UI, Command, Event).

## Basic Syntax

```mermaid
eventmodeling
    tf 01 ui CartUI
    tf 02 cmd AddItem
    tf 03 evt ItemAdded
    data ItemAdded01 { "name": "item" }
```

## Swimlanes

### UI (User Interface)

Represents views or screens users interact with:

```mermaid
eventmodeling
    tf 01 ui ProductPage
    tf 02 ui CartPage
    tf 03 ui CheckoutPage
```

### Command

Represents actions or commands users trigger:

```mermaid
eventmodeling
    tf 01 cmd ViewProduct
    tf 02 cmd AddToCart
    tf 03 cmd PlaceOrder
```

### Event

Represents state changes or domain events:

```mermaid
eventmodeling
    tf 01 evt ProductViewed
    tf 02 evt ItemAdded
    tf 03 evt OrderPlaced
```

## Data

Attach data to events:

```mermaid
eventmodeling
    tf 01 cmd AddItem
    tf 02 evt ItemAdded
    data ItemAdded01 { 
        "productId": "123",
        "quantity": 2,
        "price": 29.99
    }
```

## Comprehensive Example

```mermaid
eventmodeling
    tf 01 ui ProductCatalog
    tf 02 cmd ViewProduct
    tf 03 evt ProductViewed
    
    tf 04 ui ProductDetail
    tf 05 cmd AddToCart
    tf 06 evt ItemAddedToCart
    data ItemAdded01 {
        "cartId": "cart-001",
        "productId": "prod-123",
        "quantity": 1,
        "price": 49.99
    }
    
    tf 07 ui CartPage
    tf 08 cmd UpdateQuantity
    tf 09 evt QuantityUpdated
    
    tf 10 cmd RemoveItem
    tf 11 evt ItemRemoved
    
    tf 12 cmd ProceedToCheckout
    tf 13 ui CheckoutPage
    tf 14 cmd PlaceOrder
    tf 15 evt OrderPlaced
    data OrderPlaced01 {
        "orderId": "ord-456",
        "customerId": "cust-789",
        "total": 49.99,
        "items": [
            {"productId": "prod-123", "quantity": 1}
        ]
    }
    
    tf 16 evt PaymentProcessed
    tf 17 ui OrderConfirmation
```

## Best Practices

1. **Follow the timeline** - Events flow left to right through time
2. **Use swimlanes** - Separate UI, commands, and events
3. **Attach data** - Show what information changes
4. **Be specific** - Use realistic example data
5. **Show progression** - Demonstrate the full lifecycle

## Common Use Cases

- Event-sourced system design
- Domain event flows
- CQRS pattern documentation
- System state transitions
- Audit trail visualization
