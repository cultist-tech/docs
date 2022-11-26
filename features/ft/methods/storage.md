# Storage

Storage methods manage the storage costs of FT internal data payed by users

### Storage deposit

Method reserves storage space for FTs according to attached deposit amount

```rust
fn storage_deposit(
        &mut self,
        account_id: Option<AccountId>,
        registration_only: Option<bool>
) -> StorageBalance
```

### Storage withdraw

Method withdraws funds payed for reserved storage space for FTs

```rust
fn storage_withdraw(&mut self, amount: Option<U128>) -> StorageBalance
```

### Storage unregister

Method unregisters user from FT smart contract and returns funds payed for reserved storage space for FTs

```rust
fn storage_unregister(&mut self, force: Option<bool>) -> bool
```

### Storage balance bounds

Method views min and max storage balance bounds

```rust
fn storage_balance_bounds(&self) -> StorageBalanceBounds
```

### Storage balance of

Method views storage balance of provided user

```rust
fn storage_balance_of(&self, account_id: AccountId) -> Option<StorageBalance>
```
