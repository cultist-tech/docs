# The-Graph API

## Queries

### Find NFT IDOs

```graphql
query nftIdos(
  $first: Int = 10, 
  $orderBy: NftIdo_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $where: NftIdo_filter = {}
) {
  nftIdos(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    where: $where
  ) {
    ...NftIdo
  }
}
```

### Get NFT IDO

```graphql
query nftIdo($id: ID = "") {
  nftIdo(id: $id) {
    ...NftIdo
  }
}
```

## Fragments

```graphql
fragment NftIdo on NftIdo {
	id: ID!
	idoId: ID!
	contractId: ID!
	name: String!
	media: String
	amount: Int
	price: String!
	buyMax: Int!
	perTransactionMin: Int!
	perTransactionMax: Int!
	amountReady: Int!
	notMinted: Int!
	locked: Boolean!
	startDate: Int
	ftToken: String
	nfts: [Nft!]!
}
```
