# Enumeration

### Supported FT token ids

Method views FT tokens that are supported on the market for the NFT token sales

```rust
fn supported_ft_token_ids(&self) -> Vec<AccountId>
```

### Market supply sales

Method views the total number of sales currently on the market

```rust
fn market_supply_sales(&self) -> U64
```

### Market supply by owner

Method views the total number of market sales by provided user

```rust
fn market_supply_by_owner_id(&self, account_id: AccountId) -> U64
```

### Market sales by owner ID

Method views the current market sales of the provided user

```rust
fn market_sales_by_owner_id(
        &self,
        account_id: AccountId,
        from_index: U64,
        limit: u64
) -> Vec<Sale>
```

### Market supply by NFT contract ID

Method views the total number of current market sales by the provided NFT smart contract

```rust
fn market_supply_by_nft_contract_id(&self, nft_contract_id: AccountId) -> U64
```

### Market sales by NFT contract ID

Method views the current market sales by the provided NFT smart contract

```rust
fn market_sales_by_nft_contract_id(
        &self,
        nft_contract_id: AccountId,
        from_index: U64,
        limit: u64
) -> Vec<Sale>
```

### Market sale

Method views provided NFT token market sale

```rust
fn market_sale(&self, contract_id: AccountId, token_id: TokenId) -> Option<Sale> 
```
