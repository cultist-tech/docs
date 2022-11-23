# The-Graph API

## Queries

### Find Tokens

```graphql
query nfts($limit: Int!, $offset: Int!, $where: Nft_filter! $orderBy: Nft_orderBy!, $orderDirection: OrderDirection!) {
  nfts(first: $limit, skip: $offset, where: $where, orderBy: $orderBy, orderDirection: $orderDirection) {
    ...Nft
  }
}
```

### Get Token

```graphql
query nft($id: ID!)
  nft(id: $id) {
    ...Nft
  }
}
```

## Fragments

### Nft

```graphql
fragment Nft on Nft {
	id: ID!
	nftId: String!
	contractId: ID!
	rarity: Int
	bindToOwner: Boolean!
	createdAt: BigInt!
	revealAt: Int
	ownerId: ID!
	nftMetadataId: ID!
	rentId: ID
	saleId: ID
	fractionationId: ID
	nftIdoId: ID
	owner: Account!
	nftMetadata: NftMetadata!
	rent: MarketRent
	sale: MarketSale
	fractionation: NftFractionation
	nftIdo: NftIdo
	nftUpgrade: NftUpgrade
	nftBurner: NftBurner
	nftUpgradeId: ID
	nftBurnerId: ID
	royalty: [NftRoyalty!]!
	stats: [NftStat!]!
}
```

### NftMetadata

```graphql
fragment NftMetadata on NftMetadata {
	id: ID!
	title: String
	description: String
	media: String
	nftId: String!
}
```

### NftRoyalty

```graphql
fragment NftRoyalty on NftRoyalty {
	id: ID!
	nftId: ID!
	accountId: String!
	value: Int!
	nft: Nft!
}
```

### NftStat

```graphql
fragment NftStat on NftStat {
	id: ID!
	nftId: ID!
	nft: Nft!
	key: String!
	value: String!
}
```

### NftUpgrade

```graphql
fragment NftUpgrade on NftUpgrade {
	id: ID!
	rarity: Int!
	ftTokenId: ID!
	price: String!
}
```

### NftBurner

```rust
fragment NftBurner on NftBurner {
	id: ID!
	rarity: Int!
	rarity_sum: Int!
}
```
