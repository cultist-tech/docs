# Structures

The structures used in smart contract methods are described here

### Token

```rust
pub struct Token {
    // core
    pub token_id: TokenId,
    pub owner_id: AccountId,
    pub metadata: Option<TokenMetadata>,
    pub approved_account_ids: Option<HashMap<AccountId, u64>>,

    // royalty extension
    pub royalty: Option<Royalty>,

    // bind to owner extension
    pub bind_to_owner: Option<bool>,

    pub reveal_at: Option<u64>,

    // extra fields
    pub rarity: Option<TokenRarity>,
    pub types: Option<TokenTypes>,
}
```

### TokenMetadata

```rust
pub struct TokenMetadata {
    pub title: Option<String>,
    pub description: Option<String>,
    pub media: Option<String>,
    pub media_hash: Option<Base64VecU8>, 
    pub copies: Option<u64>, 
    pub issued_at: Option<String>, 
    pub expires_at: Option<String>, 
    pub starts_at: Option<String>, 
    pub updated_at: Option<String>, 
    pub extra: Option<String>, 
    pub reference: Option<String>, 
    pub reference_hash: Option<Base64VecU8>,  
}
```

### Royalty

```rust
pub type Royalty = HashMap<AccountId, u32>;
```

### Payout

```rust
pub struct Payout {
    pub payout: HashMap<AccountId, U128>,
}
```

### TokenRarity

```rust
pub type TokenRarity = u8;
```

### TokenTypes

```rust
pub type TokenTypes = HashMap<String, String>;
```

### BurnerPrice

```rust
pub type BurnerPrice = u8;
```

### PriceType

```rust
pub enum PriceType {
    Upgradable,
    Burner,
}
```
