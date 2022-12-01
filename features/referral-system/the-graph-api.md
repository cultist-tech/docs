# The-Graph API

## Queries

### Find Referrals

```graphql
query referrals(
  $first: Int = 10, 
  $orderBy: Referral_orderBy = id, 
  $where: Referral_filter = {}, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10
) {
  referrals(
    first: $first
    orderBy: $orderBy
    where: $where
    orderDirection: $orderDirection
    skip: $skip
  ) {
    ...Referral
  }
}
```

### Get Referral

```graphql
query referral($id: ID = "") {
  referral(id: $id) {
    ...Referral
  }
}
```

### Find ReferralPrograms

```graphql
query referralPrograms(
  $first: Int = 10, 
  $orderBy: ReferralProgram_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralProgram_filter = {}
) {
  referralPrograms(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...ReferralProgram
  }
}

```

### Get ReferralProgram

```rust
query referralProgram($id: ID = "") {
  referralProgram(id: $id) {
    ...ReferralProgram
  }
}
```

### Find  ReferralContracts

```graphql
query referralContracts(
  $first: Int = 10, 
  $orderBy: ReferralContract_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $where: ReferralContract_filter = {}
) {
  referralContracts(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    where: $where
  ) {
    ...ReferralContract
  }
}
```

### Get ReferralContract

```graphql
query referralContract($id: ID = "") {
  referralContract(id: $id) {
    ...ReferralContract
  }
}
```

### Find ReferralContractInfluencer

```graphql
query referralContractInfluencers(
  $first: Int = 10, 
  $orderBy: ReferralContractInfluencer_orderBy = id,   
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralContractInfluencer_filter = {}
) {
  referralContractInfluencers(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...ReferralContractInfluencer
  }
}
```

### Get ReferralContractInfluencer

```graphql
query referralContractInfluencer($id: ID = "") {
  referralContractInfluencer(id: $id) {
    ...ReferralContractInfluencer
  }
}
```

### Find ReferralInfluencer

```graphql
query referralInfluencers(  
  $first: Int = 10, 
  $orderBy: ReferralInfluencer_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralInfluencer_filter = {}
) {
  referralInfluencers(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...ReferralInfluencer
  }
}
```

### Get ReferralInfluencer

```graphql
query referralInfluencer($id: ID = "") {
  referralInfluencer(id: $id) {
    ...ReferralInfluencer
  }
}
```

### Find ReferralInfluencerContract

```graphql
query referralInfluencerContracts(
  $first: Int = 10, 
  $orderBy: ReferralInfluencerContract_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralInfluencerContract_filter = {}
) {
  referralInfluencerContracts(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...ReferralInfluencerContract
  }
}
```

### Get ReferralInfluencerContract

```graphql
query referralInfluencerContract($id: ID = "") {
  referralInfluencerContract(id: $id) {
    ...ReferralInfluencerContract
  }
}
```

### Find ReferralProgramVolume

```graphql
query referralProgramVolumes(
  $first: Int = 10, 
  $orderBy: ReferralProgramVolume_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralProgramVolume_filter = {}
) {
  referralProgramVolumes(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {
    ...ReferralProgramVolume
  }
}
```

### Get ReferralProgramVolume

```graphql
query referralProgramVolume($id: ID = "") {
  referralProgramVolume(id: $id) {
    ...ReferralProgramVolume
  }
}
```

### Find ReferralContractVolume

```graphql
query referralContractVolumes(
  $first: Int = 10, 
  $orderBy: ReferralContractVolume_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $where: ReferralContractVolume_filter = {}
) {
  referralContractVolumes(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    where: $where
  ) {
    ...ReferralContractVolume
  }
}
```

### Get ReferralContractVolume

```graphql
query referralContractVolume($id: ID = "") {
  referralContractVolume(id: $id) {
    ...ReferralContractVolume
  }
}
```

### Find ReferralInfluencerVolume

```graphql
query referralInfluencerVolumes(
  $first: Int = 10, 
  $orderBy: ReferralInfluencerVolume_orderBy = id, 
  $orderDirection: OrderDirection = asc, 
  $skip: Int = 10, 
  $where: ReferralInfluencerVolume_filter = {}
) {
  referralInfluencerVolumes(
    first: $first
    orderBy: $orderBy
    orderDirection: $orderDirection
    skip: $skip
    where: $where
  ) {    
    ...ReferralInfluencerVolume
  }
}
```

### Get ReferralInfluencerVolume

```graphql
query referralInfluencerVolume($id: ID = "") {
  referralInfluencerVolume(id: $id) {
    ...ReferralInfluencerVolume
  }
}
```

## Fragments

### Referral

```graphql
fragment Referral on Referral {
	id: ID!
	contractId: ID!
	influencerId: ID!
	programId: ID!
	accountId: ID!
	payoutCount: Int!
	payoutNear: String!
	contract: ReferralContract!
	influencer: ReferralInfluencer!
	program: ReferralProgram!
	account: Account!
	createdAt: BigInt!
}
```

### ReferralProgram

```graphql
fragment ReferralProgram on ReferralProgram {
	id: ID!
	contractId: ID!
	influencerId: ID!
	programId: ID!
	code: String!
	royalty_percent: Int!
	title: String
	description: String
	media: String
	url: String
	referralsCount: Int!
	activeReferralsCount: Int!
	payoutCount: Int!
	payoutNear: String!
	createdAt: BigInt!
	contract: ReferralContract!
	influencer: ReferralInfluencer!
}
```

### ReferralContract

```graphql
fragment ReferralContract on ReferralContract {
	id: ID!
	contractId: ID!
	influencersCount: Int!
	programsCount: Int!
	referralsCount: Int!
	activeReferralsCount: Int!
	payoutCount: Int!
	payoutNear: String!
	createdAt: BigInt!
	programs: [ReferralProgram!]!
}
```

### ReferralContractInfluencer

```graphql
fragment ReferralContractInfluencer on  ReferralContractInfluencer {
	id: ID!
	contractId: ID!
	influencerId: ID!
	programsCount: Int!
	referralsCount: Int!
	activeReferralsCount: Int!
	payoutCount: Int!
	payoutNear: String!
	createdAt: BigInt!
}
```

### ReferralInfluencer

```graphql
fragment ReferralInfluencer on ReferralInfluencer {
	id: ID!
	influencerId: ID!
	contractsCount: Int!
	programsCount: Int!
	referralsCount: Int!
	activeReferralsCount: Int!
	payoutCount: Int!
	payoutNear: String!
	createdAt: BigInt!
	programs: [ReferralProgram!]!
}
```

### ReferralInfluencerContract

```graphql
fragment ReferralInfluencerContract on ReferralInfluencerContract {
	id: ID!
	influencerId: ID!
	contractId: ID!
	programsCount: Int!
	referralsCount: Int!
	activeReferralsCount: Int!
	payoutCount: Int!
	payoutNear: String!
	createdAt: BigInt!
}
```

### ReferralProgramVolume

```graphql
fragment ReferralProgramVolume on ReferralProgramVolume {
	id: ID!
	contractId: ID!
	influencerId: ID!
	programId: ID!
	ftTokenId: ID!
	amount: String!
}
```

### ReferralContractVolume

```graphql
fragment ReferralContractVolume on ReferralContractVolume {
	id: ID!
	contractId: ID!
	ftTokenId: ID!
	amount: String!
}
```

### ReferralInfluencerVolume

```graphql
fragment ReferralInfluencerVolume on ReferralInfluencerVolume {
	id: ID!
	influencerId: ID!
	ftTokenId: ID!
	amount: String!
}
```
