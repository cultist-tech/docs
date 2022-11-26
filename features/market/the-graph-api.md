# The-Graph API

## Queries

### Find MarketSales

```graphql
query marketSales(
  $first: Int = 10,
  $orderBy: MarketSale_orderBy = id,
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: MarketSale_filter = {}
) {
  marketSales(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...MarketSale
  }
}

```

### Get MarketSale

```graphql
query marketSale($id: ID = "") {
  marketSale(id: $id){
    ...MarketSale
  }
}
```

### Find marketSaleCondition

```graphql
query marketSale(
  $id: ID = "", 
  $first: Int = 10, 
  $orderBy: MarketSaleCondition_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: MarketSaleCondition_filter = {}
) {
  marketSaleConditions(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...marketSaleCondition
  }
}

```

### Get marketSaleCondition

```graphql
query marketSaleCondition($id: ID = "") {
  marketSaleCondition(id: $id){
    ...marketSaleCondition
  }
}
```

## Fragments

### MarketSale

```graphql
fragment MarketSale on MarketSale {
	id: ID!
	ownerId: ID!
	contractId: ID!
	nftId: ID!
	isAuction: Boolean!
	createdAt: BigInt!
	owner: Account!
	nft: Nft!
	isDeleted: Boolean!
	conditions: [MarketSaleCondition!]!
}
```

### MarketSaleCondition

```graphql
fragment MarketSaleCondition on MarketSaleCondition {
	id: ID!
	ftTokenId: ID!
	price: String!
	sale: MarketSale!
	saleId: ID!
}
```
