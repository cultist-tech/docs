# FT to NFT

### FT to NFT offer create

FT to NFT offer can be created by the use of FT transfer call of the FT smart contract. The FT transfer of some amount must be addressed to the contract that implements escrow feature with provided EscrowOnFtTransferArgs message, that specifies the receiver of the exchange, NFT smart contract to exchange with and an NFT token that is expected.

### FT to NFT offer accept

FT to NFT offer can be accepted by the receiver with the use of NFT transfer call of the NFT smart contract, which token offer expects to receive. The NFT transfer of expected in offer token must be addressed to the contract that implements escrow feature, with provided EscrowOnNFtTransferArgs message, that specifies the exchange offer ID.
