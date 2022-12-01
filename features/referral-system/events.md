# Events

### ProgramCreate

```rust
pub struct ProgramCreate<'a> {
    pub contract_id: &'a AccountId,
    pub influencer_id: &'a AccountId,
    pub program_id: &'a String,
    pub royalty_percent: &'a Option<u64>,
    pub code: &'a String,
    pub metadata: &'a Option<ReferralProgramMetadata>,
}
```

### ReferralAccept

```rust
pub struct ReferralAccept<'a> {
    pub contract_id: &'a AccountId,
    pub influencer_id: &'a AccountId,
    pub program_id: &'a String,
    pub account_id: &'a AccountId,
}
```
