# Transfer

Transfer is a base feature that allows to send NFT to another users or smart contracts

### NFT transfer

Method initiates the transfer of the token to another valid user (optional fields can be omitted)

```rust
pub fn nft_transfer(
        &mut self,
        receiver_id: ValidAccountId,
        token_id: TokenId,
        approval_id: Option<u64>,
        memo: Option<String>,
)
```

### NFT transfer call

Method initiates the transfer of the token to another smart contract (optional fields can be omitted)

```rust
fn nft_transfer_call(
        &mut self,
        receiver_id: AccountId,
        token_id: TokenId,
        approval_id: Option<u64>,
        memo: Option<String>,
        msg: String,
) -> PromiseOrValue<bool>
```
