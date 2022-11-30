# Events

### FractionationCreate

```rust
pub struct FractionationCreate<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub entries: &'a Vec<TokenId>,
}
```

### FractionationComplete

```rust
pub struct FractionationComplete<'a> {
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub receiver_id: &'a AccountId,
}
```

### FractionationProcess

```rust
pub struct FractionationProcess<'a> {    
    pub token_id: &'a TokenId,
    pub contract_id: &'a AccountId,
    pub account_id: &'a AccountId,
}
```
