# Early Compound Stakers

## Data Source
- Google Cloud Bigquery public data set
- Table: bigquery-public-data.crypto_ethereum.transactions  

## Compound V1 - deprecated before Jund 2019
- Staker supply tokens to the compound pool
- contract address = 0x3fda67f7583380e67ef93072294a7fac882fd7e7
- Supply Method ID = 0xf2b9fdb8
- Filtering logic will be addresses that supplied asset to this contract address before June 2020

## Compound V2 - Launched after June 2019
- Staker supply liquidity to the pool using cTokens
- Search critiria will be limited to minting event (Method Id = 0xa0712d68)
- Filtering logic will be address that minted cTokens before June 2020
- Token Contract Address in https://compound.finance/docs#guides 
