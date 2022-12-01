# Referrals info

### Referral program

Method shows parameters of referral program

```rust
fn referral_program(
        &self, 
        contract_id: ContractId, 
        influencer_id: InfluencerId, 
        program_id: ProgramId
) -> Option<ReferralProgram>
```

### Referral by

Method returns an Influencer for the contact and account IDs

```rust
fn referral_by(&self, contract_id: AccountId, account_id: AccountId) -> Option<AccountId>
```

### Referral program royalty

Method returns royalty for the program with provided parameters

```rust
fn referral_program_royalty(
        &self,
        contract_id: AccountId,
        influencer_id: InfluencerId,
        program_id: ProgramId
) -> Option<u64> 
```
