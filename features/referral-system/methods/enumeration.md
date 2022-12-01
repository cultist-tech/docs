# Enumeration

### Referrals by contract

Method views the referrals for provided contract

```rust
fn referrals_by_contract(&self, contract_id: AccountId) -> Vec<AccountId>
```

### Referrals supply by contract

Method views the total number of referrals for provided contract

```rust
fn referrals_supply_by_contract(&self, contract_id: AccountId) -> u128
```

### Referrals by program

Method views the list of referrals for the program with provided parameters

```rust
fn referrals_by_program(
        &self,
        contract_id: AccountId,
        influencer_id: AccountId,
        program_id: String
    ) -> Vec<AccountId>
```

### Referrals supply by program

Method views the total number of referrals for the program with provided parameters

```rust
fn referrals_supply_by_program(
        &self,
        contract_id: AccountId,
        influencer_id: AccountId,
        program_id: String
    ) -> u128 
```

### Referrals by influencer

Method views the list of referrals for the provided influencer

```rust
fn referrals_by_influencer(&self, influencer_id: InfluencerId) -> Vec<AccountId> 
```

### Referrals supply by influencer

Method views the total number of referrals for the provided influencer

```rust
fn referrals_supply_by_influencer(&self, influencer_id: InfluencerId) -> u128 
```

### Referral contracts by influencer

Method views the list of referral contracts for the provided influencer

```rust
fn referral_contracts_by_influencer(
        &self, 
        influencer_id: InfluencerId
) -> Vec<ContractId> 
```

### Referral program by influencer

Method views the list of referral programs for the provided influencer and contract

```rust
fn referral_programs_by_influencer(
        &self,
        influencer_id: InfluencerId,
        contract_id: ContractId
) -> Vec<ProgramId>
```

### Referral influencers by contract

Method views the list of influencers for the provided contract

```rust
fn referral_influencers_by_contract(
        &self, 
        contract_id: ContractId
) -> Vec<InfluencerId>
```

### Referral programs by contract

Method views the list of referral programs for the provided contract and influencer

```rust
fn referral_programs_by_contract(
        &self,
        contract_id: InfluencerId,
        influencer_id: InfluencerId
) -> Vec<ProgramId>
```
