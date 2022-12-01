# Referral code

### Referral code info

Method returns referral info for the provided code

```rust
fn referral_code_info(&self, code: String) -> Option<ReferralInfo>
```

### Referral program code

Method returns referral code for the program with provided parameters

```rust
fn referral_program_code(
        &self,
        contract_id: ContractId,
        influencer_id: InfluencerId,
        program_id: ProgramId
) -> Option<String>
```

### Referral accept code

Method allows accept referral program for the provided code

```rust
fn referral_accept_code(&mut self, code: String) 
```
