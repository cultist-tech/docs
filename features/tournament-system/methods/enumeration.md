# Enumeration

### Tournament

Method views the tournament with provided ID

```rust
fn tournament(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId
) -> Option<JsonTournament>
```

### Tournaments

Method views the list tournaments for provided owner account

```rust
fn tournaments(
        &self,
        owner_id: AccountId,
        from_index: Option<U128>,
        limit: Option<u64>
) -> Vec<JsonTournament>
```

### Tournament players

Method views the list of joined the tournament players

```rust
fn tournament_players(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId
) -> Vec<AccountId>
```

### Tournament prizes

Method views the place-prize map for the provided tournament

```rust
fn tournament_prizes(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId
) -> HashMap<WinnerPlace, Vec<RewardPrize>>
```

### Tournament free places

Method views the number of the free places for the provided tournament

```rust
fn tournament_free_places(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId
) -> Option<u64>
```

### Tournament member

Method views if the provided account is a member of the tournament, or not

```rust
fn tournament_member(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId,
        account_id: AccountId
) -> bool 
```

### Tournament is whitelist prize owner

Method views if the provided account is able to provide the prizes to the tournament contract, or not

```rust
fn tournament_is_whitelist_prize_owner(
        &self,
        tournament_id: TournamentId,
        owner_id: AccountId,
        account_id: AccountId
) -> bool
```

### Tournament whitelist prize owners

Method views the list of accounts that are able to provide prizes for the tournament

```rust
fn tournament_whitelist_prize_owners(
        &self, 
        tournament_id: TournamentId, 
        owner_id: AccountId
) -> Vec<AccountId>
```
