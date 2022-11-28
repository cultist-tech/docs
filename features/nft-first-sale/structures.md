# Structures

### Ido

```rust
pub struct Ido {
    pub ido_id: IdoId,
    pub contract_id: AccountId,
    pub name: String,
    pub media: Option<String>,
    pub amount: u64,
    pub price: U128,
    pub buy_max: u64,
    pub per_transaction_min: u64,
    pub per_transaction_max: u64,
}
```

### JsonIdo

```rust
pub struct JsonIdo {
    pub ido_id: IdoId,
    pub contract_id: AccountId,
    pub name: String,
    pub media: Option<String>,
    pub amount: u64,
    pub amount_ready: u64,
    pub price: U128,
    pub buy_max: u64,
    pub per_transaction_min: u64,
    pub per_transaction_max: u64,
    pub not_minted: u64,
    pub locked: bool,
    pub start_date: Option<u64>,
    pub ft_token: Option<AccountId>,
}
```

### NftIdoOnNftTransferArgs

```rust
pub struct NftIdoOnNftTransferArgs {
    pub ido_id: IdoId,
}
```

### NftIdoOnFtTransferArgs

```rust
pub struct NftIdoOnFtTransferArgs {    
    pub contract_id: AccountId,
    pub ido_id: IdoId,
    pub receiver_id: AccountId,
    pub mint_amount: u64,
}
```
