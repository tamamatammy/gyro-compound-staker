# Early Compound Stakers

## Data Source
- The Graph https://thegraph.com/hosted-service/subgraph/graphprotocol/compound-v2
- Google Cloud Bigquery public dataset - ```bigquery-public-data.crypto_ethereum.transactions```  

## Compound V1 - deprecated before June 2019
I cannot find v1 data from the Graph. Instead, I can filter for addresses that supply to compound addresses before the launch of V1 from Google Cloud. Since my google quota is finished, I am not able to provide the actual data. The bigquery query for extracting the addresses are attached as ```compound_stakers_v1.txt```. Query logic is as below:
- Staker supply tokens to the compound pool
- contract address = 0x3fda67f7583380e67ef93072294a7fac882fd7e7
- Supply Method ID = 0xf2b9fdb8
- Filtering logic will be addresses that supplied asset to this contract address before June 2020

## Compound V2 - Launched after June 2019
Addresses are extracted from the Grpah and saved as pickle file ```df_mint_address.pk```
- Extract minter address, acounts that received cToken, before 2020-06-01, graph ql query is as belo:
```
{
 mintEvents(
    where:{blockTime_lt: 1590969213}
    orderBy: blockTime
    orderDirection: desc
  ) {
blockTime
blockNumber
}
}
```
