# Events

### NftCreate

```rust
pub struct NftCreate<'a> {
    pub token: &'a Token,
}
```

### NftMint ****&#x20;

```rust
pub struct NftMint<'a> {
    pub owner_id: &'a AccountId,
    pub token_ids: &'a Vec<String>,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### NftTransfer

```rust
pub struct NftTransfer<'a> {
    pub old_owner_id: &'a AccountId,
    pub new_owner_id: &'a AccountId,
    pub token_ids: &'a [&'a str],
    #[serde(skip_serializing_if = "Option::is_none")]
    pub authorized_id: Option<&'a AccountId>,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### NftBurn

```rust
pub struct NftBurn<'a> {
    pub owner_id: &'a AccountId,
    pub token_ids: &'a [&'a str],
    #[serde(skip_serializing_if = "Option::is_none")]
    pub authorized_id: Option<&'a AccountId>,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### NftTransferPayout

```rust
pub struct NftTransferPayout<'a> {
    pub token_id: &'a TokenId,
    pub sender_id: &'a AccountId,
    pub receiver_id: &'a AccountId,
    pub balance: &'a U128,
    pub payout: &'a HashMap<AccountId, U128>,
}
```

### NftReveal

```rust
pub struct NftReveal<'a> {
    pub owner_id: &'a AccountId,
    pub token_ids: &'a [&'a str],
    #[serde(skip_serializing_if = "Option::is_none")]
    pub authorized_id: Option<&'a AccountId>,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```

### NftUpgrade

<pre class="language-rust"><code class="lang-rust">pub struct NftUpgrade&#x3C;'a> {
    pub owner_id: &#x26;'a AccountId,
    pub rarity: &#x26;'a TokenRarity,
    pub token_id: &#x26;'a TokenId,
<strong>}</strong></code></pre>

### NftSetUpgradePrice

```rust
pub struct NftSetUpgradePrice<'a> {  
    pub rarity: &'a TokenRarity,
    pub types: &'a Option<TokenTypes>,
    pub ft_token: &'a AccountId,
    pub price: &'a U128,
}
```

### NftSetBurnerPrice

```rust
pub struct NftSetBurnerPrice<'a> {  
    pub rarity: &'a TokenRarity,
    pub types: &'a Option<TokenTypes>,
    pub burning_rarity_sum: &'a u8,  
}
```

### NftRemoveUpgradePrice

```rust
pub struct NftRemoveUpgradePrice<'a> {
    pub price_type: &'a PriceType,
    pub rarity: &'a TokenRarity,
    pub types: &'a Option<TokenTypes>,  
}
```
