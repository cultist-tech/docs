# Structures

### Tournament

```rust
pub struct Tournament {
    pub tournament_id: TournamentId,
    pub owner_id: AccountId,
    pub access_nft_contract: Option<AccountId>,

    pub players_number: u8,
    pub price: Option<U128>,

    pub started_at: Option<u64>,
    pub ended_at: Option<u64>,
    pub created_at: u64,
}
```

### TournamentMetadata

```rust
pub struct TournamentMetadata {
    pub name: String,
    pub media: Option<String>,
    pub summary: Option<String>,
}
```

### JsonTournament

```rust
pub struct JsonTournament {
    pub tournament_id: TournamentId,    
    pub owner_id: AccountId,    
    pub metadata: TournamentMetadata,

    pub access_nft_contract: Option<AccountId>,
    pub price: Option<U128>,

    pub players_total: u8,
    pub players_current: u8,

    pub started_at: Option<u64>,
    pub ended_at: Option<u64>,
    pub created_at: u64,
}
```

```rust
pub enum RewardPrize {
    Near {
        amount: U128,
        owner_id: Option<AccountId>,
    },
    Ft {
        ft_contract_id: AccountId,
        amount: U128,
        owner_id: Option<AccountId>,
    },
    Nft {
        nft_contract_id: AccountId,
        token_id: TokenId,
        owner_id: Option<AccountId>,
    },
}
```

### TournamentOnFtTransferArgs

```rust
pub struct TournamentOnFtTransferArgs {    
    pub tournament_id: TournamentId,
    pub owner_id: AccountId,
    pub place: Option<u8>,
    pub prize_id: Option<PrizeId>,
}
```

### TournamentOnNftTransferArgs

```rust
pub struct TournamentOnNftTransferArgs {
    pub tournament_id: TournamentId,
    pub owner_id: AccountId,
    pub place: Option<WinnerPlace>,
    pub prize_id: Option<PrizeId>,
}
```
