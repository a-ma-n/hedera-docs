# TokenTransferList

A list of token IDs and amounts representing the transferred out (negative) or into (positive) amounts, represented in the lowest denomination of the token.

| Field               | Type                                       | Description                                                                                                                                                                |
| ------------------- | ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `token`             | [TokenID](tokenid.md)                      | The ID of the token                                                                                                                                                        |
| `transfers`         | repeated [AccountAmount](accountamount.md) | Multiple list of AccountAmounts, each of which has an account and amount                                                                                                   |
| `nftTransfers`      | repeated [NftTransfers](nfttransfer.md)    | Applicable to tokens of type NON\_FUNGIBLE\_UNIQUE. Multiple list of NftTransfers, each of which has a sender and receiver account, including the serial number of the NFT |
| `expected_decimals` | google.protobuf.UInt32Value                | If present, the number of decimals this fungible token type is expected to have. The transfer will fail with UNEXPECTED\_TOKEN\_DECIMALS if the actual decimals differ.    |

