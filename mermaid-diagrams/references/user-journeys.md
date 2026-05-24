# User Journey Diagrams

User journey diagrams describe the exact steps different users take to complete a specific task within a system. Tasks are scored by satisfaction (1-5) and assigned to actors.

## Basic Syntax

```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```

## Sections and Tasks

### Defining Sections

Break journeys into logical sections:

```mermaid
journey
    title Online Shopping Experience
    section Browse
      Search products: 4: Customer
      View details: 5: Customer
      Compare items: 3: Customer
    section Purchase
      Add to cart: 5: Customer
      Checkout: 4: Customer
      Pay: 3: Customer, PaymentService
    section Delivery
      Confirm order: 5: System
      Ship package: 4: Warehouse
      Receive: 5: Customer
```

### Task Scoring

Score each task from 1-5 (5 = highest satisfaction):

```mermaid
journey
    title App Onboarding
    section Registration
      Enter email: 4: User
      Verify email: 2: User
      Create password: 3: User
    section Setup
      Upload photo: 2: User
      Add interests: 3: User
      Connect friends: 4: User, System
```

## Multiple Actors

Show when multiple actors are involved:

```mermaid
journey
    title Customer Support Ticket
    section Submission
      Create ticket: 4: Customer
      Auto-assign: 5: System
    section Resolution
      Investigate: 3: Agent
      Request info: 2: Agent, Customer
      Provide solution: 4: Agent
    section Closure
      Confirm fix: 5: Customer
      Close ticket: 5: System
```

## Comprehensive Example: E-Commerce Checkout

```mermaid
journey
    title E-Commerce Checkout Journey
    section Browse
      Search products: 4: Customer
      Filter results: 5: Customer
      View product details: 5: Customer
      Read reviews: 4: Customer
    section Cart
      Add to cart: 5: Customer
      Apply coupon: 3: Customer
      Review cart: 4: Customer
    section Checkout
      Enter shipping: 3: Customer
      Select shipping method: 4: Customer
      Enter payment: 2: Customer
      Place order: 5: Customer, System
    section Post-Purchase
      Receive confirmation: 5: Customer
      Track shipment: 4: Customer
      Receive package: 5: Customer
      Leave review: 3: Customer
```

## Best Practices

1. **Use clear section names** - Break journeys into logical phases
2. **Be honest with scores** - Low scores identify pain points
3. **Include all actors** - Show when systems or other users are involved
4. **Focus on one persona** - Create separate diagrams for different user types
5. **Iterate and improve** - Re-score after UX improvements

## Common Use Cases

- UX research and analysis
- Customer experience mapping
- Service design
- Process improvement
- Onboarding flow evaluation
