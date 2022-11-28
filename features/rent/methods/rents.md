# Rents

Rent feature allows to rent NFT tokens at the smart contract

Rent offer may be created by the use of approve mechanics of the NFT contact

### Rent update

Method updates the rent conditions (only before the rent started)

```rust
fn rent_update(
        &mut self,
        contract_id: AccountId,
        token_id: TokenId,
        ft_token_id: &AccountId,
        price_per_hour: U128,
        min_time: u64,
        max_time: u64
)
```

### Rent remove

Method removes rent offer&#x20;

```rust
fn rent_remove(&mut self, contract_id: AccountId, token_id: TokenId)
```

### Rent pay

Method allows to take NFT token into a rent for provided period of time

```rust
fn rent_pay(
        &mut self,
        contract_id: AccountId,
        token_id: TokenId,
        time: u64,
        receiver_id: AccountId
) -> Promise 
```

### Rent claim

Method allows to take NFT token back to owner, when the rent is ended.

```rust
fn rent_claim(&mut self, contract_id: AccountId, token_id: TokenId) -> Promise
```
