# Fractionation

### NFT fractionation create

Fractionation can be created by the use of NFT transfer call of the NFT smart contract. The NFT transfer of fractionating token must be addressed to the contract that implements fractionation feature with provided list of NFT tokens ids that must be used to complete fractionation.

### NFT fractionation process

Fractionation can be completed by the use of NFT transfer call of NFT smart contract used.  The NFT transfer of fraction tokens must be addressed to the fractionation contract.

### NFT fractionation complete

Method allows to get fractionating token, after transfer of all the NFT tokens specified at fractionation creation.

```rust
fn nft_fractionation_complete(
        &mut self, 
        contract_id: AccountId, 
        token_id: FractionationId
)
```
