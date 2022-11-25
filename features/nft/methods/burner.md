# Burner

Burner feature allows upgrade certain type NFTs by transferring a certain amount of NFTs of lesser value

### NFT burner upgrade

Method upgrades NFT rarity feature up for one value, per burning a collection of NFTs with a given summarized rarity

Requires the _rarity_ option must be specified at the mint time

```rust
fn nft_burner_upgrade(&mut self, token_id: TokenId, burning_tokens: Vec<TokenId>)
```

### NFT set burner upgrade price

Method sets NFT rarity burner upgrade price in summarized rarity of burning collection of NFTs, according to the specified token types

```rust
fn nft_set_burner_upgrade_price(
        &mut self,
        types: Option<TokenTypes>,
        rarity: TokenRarity,       
        burning_rarity_sum: u8,
) 
```

### NFT remove burner upgrade price

Method removes NFT rarity burner upgrade price according to the specified token types

```rust
fn nft_remove_burner_upgrade_price(
        &mut self,
        types: Option<TokenTypes>,
        rarity: TokenRarity
)
```

### NFT burner upgrade price

Method views NFT rarity burner upgrade price for provided token in summarized rarity of burning collection of NFTs

```rust
fn nft_burner_upgrade_price(&self, token_id: TokenId) -> Option<BurnerPrice>
```
