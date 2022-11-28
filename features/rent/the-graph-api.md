# The-Graph API

## Queries

### Find MarketRents

```graphql
query marketRents($first: Int = 10, $orderBy: MarketRent_orderBy = id, $orderDirection: OrderDirection = asc, $skip: Int = 10, $where: MarketRent_filter = {}) {
  marketRents(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...MarketRent
  }
}
```

### Get MarketRent

```graphql
query marketRent($id: ID = "") {
  marketRent(id: $id){
    ...MarketRent
  }
}
```

### Find MarketRentConditions

```graphql
query marketRentConditions($first: Int = 10, $orderBy: MarketRentCondition_orderBy = id, $orderDirection: OrderDirection = asc, $skip: Int = 10, $where: MarketRentCondition_filter = {}) {
  marketRentConditions(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...MarketRentCondition
  }
}

```

### Get MarketRentCondition

```graphql
query marketRentCondition($id: ID = "") {
  marketRentCondition(id: $id) {
    ...MarketRentCondition
  }
}
```

## Fragments

```graphql
fragment MarketRent on MarketRent {
	id: ID!
	contractId: ID!
	nftId: ID!
	ownerId: ID!
	minTime: Int!
	maxTime: Int!
	endedAt: Int
	createdAt: BigInt!
	renterId: ID
	owner: Account!
	nft: Nft!
	conditions: [MarketRentCondition!]!
}
```

### MarketRentCondition

```graphql
fragment MarketRentCondition on MarketRentCondition {
	id: ID!
	ftTokenId: ID!
	price: String!
	rent: MarketRent!
	rentId: ID!
}
```
