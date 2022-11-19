# The-Graph API

## Queries

### Find Tokens

```graphql
query tokens($limit: Int!, $offset: Int!, $where: Token_filter! $orderBy: Token_orderBy!, $orderDirection: OrderDirection!) {
  tokens(first: $limit, skip: $offset, where: $where, orderBy: $orderBy, orderDirection: $orderDirection) {
    ...Token
  }
}
```

### Get Token

```graphql
query token($id: ID!)
  token(id: $id) {
    ...Token
  }
}
```

## Fragments

### Nft

```graphql
fragment Nft on Nft {
    id: ID!
    tokenId: String!
    contractId: ID!
    rarity: Int
    bindToOwner: Boolean!
    createdAt: BigInt!
    revealAt: Int
    ownerId: ID!
    tokenMetadataId: ID!
    rentId: ID
    saleId: ID
    fractionationId: ID
    nftIdoId: ID
    owner: Account!
    tokenMetadata: TokenMetadata!
    rent: MarketRent
    sale: MarketSale
    fractionation: NftFractionation
    nftIdo: NftIdo
    nftUpgrade: TokenUpgrade
    nftBurner: TokenBurner
    nftUpgradeId: ID
    nftBurnerId: ID
    royalty: [TokenRoyalty!]!
    stats: [TokenStat!]!
}
```

### NftMetadata
