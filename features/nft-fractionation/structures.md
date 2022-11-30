# Structures

### Fractionation

```rust
pub struct Fractionation {
    pub token_id: FractionationId,
    pub contract_id: AccountId,
    pub entries: Vec<TokenId>,    
}
```

### FractionationNftOnTransferArgs

```rust
pub struct FractionationNftOnTransferArgs {
    pub fractionation_tokens: Option<Vec<TokenId>>,
}
```
