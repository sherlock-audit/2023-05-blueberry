
# [project name] contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

# Audit scope


[2023-04-blueberry @ 96eb1829571dc46e1a387985bd56989702c5e1dc](https://github.com/sherlock-audit/2023-04-blueberry/tree/96eb1829571dc46e1a387985bd56989702c5e1dc)
- [2023-04-blueberry/blueberry-core/contracts/BlueBerryBank.sol](2023-04-blueberry/blueberry-core/contracts/BlueBerryBank.sol)
- [2023-04-blueberry/blueberry-core/contracts/FeeManager.sol](2023-04-blueberry/blueberry-core/contracts/FeeManager.sol)
- [2023-04-blueberry/blueberry-core/contracts/ProtocolConfig.sol](2023-04-blueberry/blueberry-core/contracts/ProtocolConfig.sol)
- [2023-04-blueberry/blueberry-core/contracts/libraries/BBMath.sol](2023-04-blueberry/blueberry-core/contracts/libraries/BBMath.sol)
- [2023-04-blueberry/blueberry-core/contracts/libraries/Paraswap/PSwapLib.sol](2023-04-blueberry/blueberry-core/contracts/libraries/Paraswap/PSwapLib.sol)
- [2023-04-blueberry/blueberry-core/contracts/libraries/Paraswap/Utils.sol](2023-04-blueberry/blueberry-core/contracts/libraries/Paraswap/Utils.sol)
- [2023-04-blueberry/blueberry-core/contracts/libraries/UniV3/UniV3WrappedLib.sol](2023-04-blueberry/blueberry-core/contracts/libraries/UniV3/UniV3WrappedLib.sol)
- [2023-04-blueberry/blueberry-core/contracts/libraries/UniV3/UniV3WrappedLibMockup.sol](2023-04-blueberry/blueberry-core/contracts/libraries/UniV3/UniV3WrappedLibMockup.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/AggregatorOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/AggregatorOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/BalancerPairOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/BalancerPairOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/BandAdapterOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/BandAdapterOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/BaseAdapter.sol](2023-04-blueberry/blueberry-core/contracts/oracle/BaseAdapter.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/BaseOracleExt.sol](2023-04-blueberry/blueberry-core/contracts/oracle/BaseOracleExt.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/ChainlinkAdapterOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/ChainlinkAdapterOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/CoreOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/CoreOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/IchiVaultOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/IchiVaultOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/UniswapV2Oracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/UniswapV2Oracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/UniswapV3AdapterOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/UniswapV3AdapterOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/oracle/UsingBaseOracle.sol](2023-04-blueberry/blueberry-core/contracts/oracle/UsingBaseOracle.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/AuraSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/AuraSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/BasicSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/BasicSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/ConvexSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/ConvexSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/CurveSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/CurveSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/IchiSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/IchiSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/spell/ShortLongSpell.sol](2023-04-blueberry/blueberry-core/contracts/spell/ShortLongSpell.sol)
- [2023-04-blueberry/blueberry-core/contracts/utils/BlueBerryConst.sol](2023-04-blueberry/blueberry-core/contracts/utils/BlueBerryConst.sol)
- [2023-04-blueberry/blueberry-core/contracts/utils/BlueBerryErrors.sol](2023-04-blueberry/blueberry-core/contracts/utils/BlueBerryErrors.sol)
- [2023-04-blueberry/blueberry-core/contracts/utils/ERC1155NaiveReceiver.sol](2023-04-blueberry/blueberry-core/contracts/utils/ERC1155NaiveReceiver.sol)
- [2023-04-blueberry/blueberry-core/contracts/utils/EnsureApprove.sol](2023-04-blueberry/blueberry-core/contracts/utils/EnsureApprove.sol)
- [2023-04-blueberry/blueberry-core/contracts/vault/HardVault.sol](2023-04-blueberry/blueberry-core/contracts/vault/HardVault.sol)
- [2023-04-blueberry/blueberry-core/contracts/vault/SoftVault.sol](2023-04-blueberry/blueberry-core/contracts/vault/SoftVault.sol)
- [2023-04-blueberry/blueberry-core/contracts/wrapper/WAuraPools.sol](2023-04-blueberry/blueberry-core/contracts/wrapper/WAuraPools.sol)
- [2023-04-blueberry/blueberry-core/contracts/wrapper/WConvexPools.sol](2023-04-blueberry/blueberry-core/contracts/wrapper/WConvexPools.sol)
- [2023-04-blueberry/blueberry-core/contracts/wrapper/WCurveGauge.sol](2023-04-blueberry/blueberry-core/contracts/wrapper/WCurveGauge.sol)
- [2023-04-blueberry/blueberry-core/contracts/wrapper/WERC20.sol](2023-04-blueberry/blueberry-core/contracts/wrapper/WERC20.sol)
- [2023-04-blueberry/blueberry-core/contracts/wrapper/WIchiFarm.sol](2023-04-blueberry/blueberry-core/contracts/wrapper/WIchiFarm.sol)


