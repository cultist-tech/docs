# Events

### FtMint

```rust
pub struct FtMint<'a> {
    pub owner_id: &'a AccountId,
    pub amount: &'a U128,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### FtTransfer

```rust
pub struct FtTransfer<'a> {
    pub old_owner_id: &'a AccountId,
    pub new_owner_id: &'a AccountId,
    pub amount: &'a U128,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### FtBurn

```rust
pub struct FtBurn<'a> {
    pub owner_id: &'a AccountId,
    pub amount: &'a U128,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```
