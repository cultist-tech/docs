# Upgrade

Upgrade feature allows upgrade certain type NFTs by transferring a certain amount of FT or NEAR

### NFT upgrade

Method upgrades NFT rarity feature up for one value

Requires the _rarity_ option must be specified at the mint time

```rust
fn nft_upgrade(&mut self, token_id: TokenId)
```

### NFT set upgrade price

Method sets NFT rarity upgrade price in NEAR or FT, according to the specified token types

```rust
fn nft_set_upgrade_price(
        &mut self,
        types: Option<TokenTypes>,
        rarity: TokenRarity,
        ft_token_id: AccountId,
        price: U128
) 
```

### NFT remove upgrade price

Method removes NFT rarity upgrade price according to the specified token types

```rust
fn nft_remove_upgrade_price(
        &mut self,
        types: Option<TokenTypes>,
        rarity: TokenRarity,       
)
```

### NFT upgrade price

Method views NFT rarity upgrade price for provided token in NEAR or FT

```rust
fn nft_upgrade_price(&self, token_id: TokenId) -> Option<(AccountId, U128)>
```
