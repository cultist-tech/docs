# Sales

Sales feature is basic and allows sale NFT tokens at the market&#x20;

Sale may be created by the use of approve mechanics of the NFT contact, and can be marked as an auction

### Market add FT token

Methods allows add a support of provided FT token to the market

```rust
fn market_add_ft_token(&mut self, nft_contract_id: AccountId) -> bool
```

### Market remove sale

Method removes provided NFT token sale from the market

```rust
fn market_remove_sale(&mut self, nft_contract_id: AccountId, token_id: String)
```

### Market update price

Method updates the price was set for the NFT token on sale

```rust
fn market_update_price(
        &mut self,
        nft_contract_id: AccountId,
        token_id: String,
        ft_token_id: AccountId,
        price: U128
)
```

### Market offer

Method allows buyer make an offer for the NFT token sale

```rust
fn market_offer(&mut self, nft_contract_id: AccountId, token_id: String)
```

### Market accept offer

Method allows NFT token owner accept a acceptable auction offer on the market&#x20;

```rust
fn market_accept_offer(
        &mut self,
        nft_contract_id: AccountId,
        token_id: String,
        ft_token_id: AccountId
) 
```
