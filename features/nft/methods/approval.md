# Approval

Feature implements NEP-178 standard

Approval allows to transfer NFTs on behalf of an owner.

### NFT approve

Method approves provided NFT token for provided account

```rust
fn nft_approve(
        &mut self,
        token_id: TokenId,
        account_id: AccountId,
        msg: Option<String>
) -> Option<Promise>
```

### NFT revoke

Method revokes provided NFT token for provided account

```rust
fn nft_revoke(&mut self, token_id: TokenId, account_id: AccountId)
```

### NFT revoke all

Method revokes provided NFT token for all approved accounts

```rust
fn nft_revoke_all(&mut self, token_id: TokenId)
```

### NFT is approved

Method views if account is approved for NFT token or not

```rust
fn nft_is_approved(
        &self,
        token_id: TokenId,
        approved_account_id: AccountId,
        approval_id: Option<u64>
) -> bool
```
