# Structures

The structures used in smart contract methods are described here

### Rent

```rust
pub struct Rent {
    pub token_id: TokenId,
    pub contract_id: AccountId,
    pub owner_id: AccountId,
    pub sale_conditions: SaleConditions,
    pub min_time: u64,
    pub max_time: u64,
    pub created_at: u64,
}
```

### SaleConditions

```rust
pub type SaleConditions = HashMap<AccountId, U128>;
```

### JsonRent

```rust
pub struct JsonRent {
    pub token_id: TokenId,
    pub contract_id: AccountId,
    pub owner_id: AccountId,
    pub sale_conditions: SaleConditions,
    pub min_time: u64,
    pub max_time: u64,
    pub created_at: u64,
    pub ended_at: Option<u64>,
    pub renter_id: Option<AccountId>,
}
```
