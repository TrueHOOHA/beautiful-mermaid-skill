# Packet Diagrams

Packet diagrams visually represent the structure and contents of network packets, showing bit positions and field descriptions. They're ideal for protocol documentation and network analysis.

## Basic Syntax

```mermaid
packet
    title UDP Packet
    0-15: Source Port
    16-31: Destination Port
    32-63: Length
    64-95: Checksum
    +96: data octets...
```

## Bit Fields

### Simple Fields

```mermaid
packet
    title TCP Header (First 32 bits)
    0-15: Source Port
    16-31: Destination Port
```

### Variable Length

Use `+` to indicate variable-length fields:

```mermaid
packet
    title IP Header
    0-3: Version
    4-7: IHL
    8-15: TOS
    16-31: Total Length
    32-47: Identification
    +48: Flags, Fragment Offset, TTL, Protocol, Checksum
    +64: Source Address
    +96: Destination Address
    +128: Options + Padding
    +160: Data Payload
```

## Complex Packet Example

```mermaid
packet
    title Ethernet Frame
    0-47: Destination MAC Address
    48-95: Source MAC Address
    96-111: EtherType (0x0800 = IPv4)
    +112: Payload (46-1500 bytes)
    +Variable: FCS (Frame Check Sequence)
```

## Comprehensive Example: HTTP/2 Frame

```mermaid
packet
    title HTTP/2 Frame Header
    0-23: Length (24 bits)
    24-31: Type (8 bits)
    32-39: Flags (8 bits)
    40-63: Reserved (1 bit) + Stream Identifier (31 bits)
    +64: Payload (variable length)
    
    title HTTP/2 Frame Types
    0x0: DATA
    0x1: HEADERS
    0x2: PRIORITY
    0x3: RST_STREAM
    0x4: SETTINGS
    0x5: PUSH_PROMISE
    0x6: PING
    0x7: GOAWAY
    0x8: WINDOW_UPDATE
    0x9: CONTINUATION
```

## Best Practices

1. **Show bit positions** - Always indicate bit ranges
2. **Use consistent widths** - Align fields by bit position
3. **Label clearly** - Include field names and descriptions
4. **Use `+` for variable fields** - Indicate fields of variable length
5. **Include protocol context** - Mention what protocol you're describing

## Common Use Cases

- Protocol documentation
- Network packet analysis
- Binary data layouts
- Hardware register maps
- File format specifications
