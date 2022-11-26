# The-Graph API

## Queries

### Find Balances

<pre class="language-graphql"><code class="lang-graphql">query ftBalances(
  $first: Int = 10,
  $orderBy: FtBalance_orderBy = id,
  $orderDirection: OrderDirection = asc,
  $skip: Int = 10,
  $where: FtBalance_filter = {}
<strong>) {
</strong>  ftBalances(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...FtBalance
  }
}</code></pre>

### Get Balance

```graphql
query ftBalance($id: ID = "") {
  ftBalance(id: $id) {
    ...FtBalance
  }
}
```

## Fragments

```graphql
fragment FtBalance on FtBalance {
	id: ID!
	contractId: ID!
	accountId: ID!
	balance: BigInt!
	owner: Account!
}
```

