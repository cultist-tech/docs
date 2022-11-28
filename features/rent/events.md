# Events

### RentAdd

```rust
pub struct RentAdd<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub owner_id: &'a AccountId,
    pub sale_conditions: &'a SaleConditions,
    pub min_time: &'a u64,
    pub max_time: &'a u64,
    pub created_at: &'a u64,
}
```

### RentUpdate

```rust
pub struct RentUpdate<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub owner_id: &'a AccountId,
    pub ft_token_id: &'a AccountId,
    pub price: &'a U128,
    pub min_time: &'a u64,
    pub max_time: &'a u64,
    pub created_at: &'a u64,
}
```

### RentRemove

```rust
pub struct RentRemove<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub account_id: &'a AccountId,
}
```

### RentPay

```rust
pub struct RentPay<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub owner_id: &'a AccountId,
    pub receiver_id: &'a AccountId,
    pub time: &'a u64,
    pub end_time: &'a u64,
    pub price: &'a U128,
}
```

### RentClaim

```rust
pub struct RentClaim<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub owner_id: &'a AccountId,
    pub renter_id: &'a AccountId,
}
```
