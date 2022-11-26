# Events

### MarketCreateSale

```rust
pub struct MarketCreateSale<'a> {
    pub owner_id: &'a AccountId,
    pub nft_contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
    pub sale: &'a Sale,
}
```

### MarketUpdateSale

```rust
pub struct MarketUpdateSale<'a> {
    pub owner_id: &'a AccountId,
    pub nft_contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
    pub ft_token_id: &'a AccountId,
    pub price: &'a U128,
}
```

### MarketRemoveSale

```rust
pub struct MarketRemoveSale<'a> {
    pub owner_id: &'a AccountId,
    pub nft_contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
}
```

### MarketOffer

```rust
pub struct MarketOffer<'a> {
    pub owner_id: &'a AccountId,
    pub receiver_id: &'a AccountId,
    pub nft_contract_id: &'a AccountId,
    pub token_id: &'a TokenId,
    pub payout: &'a HashMap<AccountId, U128>,
    pub ft_token_id: &'a AccountId,
    pub price: &'a U128,
}
```
