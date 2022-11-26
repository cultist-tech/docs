# Structures

### Sale

```rust
pub struct Sale {
    pub owner_id: AccountId,
    pub approval_id: u64,
    pub nft_contract_id: AccountId,
    pub token_id: String,
    pub sale_conditions: SaleConditions,
    pub bids: Bids,
    pub created_at: u64,
    pub is_auction: bool,
}
```

### SaleConditions

```rust
pub type SaleConditions = HashMap<FungibleTokenId, U128>
```

### MarketOnNftApproveArgs

```rust
pub struct MarketOnNftApproveArgs {
    pub sale_conditions: SaleConditions,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub is_auction: Option<bool>,
}
```
