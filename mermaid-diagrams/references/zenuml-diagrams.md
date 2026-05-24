# ZenUML Diagrams

ZenUML provides an alternative syntax for sequence diagrams, using a code-like bracket-based format similar to programming languages. It's ideal for developers who prefer inline function call syntax.

## Basic Syntax

```mermaid
zenuml
    title Demo
    Alice->John: Hello John, how are you?
    John->Alice: Great!
    Alice->John: See you later!
```

## Participants

### Simple Participants

```mermaid
zenuml
    Client->Server: Request
    Server->Database: Query
    Database->Server: Result
    Server->Client: Response
```

### Named Participants

```mermaid
zenuml
    @Actor User
    @Service API
    @Database DB
    
    User->API: POST /login
    API->DB: SELECT * FROM users
    DB->API: User record
    API->User: JWT token
```

## Messages

### Synchronous Calls

```mermaid
zenuml
    A->B: syncCall()
```

### Replies

```mermaid
zenuml
    A->B: request()
    B->A: response
```

### Self Calls

```mermaid
zenuml
    User->User: validateInput()
    User->API: sendData()
```

## Grouping

### IF/ELSE

```mermaid
zenuml
    User->API: login()
    if (valid) {
        API->DB: storeSession()
        API->User: token
    } else {
        API->User: error
    }
```

### Loops

```mermaid
zenuml
    User->API: getOrders()
    while (hasMore) {
        API->DB: fetchBatch()
        DB->API: orders
    }
    API->User: allOrders
```

### Try/Catch

```mermaid
zenuml
    try {
        User->API: processPayment()
        API->Payment: charge()
    } catch (Error e) {
        API->User: paymentFailed
    }
```

## Comprehensive Example

```mermaid
zenuml
    @Actor User
    @Service AuthAPI
    @Service UserService
    @Database DB
    @Service EmailService
    
    User->AuthAPI: register()
    AuthAPI->AuthAPI: validateInput()
    
    if (valid) {
        AuthAPI->DB: checkExisting()
        DB->AuthAPI: notFound
        
        AuthAPI->DB: createUser()
        DB->AuthAPI: userId
        
        par {
            AuthAPI->EmailService: sendWelcome()
            AuthAPI->UserService: createProfile()
        }
        
        AuthAPI->User: success + token
    } else {
        AuthAPI->User: validationError
    }
```

## Best Practices

1. **Use @declarations** - Type participants with @Actor, @Service, @Database
2. **Group with brackets** - Use if/while/try for complex logic
3. **Keep it readable** - Prefer ZenUML when you want code-like syntax
4. **Use par for parallel** - Show concurrent operations
5. **Self calls for internals** - Show internal processing

## When to Use ZenUML vs Sequence Diagram

**Use ZenUML when:**
- You prefer coding syntax
- Working with developers familiar with code blocks
- Need inline conditionals/loops
- Want a more compact representation

**Use standard sequenceDiagram when:**
- Working with non-developers
- Need visual richness (notes, activations, etc.)
- Need more diagram types (break, critical regions)
