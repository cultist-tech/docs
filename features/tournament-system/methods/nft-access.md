# NFT access

### Tournament add NFT access

Method allows further access to the tournament using one of the provided tokens

```rust
fn tournament_add_nft_access(
        &mut self, 
        tournament_id: TournamentId, 
        token_ids: Vec<TokenId>
) 
```

### Tournament NFT access&#x20;

Method views the list of tokens that can be used to access the tournament

```rust
fn tournament_nft_access(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId
) -> Vec<TokenId> 
```

### Use NFT access

The player can join the tournament by the use of NFT transfer call of the NFT smart contract. The NFT transfer of certain token must be addressed to the tournament contract with provided TournamentOnNftTransferArgs message containing an empty "place" field.
