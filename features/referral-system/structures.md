# Structures

### ReferralInfo

```graphql
pub struct ReferralInfo {
    pub contract_id: ContractId,
    pub influencer_id: InfluencerId,
    pub program_id: ProgramId,
}
```

### ReferralProgram

```rust
pub struct ReferralProgram {
    pub contract_id: ContractId,
    pub influencer_id: InfluencerId,
    pub program_id: ProgramId,
    pub metadata: Option<ReferralProgramMetadata>,
    pub code: String,
}
```

### ReferralProgramMetadata

```rust
pub struct ReferralProgramMetadata {
    pub title: Option<String>,
    pub media: Option<String>,
    pub description: Option<String>,
    pub url: Option<String>,
}
```
