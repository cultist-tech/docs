# Royalty

### Set royalty value

Method sets the provided royalty for the smart contract

```rust
fn set_royalty_value(&mut self, contract_royalty: u32)
```

### Set royalty account

Method sets the royalty account for the smart contract

```rust
fn set_royalty_account(&mut self, account_id: AccountId) -> AccountId
```

### NFT royalty value

Method views current royalty for smart contract

```rust
fn nft_royalty_value(&self) -> u32
```

### NFT royalty account

Method views current smart contract royalty account

```rust
fn nft_royalty_account(&self) -> AccountId
```
