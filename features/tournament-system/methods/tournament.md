# Tournament

### Tournament create

Method creates tournament with provided parameters

```rust
fn tournament_create(
        &mut self,
        tournament_id: TournamentId,
        players_number: u8,
        price: Option<U128>,
        name: String,
        media: Option<String>,
        summary: Option<String>,
        nft_access_contract: Option<AccountId>
) 
```

### Tournament add whitelist prize owner

Method adds the account to the whitelist of accounts which can add some prizes for certain places in the tournament

```rust
fn tournament_add_whitelist_prize_owner(
        &mut self,
        tournament_id: TournamentId,
        account_id: AccountId
)
```

### Tournament add prize

Method adds the tournament prize for the provided place number, nominated in NEAR

```rust
fn tournament_add_prize(
        &mut self,
        tournament_id: TournamentId,
        owner_id: AccountId,
        place_number: u8,
        prize_id: String
) 
```

### Tournament add FT prize

FT prize can be added by the use of FT transfer call of the FT smart contract. The FT transfer of prize amount of tokens must be addressed to the tournament contract with provided TournamentOnFtTransferArgs message for the certain place in tournament.

### Tournament add NFT prize

NFT token prize can be added by the use of NFT transfer call of the NFT smart contract. The NFT transfer of prize token must be addressed to the tournament contract with provided TournamentOnNftTransferArgs message for the certain place in tournament.

### Tournament join

Method allows users to join the tournament with the provided ID and with attached join price, nominated in NEAR, while it is not started

```rust
fn tournament_join(&mut self, tournament_id: TournamentId, owner_id: AccountId)
```

### Tournament start

Method checks the tournament is filled with the players, and mark it as started

```rust
fn tournament_start(&mut self, tournament_id: TournamentId)
```

### Tournament end

Method marks the tournament as ended

```rust
fn tournament_end(&mut self, tournament_id: TournamentId)
```

### Tournament execute reward

Method rewards the account with the prize for the provided place after the tournament ends

```rust
fn tournament_execute_reward(
        &mut self,
        tournament_id: TournamentId,
        winner_place: u8,
        account_id: AccountId
)
```

