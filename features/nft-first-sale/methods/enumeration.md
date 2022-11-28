# Enumeration

### NFT IDOs

Method views the list of available NFT IDOs

```rust
fn nft_idos(&self) -> Vec<JsonIdo>
```

### NFT IDO

Method views the provided IDO parameters

```rust
fn nft_ido(&self, contract_id: AccountId, ido_id: IdoId) -> Option<JsonIdo>
```

### NFT IDO not minted

Method views the number of NFT tokens available for First Sale with the IDO

```
fn nft_ido_not_minted(&self, contract_id: AccountId, ido_id: IdoId) -> u64
```

### NFT IDO tokens

Method views the list of the tokens available with the IDO

```rust
fn nft_ido_tokens(
        &self,
        contract_id: AccountId,
        ido_id: IdoId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<TokenId>
```

### NFT IDO account minted

Method views the number of NFT tokens that were minted with IDO for the provided account

```rust
fn nft_ido_account_minted(
        &self,
        contract_id: AccountId,
        ido_id: IdoId,
        account_id: AccountId
) -> u64 
```

### NFT IDOs by contract

Method views the list of NFT IDOs for provided NFT smart contract

```rust
fn nft_idos_by_contract(
        &self,
        contract_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<JsonIdo> 
```

### NFT IDOs supply by contact

Method views the total number of NFT tokens available with IDOs for the provided NFT smart contract

```rust
fn nft_idos_supply_by_contract(&self, contract_id: AccountId) -> U128
```
