# NFT to FT

### NFT to FT offer create

NFT to FT offer can be created by the use of NFT transfer call of the NFT smart contract. The NFT transfer of some token must be addressed to the contract that implements escrow feature with provided EscrowOnNftTransferArgs message, that specifies the receiver of the exchange, FT smart contract to exchange with and an amount of FT tokens for that exchange expected.

### NFT to FT accept

NFT to FT offer can be accepted by the receiver with the use of FT transfer call of the FT smart contract, which tokens offer expects to receive. The FT transfer of expected in offer amount must be addressed to the contract that implements escrow feature, with provided EscrowOnFtTransferArgs message, that specifies the exchange offer ID.
