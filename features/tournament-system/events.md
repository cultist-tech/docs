# Events

### TournamentCreate

```rust
pub struct TournamentCreate<'a> {
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
    pub players_number: &'a u8,
    pub price: &'a Option<U128>,
}
```

### TournamentJoin

```rust
pub struct TournamentJoin<'a> {
    pub account_id: &'a AccountId,
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
}
```

### TournamentStart

```rust
pub struct TournamentStart<'a> {
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
    pub date: &'a u64,
}
```

### TournamentEnd

```rust
pub struct TournamentEnd<'a> {
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
    pub date: &'a u64,
}
```

### TournamentReward

```rust
pub struct TournamentReward<'a> {
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
    pub place: &'a u8,
    pub prize: &'a RewardPrize,
}
```

### TournamentAddPrize

```rust
pub struct TournamentAddPrize<'a> {
    pub tournament_id: &'a TournamentId,
    pub owner_id: &'a AccountId,
    pub prize: &'a RewardPrize,
}
```

### TournamentAddNftAccess

```rust
pub struct TournamentAddNftAccess<'a> {
    pub tournament_id: &'a String,
    pub owner_id: &'a AccountId,
    pub token_ids: &'a Vec<TokenId>,
}
```
