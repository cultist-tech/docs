# Enumeration

### Escrow offer

Method views already made offer by the provided offer ID

```rust
fn escrow_offer(&self, offer_id: EscrowOfferId) -> Option<JsonEscrow>
```

### Escrow offers by owner

Method views a list of offers made by the provided account&#x20;

```rust
fn escrow_offers_by_owner(
        &self,
        account_id: AccountId,
        limit: Option<u64>,
        offset: Option<U128>
    ) -> Vec<JsonEscrow>
```

### Escrow offers total by owner

Method views the total number of offers made by the provided account

```rust
fn escrow_offers_total_by_owner(&self, account_id: AccountId) -> u64
```

### Escrow offers for owner

Method views a list of offers made for the provided account

```rust
fn escrow_offers_for_owner(
        &self,
        account_id: AccountId,
        limit: Option<u64>,
        offset: Option<U128>
    ) -> Vec<JsonEscrow>
```

### Escrow offers total for owner

Method views the total number of offers made for the provided account

```rust
fn escrow_offers_total_for_owner(&self, account_id: AccountId) -> u64
```
