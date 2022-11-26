# Enumeration

Enumeration methods perform view calls to FT smart contract, that shows information about FT state

### FT total supply

Method views the total supply of FT

```rust
fn ft_total_supply(&self) -> U128
```

### FT balance of

Method views the balance of the provided account

```rust
fn ft_balance_of(&self, account_id: AccountId) -> U128
```
