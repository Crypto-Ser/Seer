# Tech

### Pluging everything together

In this project, we didn't write any new code but plugged together existing tools to create a subsidized prediction market.
Note that this was still a technical project as it required reading docs, code, hacking around buggy UI, making direct smart contract call.
It's using a patchwork of different projects and interfaces (open execution and money legos), but everythings works and is fully decentralized and censorship resistant!

We used:
- [Gnosis Conditional Tokens](https://docs.gnosis.io/conditionaltokens/) for creating tokenized market positions.
- [Reality.eth](https://reality.eth.link/) as an oracle to resolve those positions.
- [Kleros](https://kleros.io/) as an arbitrator to Reality.eth oracle.
- [1155-to-20](https://github.com/gnosis/1155-to-20) to wrapped the conditional token positions into ERC20 tokens.
- [Swapr](https://swapr.eth.link) as an Automated Market Maker and a way to subsidize liquidity.

### Deployments
- [Condition](https://cte.gnosis.io/#/conditions/0xc983363863c95ec27501b2d396d7af72035b4660aa1e6bad9327ce1d7b950e3a) splitting the DAI into Yes-DAI and No-DAI (to the question "Will Russia launch a military operation in Moldova in 2022?").
- [Question](https://reality.eth.link/app/#!/question/0x325a2e0f3cca2ddbaebb4dfc38df8d19ca165b47-0x7d118e72257f0dbb9d0ae06778f3e891af58fefb861e486d4b2b938c8f67a34f) on Reality.eth using Kleros as an arbitrator.
- [Wrapped ERC20](https://etherscan.io/token/0xd71d475a6318a3e1dc947a657b01dcbda15e9b40) token representing No-DAI (redeem for DAI if the answer is "No").
- [Liquidity Pool](https://swapr.eth.link/#/pools/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xd71D475A6318A3E1dc947A657B01dcBDa15E9B40?chainId=1) ([DXswapPool Token](https://etherscan.io/address/0xbd51cc182c446933c721891c80cbc241a7e84635))
- [Trading interface on DXswap](https://swapr.eth.link/#/swap?chainId=1). Note that the No-DAI token is unlisted so you need to copy the address 0xd71d475a6318a3e1dc947a657b01dcbda15e9b40 an "import token".
- [Rewards](https://swapr.eth.link/#/rewards/campaign/0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2/0xd71D475A6318A3E1dc947A657B01dcBDa15E9B40/0x2e9B038F6b90266e1d53101bd129B6b916d05D8e?chainId=1) where you can stake your DXswapPool tokens to get part of the 10 DAI subsidies.


### Mockups
We made a mockup of a combined interface (allowing to perform all actions related to Seer in a unique interface).
- [Mockup](https://github.com/Crypto-Ser/Seer/blob/main/CombineInterfaceMockUp.pdf)
Implementing it will be the next step after the hackathon.
![307224239_1436050570233128_9040444296082608918_n](https://user-images.githubusercontent.com/113799257/190894162-6293bb26-8048-4bfa-8901-c7277ee05870.jpg)

![307090504_943627146594223_3237756096729281983_n](https://user-images.githubusercontent.com/113799257/190894149-8df7cc1d-273e-4bf7-9578-ccdac732c72a.jpg)



