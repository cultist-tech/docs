# Payout

Feature implements NEP-199 standard

Payout Feature allows NFT contracts to request that financial contracts pay-out multiple receivers, enabling flexible royalty implementations

### NFT payout

Method views the payout mapping for the provided token with the provided balance

```rust
fn nft_payout(&self, token_id: String, balance: U128, max_len_payout: u32) -> Payout
```

### NFT transfer payout

Method calculates the payout with the provided balance, calls nft\_transfer, and returns the payout mapping

```rust
fn nft_transfer_payout(
        &mut self,
        receiver_id: AccountId,
        token_id: TokenId,
        approval_id: u64,
        balance: U128,
        max_len_payout: u32,
        memo: Option<String>
) -> Payout
```
