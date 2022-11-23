# Mint

### NFT mint

Method creates NFT with the provided metadata and mints it to the receiver

```rust
fn nft_mint(
        &mut self,
        token_id: TokenId,
        receiver_id: Option<AccountId>,
        token_metadata: TokenMetadata,
        bind_to_owner: Option<bool>,
        perpetual_royalties: Option<Royalty>,
        reveal_at: Option<u64>,
        rarity: Option<TokenRarity>,
        collection: Option<String>,
        token_type: Option<String>,
        token_sub_type: Option<String>,
) -> Token
```

Optional fields defines the usage of additional NFT features
