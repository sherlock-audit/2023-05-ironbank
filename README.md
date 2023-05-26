
# Iron Bank contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
mainnet, Arbitrum, Optimism
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
USDC, USDT, wstETH, WBTC, WETH, DAI and other vanilla ERC20s
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
none
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
none
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

no
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

yes, we provide stETH wrapping helper
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
TRUSTED
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
1. guardian
2. pause supply, borrow, credit limits, configure markets
3. Stop any potential explots in time
4. Modify critical market configs such as collateral factor, interest rate model, change oracle, credit limits, etc.
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
FlashLoan.sol should comply EIP3156
PToken should comply EIP20
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
- Bad debt caused by price fluctuation
- Unable to redeem supplied asset when liquidity is insufficient in the pool
- Credit account can borrow without collateral up to credit limit
___

### Q: Please provide links to previous audits (if any).
none
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
nope
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
Not acceptable

___



# Audit scope


[ib-v2 @ 66c70f3f58a1dc1e07908b4dae2f55c30e3b7edd](https://github.com/ibdotxyz/ib-v2/tree/66c70f3f58a1dc1e07908b4dae2f55c30e3b7edd)
- [ib-v2/src/extensions/TxBuilderExtension.sol](ib-v2/src/extensions/TxBuilderExtension.sol)
- [ib-v2/src/extensions/UniswapExtension.sol](ib-v2/src/extensions/UniswapExtension.sol)
- [ib-v2/src/extensions/libraries/UniswapV2Utils.sol](ib-v2/src/extensions/libraries/UniswapV2Utils.sol)
- [ib-v2/src/extensions/libraries/UniswapV3Utils.sol](ib-v2/src/extensions/libraries/UniswapV3Utils.sol)
- [ib-v2/src/flashLoan/FlashLoan.sol](ib-v2/src/flashLoan/FlashLoan.sol)
- [ib-v2/src/libraries/Arrays.sol](ib-v2/src/libraries/Arrays.sol)
- [ib-v2/src/libraries/DataTypes.sol](ib-v2/src/libraries/DataTypes.sol)
- [ib-v2/src/libraries/PauseFlags.sol](ib-v2/src/libraries/PauseFlags.sol)
- [ib-v2/src/protocol/oracle/PriceOracle.sol](ib-v2/src/protocol/oracle/PriceOracle.sol)
- [ib-v2/src/protocol/pool/Constants.sol](ib-v2/src/protocol/pool/Constants.sol)
- [ib-v2/src/protocol/pool/CreditLimitManager.sol](ib-v2/src/protocol/pool/CreditLimitManager.sol)
- [ib-v2/src/protocol/pool/Events.sol](ib-v2/src/protocol/pool/Events.sol)
- [ib-v2/src/protocol/pool/IronBank.sol](ib-v2/src/protocol/pool/IronBank.sol)
- [ib-v2/src/protocol/pool/IronBankProxy.sol](ib-v2/src/protocol/pool/IronBankProxy.sol)
- [ib-v2/src/protocol/pool/IronBankStorage.sol](ib-v2/src/protocol/pool/IronBankStorage.sol)
- [ib-v2/src/protocol/pool/MarketConfigurator.sol](ib-v2/src/protocol/pool/MarketConfigurator.sol)
- [ib-v2/src/protocol/pool/interest-rate-model/TripleSlopeRateModel.sol](ib-v2/src/protocol/pool/interest-rate-model/TripleSlopeRateModel.sol)
- [ib-v2/src/protocol/token/DebtToken.sol](ib-v2/src/protocol/token/DebtToken.sol)
- [ib-v2/src/protocol/token/DebtTokenStorage.sol](ib-v2/src/protocol/token/DebtTokenStorage.sol)
- [ib-v2/src/protocol/token/IBToken.sol](ib-v2/src/protocol/token/IBToken.sol)
- [ib-v2/src/protocol/token/IBTokenStorage.sol](ib-v2/src/protocol/token/IBTokenStorage.sol)
- [ib-v2/src/protocol/token/PToken.sol](ib-v2/src/protocol/token/PToken.sol)
- [ib-v2/src/interfaces/DebtTokenInterface.sol](ib-v2/src/interfaces/DebtTokenInterface.sol)
- [ib-v2/src/interfaces/DeferLiquidityCheckInterface.sol](ib-v2/src/interfaces/DeferLiquidityCheckInterface.sol)
- [ib-v2/src/interfaces/IBTokenInterface.sol](ib-v2/src/interfaces/IBTokenInterface.sol)
- [ib-v2/src/interfaces/InterestRateModelInterface.sol](ib-v2/src/interfaces/InterestRateModelInterface.sol)
- [ib-v2/src/interfaces/IronBankInterface.sol](ib-v2/src/interfaces/IronBankInterface.sol)
- [ib-v2/src/interfaces/PTokenInterface.sol](ib-v2/src/interfaces/PTokenInterface.sol)
- [ib-v2/src/interfaces/PriceOracleInterface.sol](ib-v2/src/interfaces/PriceOracleInterface.sol)


