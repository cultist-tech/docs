# Structures

### JsonEscrow

```rust
pub struct JsonEscrow {
    pub offer_id: EscrowOfferId,
    pub data: EscrowEnum,
    pub sender_id: AccountId,
    pub receiver_id: AccountId,
    pub is_accepted: bool,
}
```

### EscrowEnum

```rust
pub enum EscrowEnum {
    FtToFt {
        ft_contract_id_in: ContractId,
        amount_in: U128,

        ft_contract_id_out: ContractId,
        amount_out: U128,
    },
    FtToNft {
        ft_contract_id_in: ContractId,
        amount_in: U128,

        nft_contract_id_out: ContractId,
        nft_token_id_out: TokenId,
    },
    NftToFt {
        nft_contract_id_in: ContractId,
        nft_token_id_in: TokenId,

        ft_contract_id_out: ContractId,
        amount_out: U128,
    },
    NftToNft {
        nft_contract_id_in: ContractId,
        nft_token_id_in: TokenId,

        nft_contract_id_out: ContractId,
        nft_token_id_out: TokenId,
    },
}
```

### EscrowOnFtTransferArgs

```rust
pub struct EscrowOnFtTransferArgs {
    pub ft_contract_id_out: Option<ContractId>,
    pub ft_amount_out: Option<U128>,

    pub nft_contract_id_out: Option<ContractId>,
    pub nft_token_id_out: Option<TokenId>,

    pub receiver_id: Option<AccountId>,
    pub offer_id: Option<EscrowOfferId>,
}
```

### EscrowOnNftTransferArgs

```rust
pub struct EscrowOnNftTransferArgs {
    pub ft_contract_id_out: Option<ContractId>,
    pub ft_amount_out: Option<U128>,

    pub nft_contract_id_out: Option<ContractId>,
    pub nft_token_id_out: Option<TokenId>,

    pub receiver_id: Option<AccountId>,
    pub offer_id: Option<EscrowOfferId>,
}
```

### EscrowOfferId

```rust
pub type EscrowOfferId = String;
```
