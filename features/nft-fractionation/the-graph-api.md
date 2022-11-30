# The-Graph API

## Queries

### Find nftFractionations

```graphql
query nftFractionations(
  $first: Int = 10, 
  $orderBy: NftFractionation_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: NftFractionation_filter = {}
) {
  nftFractionations(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...NftFractionation
  }
}
```

### Get nftFractionation

```graphql
query nftFractionation($id: ID = "") {
  nftFractionation(id: $id) {
    ...NftFractionation
  }
}
```

### Find nftFractionationParts

```graphql
query nftFractionationParts(
  $first: Int = 10, 
  $orderBy: NftFractionationPart_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: NftFractionationPart_filter = {}
) {
  nftFractionationParts(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...NftFractionationPart
  }
}
```

### Get  nftFractionationPart

```graphql
query nftFractionationPart($id: ID = "") {
  nftFractionationPart(id: $id) {
    ...NftFractionationPart
  }
}
```

## Fragments

### NftFractionation

```graphql
fragment NftFractionation on NftFractionation {
	id: ID!
	contractId: ID!
	nftId: ID!
	createdAt: BigInt!
	competedAt: BigInt
	competedBy: ID
	nft: Nft
	parts: [NftFractionationPart!]!
}
```

### NftFractionationPart

```graphql
fragment NftFractionationPart on NftFractionationPart {
	id: ID!
	contractId: ID!
	nftId: ID!
	ownerId: ID
	fractionation: NftFractionation!
	nft: Nft
}
```
