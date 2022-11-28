# Events

### IdoCreate

```rust
pub struct IdoCreate<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub name: &'a String,
    pub media: &'a Option<String>,
    pub amount: &'a u64,
    pub price: &'a U128,
    pub buy_max: &'a u64,
    pub per_transaction_min: &'a u64,
    pub per_transaction_max: &'a u64,
}
```

### IdoStart

```rust
pub struct IdoStart<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub date: &'a u64,
}
```

### IdoUpdate

```rust
pub struct IdoUpdate<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub date: &'a u64,
    pub per_transaction_max: &'a u64,
    pub per_transaction_min: &'a u64,
    pub buy_max: &'a u64,
}
```

### IdoPause

```rust
pub struct IdoPause<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub pause: &'a bool,
}
```

### IdoAddToken

```rust
pub struct IdoAddToken<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
}
```

### IdoBuyToken

```rust
pub struct IdoBuyToken<'a> {
    pub ido_id: &'a IdoId,
    pub contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
    pub price:&'a U128,
    pub ft_token_id: &'a AccountId,
    pub receiver_id: &'a AccountId,
}
```
