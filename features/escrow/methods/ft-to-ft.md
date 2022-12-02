# Ft to FT

### FT to FT offer create

FT to FT offer can be created by the use of FT transfer call of the FT smart contract. The FT transfer of some amount must be addressed to the contract that implements escrow feature with provided EscrowOnFtTransferArgs message, that specifies the receiver of the exchange, FT smart contract to exchange with and an amount of FT tokens for that exchange expected.

### FT to FT offer accept

FT to FT offer can be accepted by the receiver with the use of FT transfer call of the FT smart contract, which tokens offer expects to receive. The FT transfer of expected in offer amount must be addressed to the contract that implements escrow feature, with provided EscrowOnFtTransferArgs message, that specifies the exchange offer ID.
