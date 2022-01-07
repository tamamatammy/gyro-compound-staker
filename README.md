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
- Token Contract Address in 
- 
        '0xe65cdb6479bac1e22340e4e755fae7e509ecd06c'	--Compound: cAAVE Token	
        '0x70e36f6bf80a52b3b46b3af8e106cc0ed743e8e4'	--Compound: cCOMP Token	
        '0xface851a4921ce59e912d19329929ce6da6eb0c7'	--Compound: cLink Token
        '0x95b4ef2869ebd94beb4eee400a99824bf5dc325b'	--Compound: cMKR Token
        '0xf5dce57282a584d2746faf1593d3121fcac444dc'	--Compound: cSAI Token
        '0x4b0181102a0112a2ef11abee5563bb4a3176c9d7'	--Compound: cSushi Token
        '0x12392f67bdf24fae0af363c24ac620a2f67dad86'	--Compound: cTUSD Token
        '0xccf4429db6322d5c611ee964527d42e5d685dd6a'	--Compound: cWBTC2 Token
        '0x80a2ae356fc9ef4305676f7a3e2ed04e12c33946'  --Compound: cYFI Token
