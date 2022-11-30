# Structures

The structures used in smart contract methods are described here

### FungibleTokenMetadata

```rust
pub struct FungibleTokenMetadata {
    pub spec: String,
    pub name: String,
    pub symbol: String,
    pub icon: Option<String>,
    pub reference: Option<String>,
    pub reference_hash: Option<Base64VecU8>,
    pub decimals: u8,
}
```

### StorageBalance

```rust
pub struct StorageBalance {
    pub total: U128,
    pub available: U128,
}
```

### StorageBalanceBounds

```rust
pub struct StorageBalanceBounds {
    pub min: U128,
    pub max: Option<U128>,
}
```
