# Enumeration

### Rent total supply

Method views how much NFT tokens are exposed for rent

```rust
fn rent_total_supply(&self) -> u64
```

### Rents

Method views all smart contract rents

```rust
fn rents(&self, from_index: Option<U128>, limit: Option<u64>) -> Vec<JsonRen
```

### Rents for account

Method views all rents that are exposed by the provided account

```rust
fn rents_for_account(
        &self,
        account_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<JsonRent> 
```

### Rents by ID

Method views the rent conditions for the provided array of NFT tokens

```rust
fn rents_by_ids(&self, ids: Vec<TokenId>) -> Vec<JsonRent>
```

### Rent supply for account

Method views total number of rents exposed by provided account

```rust
fn rents_supply_for_account(&self, account_id: AccountId) -> U128
```

### Rent

Method views rent conditions for provided NFT token

```rust
fn rent(&self, contract_id: AccountId, token_id: TokenId) -> Option<JsonRent>
```

### Rent tokens for account

Method views the rents that were made by provided account

```rust
fn rented_tokens_for_account(
        &self,
        account_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<JsonRent> 
```

### Rented tokens supply for account

Method views total number of tokens rented by provided account

```rust
fn rented_tokens_supply_for_account(&self, account_id: AccountId) -> U128
```

### Rents by contract

Method views the rents for provided NFT contract

```rust
fn rents_by_contract(
        &self,
        contract_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<JsonRent>
```

### Rents supply by contract

Method views total number of rents for provided contract

```rust
fn rents_supply_by_contract(&self, contract_id: AccountId) -> U128
```
