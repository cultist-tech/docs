# Events

### NftMint ****&#x20;

```rust
pub struct NftMint<'a> {
    pub owner_id: &'a AccountId,
    pub token_ids: &'a Vec<String>,
    #[serde(skip_serializing_if = "Option::is_none")]
    pub memo: Option<&'a str>,
}
```
