# Reveal

Reveal feature allows to hide NFT metadata for a certain period of time from minting and than reveal it

### NFT reveal

Method reveals hidden NFT metadata

Requires the _reveal\_at_ option must be specified at the mint time

```rust
fn nft_reveal(&mut self, token_id: TokenId)
```
