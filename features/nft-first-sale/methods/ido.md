# IDO

### NFT IDO add

Method creates new IDO with provided parameters. After creation NFT tokens may be sent to the IDO smart contract using NFT transfer call mechanics of the NFT smart contract.

```rust
fn nft_ido_add(
        &mut self,
        contract_id: AccountId,
        ido_id: IdoId,
        name: String,
        amount: u64,
        price: U128,
        per_transaction_min: u64,
        per_transaction_max: u64,
        buy_max: u64,
        ft_token: Option<AccountId>,
        media: Option<String>
    ) -> JsonIdo
```

### NFT IDO start

Method starts an IDO, making it available to buy

```rust
fn nft_ido_start(&mut self, contract_id: AccountId, ido_id: IdoId, date: u64) -> JsonIdo
```

### NFT IDO update

Method updates NFT IDO parameters. Can be called only from the NFT contract, and while the IDO is not started yet

```rust
fn nft_ido_update(
        &mut self,
        contract_id: AccountId,
        ido_id: IdoId,
        date: u64,
        per_transaction_min: u64,
        per_transaction_max: u64,
        buy_max: u64
    ) -> JsonIdo
```

### NFT IDO pause

Method makes NFT IDO available or not, according to the pause parameter value

```rust
fn nft_ido_pause(
        &mut self,
        contract_id: AccountId, 
        ido_id: IdoId, 
        pause: bool
) -> JsonIdo
```

### NFT IDO buy

Method allows to buy NFT IDO with specified amount of the NFT tokens for NEAR native token. Also NFT IDO tokens can be bought using FT transfer call mechanics of FT smart contract.

```rust
fn nft_ido_buy(
        &mut self,
        contract_id: AccountId,
        receiver_id: AccountId,
        ido_id: IdoId,
        amount: u64
) 
```
