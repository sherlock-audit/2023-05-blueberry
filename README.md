
# Blueberry Update #2 contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

## Quick Note
There was a scoping mistake in Blueberry Update #1 (too many new contracts in scope for the short contest length), so Blueberry Update #2 (this contest) is meant to be a continuation of Blueberry Update #1 (same scope, except CurveSpell.sol is removed), and the issues expected to be valid in Blueberry Update #1 (using a snapshot taken of the Lead Judge's judgments for Blueberry Update #1 on May 3, 2023) are not valid to submit in Blueberry Update #2. Please see the two tables under "Please list any known issues/acceptable risks that should not result in a valid finding" for a complete list of the 39 issues that are out-of-scope for this contest. 


# Q&A

### Q: On what chains are the smart contracts going to be deployed?
Mainnet, Arbitrum
___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
Whitelisted
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
Uni-v3 LP tokens & Whitelisted ERC721
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
none
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

none
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

none
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
Trusted
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
Trusted - Multisig wallet with multiple members 
___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
none
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
none
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
- Rebasing tokens, tokens that change balance on transfer, with token burns, etc, are not compatible with the system and should not be whitelisted.

- Centralization risk is known: the DAO multi-sig for the protocol is able to set the various configurations for the protocol. 

**Please note: There are 2 lists of out-of-scope issues for this contest (39 out-of-scope issues in total):** 

- The first list of 6 issues were labeled "Won't Fix" in the first Blueberry contest:

| Issue description | GitHub Issue |
| - | - |
| ChainlinkAdapterOracle use BTC/USD chainlink oracle to price WBTC which is problematic if WBTC depegs | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/9) |
| ChainlinkAdapterOracle will return the wrong price for asset if underlying aggregator hits minAnswer | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/18) |
| LP tokens cannot be valued because ICHI cannot be priced by oracle, causing all new open positions to revert | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/152) |
| Complete debt size is not paid off for fee on transfer tokens, but users aren't warned | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/153) |
| If a token's oracle goes down or price falls to zero, liquidations will be frozen | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/161) |
| The maximum size of an `ICHI` vault spell position can be arbitrarily surpassed | [Link](https://github.com/sherlock-audit/2023-02-blueberry-judging/issues/327) |
  
- The second list of 33 issues are those expected to be rewarded from Blueberry Update #1:

| Issue description | GitHub Issue |
| - | - |
| Borrower can't repay but can be liquidated as token whitelist can prevent existing positions from repaying | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/4) |
| Accrue function is not called before executing some functions | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/10) |
| Transaction will revert when using USDT tokens (or other non-compliant ERC20 tokens) | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/15) |
| IchiVaultOracle getPrice will fail during price crashes | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/28) |
| auraPools.deposit and auraPools.withdraw  boolean return value not handled in WAuraPools.sol | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/41) |
| AuraSpell openPositionFarm does not join pool | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/46) |
| The protocol  will not be able to add liquidity on the curve with another token with a balance. | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/47) |
| Dos attack to openPositionFarm() | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/48) |
| Users can fail to closePositionFarm and lose their funds | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/64) |
| Potential DOS / lack of acccess to oracle price due to unhandled chainlink revert | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/77) |
| `getPositionRisk()` will return a wrong value of risk | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/97) |
| BlueBerryBank#getPositionValue causes DOS if reward token is added that doens't have an oracle | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/115) |
| Issue 290 from previous contest has not been fully addressed by fixes | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/117) |
| Issue 94 from previous contest has not been fixed | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/118) |
| AuraSpell#openPositionFarm uses incorrect join type for balancer | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/120) |
| Users are forced to swap all reward tokens with no slippage protection | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/121) |
| AuraSpell#closePositionFarm requires users to swap all reward tokens through same router | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/122) |
| Potential flash loan attack vulnerability in `getPrice` function of CurveOracle | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/123) |
| ConvexSpell#closePositionFarm removes liquidity without any slippage protection | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/124) |
| Issue 327 from previous contest has not been fixed | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/125) |
| ShortLongSpell#_withdraw checks slippage limit but never applies it making it useless | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/126) |
| WAuraPools will irreversibly break if reward tokens are added to pool after deposit | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/127) |
| rewardTokens removed from WAuraPool/WConvexPools will be lost forever | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/128) |
| UserData for balancer pool exits is malformed and will permanently trap users | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/129) |
| IchiSpell applies slippage to sqrtPrice which is wrong and leads to unpredictable slippage | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/131) |
| UniswapV3 sqrtRatioLimit doesn't provide slippage protection and will result in partial swaps | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/132) |
| Balance check for swapToken in ShortLongSpell#_deposit is incorrect and will result in nonfunctional contract | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/133) |
| ShortLongSpell#openPosition can cause user unexpected liquidation when increasing position size | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/135) |
| Pending CRV rewards are not accounted for and can cause unfair liquidations | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/136) |
| WIchiFarm#pendingRewards suffers from significant precision loss causing loss of rewards | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/137) |
| `BalancerPairOracle` can be manipulated using read-only reentrancy | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/141) |
| Missing checks for whether Arbitrum Sequencer is active | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/142) |
| Deadline check is not effective, allowing outdated slippage and allow pending transaction to be unexpected executed | [Link](https://github.com/sherlock-audit/2023-04-blueberry-judging/issues/145) |

Note: Why so many out-of-scope issues? There was a mistake in scoping for Blueberry Update #1 (too many new contracts in scope for the short contest length), so Blueberry Update #2 (this contest) is really just a continuation of Blueberry Update #1 (same scope, except CurveSpell.sol is removed), except the issues expected to be valid in Blueberry Update #1 (using a snapshot taken of the Lead Judge's judgments on May 3, 2023) are not valid to submit in Blueberry Update #2. 
___

### Q: Please provide links to previous audits (if any).
Sherlock audit - https://github.com/sherlock-audit/2023-02-blueberry-judging/issues

Update 1 - https://github.com/sherlock-audit/2023-04-blueberry-judging
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
none
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
We utilize chainlink price feeds as the primary source, if they are paused it may result in stale pricing or reverting transactions. But the system utilizes an aggregated oracle approach to avoid those issues.

Additionally, the external protocol integrations are all the of the spells as that is how we handle deployments/strategies to those external protocols. This is why that all Spells are whitelisted and added through the DAO multi-sig and not permissionless as they have to go through an on-boarding process.  
___



# Audit scope


[blueberry-core @ 25cf493e536e7c5d895bb7c712ce6ba0f3cb03c9](https://github.com/Blueberryfi/blueberry-core/tree/25cf493e536e7c5d895bb7c712ce6ba0f3cb03c9)
- [blueberry-core/contracts/BlueBerryBank.sol](blueberry-core/contracts/BlueBerryBank.sol)
- [blueberry-core/contracts/FeeManager.sol](blueberry-core/contracts/FeeManager.sol)
- [blueberry-core/contracts/ProtocolConfig.sol](blueberry-core/contracts/ProtocolConfig.sol)
- [blueberry-core/contracts/libraries/BBMath.sol](blueberry-core/contracts/libraries/BBMath.sol)
- [blueberry-core/contracts/libraries/Paraswap/PSwapLib.sol](blueberry-core/contracts/libraries/Paraswap/PSwapLib.sol)
- [blueberry-core/contracts/libraries/Paraswap/Utils.sol](blueberry-core/contracts/libraries/Paraswap/Utils.sol)
- [blueberry-core/contracts/libraries/UniV3/UniV3WrappedLib.sol](blueberry-core/contracts/libraries/UniV3/UniV3WrappedLib.sol)
- [blueberry-core/contracts/libraries/UniV3/UniV3WrappedLibMockup.sol](blueberry-core/contracts/libraries/UniV3/UniV3WrappedLibMockup.sol)
- [blueberry-core/contracts/oracle/AggregatorOracle.sol](blueberry-core/contracts/oracle/AggregatorOracle.sol)
- [blueberry-core/contracts/oracle/BalancerPairOracle.sol](blueberry-core/contracts/oracle/BalancerPairOracle.sol)
- [blueberry-core/contracts/oracle/BandAdapterOracle.sol](blueberry-core/contracts/oracle/BandAdapterOracle.sol)
- [blueberry-core/contracts/oracle/BaseAdapter.sol](blueberry-core/contracts/oracle/BaseAdapter.sol)
- [blueberry-core/contracts/oracle/BaseOracleExt.sol](blueberry-core/contracts/oracle/BaseOracleExt.sol)
- [blueberry-core/contracts/oracle/ChainlinkAdapterOracle.sol](blueberry-core/contracts/oracle/ChainlinkAdapterOracle.sol)
- [blueberry-core/contracts/oracle/CoreOracle.sol](blueberry-core/contracts/oracle/CoreOracle.sol)
- [blueberry-core/contracts/oracle/CurveOracle.sol](blueberry-core/contracts/oracle/CurveOracle.sol)
- [blueberry-core/contracts/oracle/IchiVaultOracle.sol](blueberry-core/contracts/oracle/IchiVaultOracle.sol)
- [blueberry-core/contracts/oracle/UniswapV2Oracle.sol](blueberry-core/contracts/oracle/UniswapV2Oracle.sol)
- [blueberry-core/contracts/oracle/UniswapV3AdapterOracle.sol](blueberry-core/contracts/oracle/UniswapV3AdapterOracle.sol)
- [blueberry-core/contracts/oracle/UsingBaseOracle.sol](blueberry-core/contracts/oracle/UsingBaseOracle.sol)
- [blueberry-core/contracts/spell/AuraSpell.sol](blueberry-core/contracts/spell/AuraSpell.sol)
- [blueberry-core/contracts/spell/BasicSpell.sol](blueberry-core/contracts/spell/BasicSpell.sol)
- [blueberry-core/contracts/spell/ConvexSpell.sol](blueberry-core/contracts/spell/ConvexSpell.sol)
- [blueberry-core/contracts/spell/IchiSpell.sol](blueberry-core/contracts/spell/IchiSpell.sol)
- [blueberry-core/contracts/spell/ShortLongSpell.sol](blueberry-core/contracts/spell/ShortLongSpell.sol)
- [blueberry-core/contracts/utils/BlueBerryConst.sol](blueberry-core/contracts/utils/BlueBerryConst.sol)
- [blueberry-core/contracts/utils/BlueBerryErrors.sol](blueberry-core/contracts/utils/BlueBerryErrors.sol)
- [blueberry-core/contracts/utils/ERC1155NaiveReceiver.sol](blueberry-core/contracts/utils/ERC1155NaiveReceiver.sol)
- [blueberry-core/contracts/utils/EnsureApprove.sol](blueberry-core/contracts/utils/EnsureApprove.sol)
- [blueberry-core/contracts/vault/HardVault.sol](blueberry-core/contracts/vault/HardVault.sol)
- [blueberry-core/contracts/vault/SoftVault.sol](blueberry-core/contracts/vault/SoftVault.sol)
- [blueberry-core/contracts/wrapper/WAuraPools.sol](blueberry-core/contracts/wrapper/WAuraPools.sol)
- [blueberry-core/contracts/wrapper/WConvexPools.sol](blueberry-core/contracts/wrapper/WConvexPools.sol)
- [blueberry-core/contracts/wrapper/WCurveGauge.sol](blueberry-core/contracts/wrapper/WCurveGauge.sol)
- [blueberry-core/contracts/wrapper/WERC20.sol](blueberry-core/contracts/wrapper/WERC20.sol)
- [blueberry-core/contracts/wrapper/WIchiFarm.sol](blueberry-core/contracts/wrapper/WIchiFarm.sol)

