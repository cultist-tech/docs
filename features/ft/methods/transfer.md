# Transfer

Transfer feature allows to send FT to another users or smart contracts

### FT transfer

Method initiates the transfer of the certain amount of the tokens to another valid user (optional fields can be omitted)

```rust
fn ft_transfer(
        &mut self,
        receiver_id: AccountId,
        amount: U128,
        memo: Option<String>
)
```

### FT transfer call

Method initiates the transfer of the certain amount of the tokens to another smart contract (optional fields can be omitted)

```rust
fn ft_transfer_call(
        &mut self,
        receiver_id: AccountId,
        amount: U128,
        memo: Option<String>,
        msg: String
) -> PromiseOrValue<U128>
```
