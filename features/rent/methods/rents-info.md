# Rents info

Methods help to get some information about the rents

### Rent token is locked

Method views if NFT token is locked with the rent or not

```rust
fn rent_token_is_locked(&self, contract_id: AccountId, token_id: TokenId) -> bool
```

### Rent is ended

Method views if the NFT token rent time is ended or not

```rust
fn rent_is_ended(&self, contract_id: AccountId, token_id: TokenId) -> bool
```

### Rent is approved

Method views if NFT token is approved for rent for provided account

```rust
fn rent_is_approved(
        &self,
        contract_id: AccountId,
        token_id: TokenId,
        account_id: AccountId
) -> bool
```
