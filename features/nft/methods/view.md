# View

### NFT token

Method views single NFT with provided id

```rust
nft_token(&self, token_id: TokenId) -> Option<Token>
```

### NFT tokens

Method views all minted NFT contracts tokens with pagination

```rust
fn nft_tokens(&self, from_index: Option<U128>, limit: Option<u64>) -> Vec<Token>
```

### NFT total supply

Method views total NFT contract token supply

```rust
fn nft_total_supply(&self) -> U128
```

### NFT tokens for owner

Method views all NFT contracts tokens owned by provided account with pagination

```rust
fn nft_tokens_for_owner(
        &self,
        account_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<Token>
```

### NFT supply for owner

Method views total NFT contract token supply for provided owner

```rust
fn nft_supply_for_owner(&self, account_id: AccountId) -> U128
```

### NFT tokens by ids

Method views an array of tokens for the provided array of token ids&#x20;

```rust
fn nft_tokens_by_ids(&self, ids: Vec<TokenId>) -> Vec<Token>
```
