# NFT to NFT

### NFT to NFT offer create

NFT to NFT offer can be created by the use of NFT transfer call of the NFT smart contract. The NFT transfer of some token must be addressed to the contract that implements escrow feature with provided EscrowOnNftTransferArgs message, that specifies the receiver of the exchange, NFT smart contract to exchange with and an NFT token that is expected.

### NFT to NFT offer accept

NFT to NFT offer can be accepted by the receiver with the use of NFT transfer call of the NFT smart contract, which token offer expects to receive. The NFT transfer of expected in offer token must be addressed to the contract that implements escrow feature, with provided EscrowOnNFtTransferArgs message, that specifies the exchange offer ID.

###
