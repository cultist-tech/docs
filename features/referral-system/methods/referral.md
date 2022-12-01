# Referral

### Referral create program

Method allows create a referral program with provided parameters

```rust
fn referral_create_program(
        &mut self,
        influencer_id: AccountId,
        program_id: ProgramId,
        royalty_percent: Option<u64>,
        metadata: Option<ReferralProgramMetadata>
)
```

### Referral accept

Method allows accept referral program

```rust
fn referral_accept(
        &mut self,
        contract_id: AccountId,
        influencer_id: AccountId,
        program_id: ProgramId
) 
```
