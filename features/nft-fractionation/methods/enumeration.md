# Enumeration

### NFT Fractionation

Method views the fractionation for the provided NFT smart contract token&#x20;

```rust
fn nft_fractionation(
        &self, 
        contract_id: AccountId, 
        token_id: TokenId
) -> Option<Fractionation>
```

### NFT fractionations

Method views the array of fractionations for the provided NFT smart contract

```rust
fn nft_fractionations(
        &self,
        contract_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
    ) -> Vec<Fractionation>
```

### NFT fractionations supply

Method views total number of fractionations for provided NFT smart contract

```rust
fn nft_fractionations_supply(&self, contract_id: AccountId) -> U128
```
