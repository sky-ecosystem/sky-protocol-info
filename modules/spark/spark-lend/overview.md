# spark-lend

## Codebases

```yaml
repositories:
- id: sparklend-v1-core
  name: sparklend-v1-core
  provider: github
  url: https://github.com/sparkdotfi/sparklend-v1-core
  ref: master
  ref_type: branch
  source_code_roots:
  - contracts
  checkout:
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    checked_out_branch: master
    pinned_commit: 8120e495061dc3315f0a86f682f4ca645a418bf7
- id: sparklend-advanced
  name: sparklend-advanced
  provider: github
  url: https://github.com/sparkdotfi/sparklend-advanced
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sparklend-advanced/branch-master"
    checked_out_branch: master
    pinned_commit: cf5bc269af45b7a3b7a8e4e07ee5bbb0f65e5f76
- id: sparklend-cap-automator
  name: sparklend-cap-automator
  provider: github
  url: https://github.com/sparkdotfi/sparklend-cap-automator
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sparklend-cap-automator/branch-master"
    checked_out_branch: master
    pinned_commit: 5c054cfddf4b8f21281ea4c23db3f0495f9aa8c5
- id: sparklend-freezer
  name: sparklend-freezer
  provider: github
  url: https://github.com/sparkdotfi/sparklend-freezer
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    checked_out_branch: master
    pinned_commit: f87388bad3302b83d4ca9b92b9219527181f0586
- id: sparklend-kill-switch
  name: sparklend-kill-switch
  provider: github
  url: https://github.com/sparkdotfi/sparklend-kill-switch
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sparklend-kill-switch/branch-master"
    checked_out_branch: master
    pinned_commit: 12cf956146bfb16498db961a8399d9c5fdf34e20
- id: sparklend-testing
  name: sparklend-testing
  provider: github
  url: https://github.com/sparkdotfi/sparklend-testing
  ref: master
  ref_type: branch
  source_code_roots:
  - src
  checkout:
    submodule_path: "./codebases/sparklend-testing/branch-master"
    checked_out_branch: master
    pinned_commit: 1c76b20d69d9bb4538bb5eb70dee1853d77b5d9e
```

## Deployments

```yaml
deployments:
- id: spell-freeze-all-ethereum
  contract_id: spell-freeze-all
  contract_name: EmergencySpell_SparkLend_FreezeAllAssets
  status: live
  chain: Ethereum
  address: '0x9e2890BF7f8D5568Cc9e5092E67Ba00C8dA3E97f'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/spells/EmergencySpell_SparkLend_FreezeAllAssets.sol
    contract_name: EmergencySpell_SparkLend_FreezeAllAssets
- id: spell-freeze-dai-ethereum
  contract_id: spell-freeze-dai
  contract_name: EmergencySpell_SparkLend_FreezeSingleAsset
  status: live
  chain: Ethereum
  address: '0xa2039bef2c5803d66E4e68F9E23a942E350b938c'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/spells/EmergencySpell_SparkLend_FreezeSingleAsset.sol
    contract_name: EmergencySpell_SparkLend_FreezeSingleAsset
- id: spell-pause-all-ethereum
  contract_id: spell-pause-all
  contract_name: EmergencySpell_SparkLend_PauseAllAssets
  status: live
  chain: Ethereum
  address: '0x425b0de240b4c2DC45979DB782A355D090Dc4d37'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/spells/EmergencySpell_SparkLend_PauseAllAssets.sol
    contract_name: EmergencySpell_SparkLend_PauseAllAssets
- id: spell-pause-dai-ethereum
  contract_id: spell-pause-dai
  contract_name: EmergencySpell_SparkLend_PauseSingleAsset
  status: live
  chain: Ethereum
  address: '0xCacB88e39112B56278db25b423441248cfF94241'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/spells/EmergencySpell_SparkLend_PauseSingleAsset.sol
    contract_name: EmergencySpell_SparkLend_PauseSingleAsset
- id: spell-remove-freezer-multisig-ethereum
  contract_id: spell-remove-freezer-multisig
  contract_name: EmergencySpell_SparkLend_RemoveMultisig
  status: live
  chain: Ethereum
  address: '0xE47AB4919F6F5459Dcbbfbe4264BD4630c0169A9'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/spells/EmergencySpell_SparkLend_RemoveMultisig.sol
    contract_name: EmergencySpell_SparkLend_RemoveMultisig
- id: user-actions-psm-variant1-ethereum
  contract_id: user-actions-psm-variant1
  contract_name: UserActions
  status: live
  chain: Ethereum
  address: '0x52d298Ff9e77E71C2EB1992260520E7b15257d99'
  implementation:
    codebase: sparklend-testing
    submodule_path: "./codebases/sparklend-testing/branch-master"
    source_path: src/UserActions.sol
    contract_name: UserActions
- id: aave-oracle-ethereum
  contract_id: aave-oracle
  contract_name: AaveOracle
  status: live
  chain: Ethereum
  address: '0x8105f69D9C41644c6A0803fDA7D03Aa70996cFD9'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/misc/AaveOracle.sol
    contract_name: AaveOracle
- id: acl-manager-ethereum
  contract_id: acl-manager
  contract_name: ACLManager
  status: live
  chain: Ethereum
  address: '0xdA135Cd78A086025BcdC87B038a1C462032b510C'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/ACLManager.sol
    contract_name: ACLManager
- id: pool-ethereum
  contract_id: pool
  contract_name: Pool
  status: live
  chain: Ethereum
  address: '0xC13e21B648A5Ee794902342038FF3aDAB66BE987'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/Pool.sol
    contract_name: Pool
- id: pool-addresses-provider-ethereum
  contract_id: pool-addresses-provider
  contract_name: PoolAddressesProvider
  status: live
  chain: Ethereum
  address: '0x02C3eA4e34C0cBd694D2adFa2c690EECbC1793eE'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/PoolAddressesProvider.sol
    contract_name: PoolAddressesProvider
- id: pool-addresses-provider-registry-ethereum
  contract_id: pool-addresses-provider-registry
  contract_name: PoolAddressesProviderRegistry
  status: live
  chain: Ethereum
  address: '0x03cFa0C4622FF84E50E75062683F44c9587e6Cc1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/PoolAddressesProviderRegistry.sol
    contract_name: PoolAddressesProviderRegistry
- id: pool-configurator-ethereum
  contract_id: pool-configurator
  contract_name: PoolConfigurator
  status: live
  chain: Ethereum
  address: '0x542DBa469bdE58FAeE189ffB60C6b49CE60E0738'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/PoolConfigurator.sol
    contract_name: PoolConfigurator
- id: cbbtc-debt-token-ethereum
  contract_id: cbbtc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x661fE667D2103eb52d3632a3eB2cAbd123F27938'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: cbbtc-sptoken-ethereum
  contract_id: cbbtc-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xb3973D459df38ae57797811F2A1fd061DA1BC123'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: dai-debt-token-ethereum
  contract_id: dai-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xf705d2B7e92B3F38e6ae7afaDAA2fEE110fE5914'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: dai-sptoken-ethereum
  contract_id: dai-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x4DEDf26112B3Ec8eC46e7E31EA5e123490B05B8B'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: ezeth-debt-token-ethereum
  contract_id: ezeth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xB0B14Dd477E6159B4F3F210cF45F0954F57c0FAb'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: ezeth-sptoken-ethereum
  contract_id: ezeth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xB131cD463d83782d4DE33e00e35EF034F0869bA1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: gno-debt-token-ethereum
  contract_id: gno-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x57a2957651DA467fCD4104D749f2F3684784c25a'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: gno-sptoken-ethereum
  contract_id: gno-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x7b481aCC9fDADDc9af2cBEA1Ff2342CB1733E50F'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: lbtc-debt-token-ethereum
  contract_id: lbtc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x096bdDFEE63F44A97cC6D2945539Ee7C8f94637D'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: lbtc-sptoken-ethereum
  contract_id: lbtc-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xa9d4EcEBd48C282a70CfD3c469d6C8F178a5738E'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: pyusd-debt-token-ethereum
  contract_id: pyusd-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x3357D2DB7763D6Cd3a99f0763EbF87e0096D95f9'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: pyusd-sptoken-ethereum
  contract_id: pyusd-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x779224df1c756b4EDD899854F32a53E8c2B2ce5d'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: reth-debt-token-ethereum
  contract_id: reth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xBa2C8F2eA5B56690bFb8b709438F049e5Dd76B96'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: reth-sptoken-ethereum
  contract_id: reth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x9985dF20D7e9103ECBCeb16a84956434B6f06ae8'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: rseth-debt-token-ethereum
  contract_id: rseth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xc528F0C91CFAE4fd86A68F6Dfd4d7284707Bec68'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: rseth-sptoken-ethereum
  contract_id: rseth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x856f1Ea78361140834FDCd0dB0b08079e4A45062'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: sdai-debt-token-ethereum
  contract_id: sdai-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xaBc57081C04D921388240393ec4088Aa47c6832B'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: sdai-sptoken-ethereum
  contract_id: sdai-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x78f897F0fE2d3B5690EbAe7f19862DEacedF10a7'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: susds-debt-token-ethereum
  contract_id: susds-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x4e89b83f426fED3f2EF7Bb2d7eb5b53e288e1A13'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: susds-sptoken-ethereum
  contract_id: susds-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x6715bc100A183cc65502F05845b589c1919ca3d3'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: tbtc-debt-token-ethereum
  contract_id: tbtc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x764591dC9ba21c1B92049331b80b6E2a2acF8B17'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: tbtc-sptoken-ethereum
  contract_id: tbtc-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xce6Ca9cDce00a2b0c0d1dAC93894f4Bd2c960567'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usdc-debt-token-ethereum
  contract_id: usdc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x7B70D04099CB9cfb1Db7B6820baDAfB4C5C70A67'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usdc-sptoken-ethereum
  contract_id: usdc-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x377C3bd93f2a2984E1E7bE6A5C22c525eD4A4815'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usds-debt-token-ethereum
  contract_id: usds-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x8c147debea24Fb98ade8dDa4bf142992928b449e'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usds-sptoken-ethereum
  contract_id: usds-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xC02aB1A5eaA8d1B114EF786D9bde108cD4364359'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usdt-debt-token-ethereum
  contract_id: usdt-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x529b6158d1D2992E3129F7C69E81a7c677dc3B12'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usdt-sptoken-ethereum
  contract_id: usdt-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0xe7dF13b8e3d6740fe17CBE928C7334243d86c92f'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: wbtc-debt-token-ethereum
  contract_id: wbtc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xf6fEe3A8aC8040C3d6d81d9A4a168516Ec9B51D2'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: wbtc-sptoken-ethereum
  contract_id: wbtc-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x4197ba364AE6698015AE5c1468f54087602715b2'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: weeth-debt-token-ethereum
  contract_id: weeth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xc2bD6d2fEe70A0A73a33795BdbeE0368AeF5c766'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: weeth-sptoken-ethereum
  contract_id: weeth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x3CFd5C0D4acAA8Faee335842e4f31159fc76B008'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: weth-debt-token-ethereum
  contract_id: weth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x2e7576042566f8D6990e07A1B61Ad1efd86Ae70d'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: weth-sptoken-ethereum
  contract_id: weth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x59cD1C87501baa753d0B5B5Ab5D8416A45cD71DB'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: wsteth-debt-token-ethereum
  contract_id: wsteth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0xd5c3E3B566a42A6110513Ac7670C1a86D76E13E6'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: wsteth-sptoken-ethereum
  contract_id: wsteth-sptoken
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x12B54025C112Aa61fAce2CDB7118740875A566E9'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: cap-automator-ethereum
  contract_id: cap-automator
  contract_name: CapAutomator
  status: live
  chain: Ethereum
  address: '0x4C1341636721b8B687647920B2E9481f3AB1F2eE'
  implementation:
    codebase: sparklend-cap-automator
    submodule_path: "./codebases/sparklend-cap-automator/branch-master"
    source_path: src/CapAutomator.sol
    contract_name: CapAutomator
- id: freezer-mom-ethereum
  contract_id: freezer-mom
  contract_name: SparkLendFreezerMom
  status: live
  chain: Ethereum
  address: '0x237e3985dD7E373F2ec878EC1Ac48A228Cf2e7a3'
  implementation:
    codebase: sparklend-freezer
    submodule_path: "./codebases/sparklend-freezer/branch-master"
    source_path: src/SparkLendFreezerMom.sol
    contract_name: SparkLendFreezerMom
- id: kill-switch-oracle-ethereum
  contract_id: kill-switch-oracle
  contract_name: KillSwitchOracle
  status: live
  chain: Ethereum
  address: '0x909A86f78e1cdEd68F9c2Fe2c9CD922c401abe82'
  implementation:
    codebase: sparklend-kill-switch
    submodule_path: "./codebases/sparklend-kill-switch/branch-master"
    source_path: src/KillSwitchOracle.sol
    contract_name: KillSwitchOracle
- id: ssr-rate-source-ethereum
  contract_id: ssr-rate-source
  contract_name: SSRRateSource
  status: live
  chain: Ethereum
  address: '0x57027B6262083E3aC3c8B2EB99f7e8005f669973'
  implementation:
    codebase: sparklend-advanced
    submodule_path: "./codebases/sparklend-advanced/branch-master"
    source_path: src/SSRRateSource.sol
    contract_name: SSRRateSource
- id: a-token-impl-ethereum
  contract_id: a-token-impl
  contract_name: AToken
  status: live
  chain: Ethereum
  address: '0x6175ddEc3B9b38c88157C10A01ed4A3fa8639cC6'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: pool-configurator-impl-ethereum
  contract_id: pool-configurator-impl
  contract_name: PoolConfigurator
  status: live
  chain: Ethereum
  address: '0xF7b656C95420194b79687fc86D965FB51DA4799F'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/PoolConfigurator.sol
    contract_name: PoolConfigurator
- id: pool-impl-ethereum
  contract_id: pool-impl
  contract_name: Pool
  status: live
  chain: Ethereum
  address: '0x5aE329203E00f76891094DcfedD5Aca082a50e1b'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/Pool.sol
    contract_name: Pool
- id: stable-debt-token-impl-ethereum
  contract_id: stable-debt-token-impl
  contract_name: StableDebtToken
  status: live
  chain: Ethereum
  address: '0x026a5B6114431d8F3eF2fA0E1B2EDdDccA9c540E'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: variable-debt-token-impl-ethereum
  contract_id: variable-debt-token-impl
  contract_name: VariableDebtToken
  status: live
  chain: Ethereum
  address: '0x86C71796CcDB31c3997F8Ec5C2E3dB3e9e40b985'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: protocol-data-provider-ethereum
  contract_id: protocol-data-provider
  contract_name: AaveProtocolDataProvider
  status: live
  chain: Ethereum
  address: '0xFc21d6d146E6086B8359705C8b28512a983db0cb'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/misc/AaveProtocolDataProvider.sol
    contract_name: AaveProtocolDataProvider
- id: borrow-logic-ethereum
  contract_id: borrow-logic
  contract_name: BorrowLogic
  status: live
  chain: Ethereum
  address: '0x4662C88C542F0954F8CccCDE4542eEc32d7E7e9a'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/BorrowLogic.sol
    contract_name: BorrowLogic
- id: bridge-logic-ethereum
  contract_id: bridge-logic
  contract_name: BridgeLogic
  status: live
  chain: Ethereum
  address: '0x2C54924711E479E639032704146b865E12f0C6D1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/BridgeLogic.sol
    contract_name: BridgeLogic
- id: emode-logic-ethereum
  contract_id: emode-logic
  contract_name: EModeLogic
  status: live
  chain: Ethereum
  address: '0x2Ad00613A66D71Ff2B0607fB3C4632C47a50DADe'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/EModeLogic.sol
    contract_name: EModeLogic
- id: flash-loan-logic-ethereum
  contract_id: flash-loan-logic
  contract_name: FlashLoanLogic
  status: live
  chain: Ethereum
  address: '0x7f44e1c1dE70059D7cc483378BEFeE2a030CE247'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/FlashLoanLogic.sol
    contract_name: FlashLoanLogic
- id: liquidation-logic-ethereum
  contract_id: liquidation-logic
  contract_name: LiquidationLogic
  status: live
  chain: Ethereum
  address: '0x6aEa92693C527bC2c7B3171C6f2598d67d619088'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/LiquidationLogic.sol
    contract_name: LiquidationLogic
- id: pool-logic-ethereum
  contract_id: pool-logic
  contract_name: PoolLogic
  status: live
  chain: Ethereum
  address: '0x1761a0f74032963B6Ad0774C5EBF4586c0bD7604'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/PoolLogic.sol
    contract_name: PoolLogic
- id: supply-logic-ethereum
  contract_id: supply-logic
  contract_name: SupplyLogic
  status: live
  chain: Ethereum
  address: '0x46256841e36b7557BB8e4c706beD38b17A9EB2c1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/libraries/logic/SupplyLogic.sol
    contract_name: SupplyLogic
- id: aave-oracle-gnosis
  contract_id: aave-oracle
  contract_name: AaveOracle
  status: live
  chain: Gnosis
  address: '0x8105f69D9C41644c6A0803fDA7D03Aa70996cFD9'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/misc/AaveOracle.sol
    contract_name: AaveOracle
- id: acl-manager-gnosis
  contract_id: acl-manager
  contract_name: ACLManager
  status: live
  chain: Gnosis
  address: '0x86C71796CcDB31c3997F8Ec5C2E3dB3e9e40b985'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/ACLManager.sol
    contract_name: ACLManager
- id: pool-gnosis
  contract_id: pool
  contract_name: Pool
  status: live
  chain: Gnosis
  address: '0x2Dae5307c5E3FD1CF5A72Cb6F698f915860607e0'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/Pool.sol
    contract_name: Pool
- id: pool-addresses-provider-gnosis
  contract_id: pool-addresses-provider
  contract_name: PoolAddressesProvider
  status: live
  chain: Gnosis
  address: '0xA98DaCB3fC964A6A0d2ce3B77294241585EAbA6d'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/PoolAddressesProvider.sol
    contract_name: PoolAddressesProvider
- id: pool-addresses-provider-registry-gnosis
  contract_id: pool-addresses-provider-registry
  contract_name: PoolAddressesProviderRegistry
  status: live
  chain: Gnosis
  address: '0x49d24798d3b84965F0d1fc8684EF6565115e70c1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/configuration/PoolAddressesProviderRegistry.sol
    contract_name: PoolAddressesProviderRegistry
- id: pool-configurator-gnosis
  contract_id: pool-configurator
  contract_name: PoolConfigurator
  status: live
  chain: Gnosis
  address: '0x2Fc8823E1b967D474b47Ae0aD041c2ED562ab588'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/PoolConfigurator.sol
    contract_name: PoolConfigurator
- id: gno-atoken-gnosis
  contract_id: gno-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x5671b0B8aC13DC7813D36B99C21c53F6cd376a14'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: gno-stable-debt-token-gnosis
  contract_id: gno-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x2f589BADbE2024a94f144ef24344aF91dE21a33c'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: gno-debt-token-gnosis
  contract_id: gno-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0xd4bAbF714964E399f95A7bb94B3DeaF22d9F575d'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: weth-atoken-gnosis
  contract_id: weth-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x629D562E92fED431122e865Cc650Bc6bdE6B96b0'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: weth-stable-debt-token-gnosis
  contract_id: weth-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0xe21Bf3FB5A2b5Bf7BAE8c6F1696c4B097F5D2f93'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: weth-debt-token-gnosis
  contract_id: weth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x0aD6cCf9a2e81d4d48aB7db791e9da492967eb84'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: wsteth-atoken-gnosis
  contract_id: wsteth-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x9Ee4271E17E3a427678344fd2eE64663Cb78B4be'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: wsteth-stable-debt-token-gnosis
  contract_id: wsteth-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x0F0e336Ab69D9516A9acF448bC59eA0CE79E4a42'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: wsteth-debt-token-gnosis
  contract_id: wsteth-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x3294dA2E28b29D1c08D556e2B86879d221256d31'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: wxdai-atoken-gnosis
  contract_id: wxdai-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0xC9Fe2D32E96Bb364c7d29f3663ed3b27E30767bB'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: wxdai-stable-debt-token-gnosis
  contract_id: wxdai-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0xab1B62A1346Acf534b581684940E2FD781F2EA22'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: wxdai-debt-token-gnosis
  contract_id: wxdai-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x868ADfDf12A86422524EaB6978beAE08A0008F37'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: sxdai-atoken-gnosis
  contract_id: sxdai-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0xE877b96caf9f180916bF2B5Ce7Ea8069e0123182'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: sxdai-stable-debt-token-gnosis
  contract_id: sxdai-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x2cF710377b3576287Be7cf352FF75D4472902789'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: sxdai-debt-token-gnosis
  contract_id: sxdai-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x1022E390E2457A78E18AEEE0bBf0E96E482EeE19'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usdc-atoken-gnosis
  contract_id: usdc-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x5850D127a04ed0B4F1FCDFb051b3409FB9Fe6B90'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usdc-stable-debt-token-gnosis
  contract_id: usdc-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x40BF0Bf6AECeE50eCE10C74E81a52C654A467ae4'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: usdc-debt-token-gnosis
  contract_id: usdc-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0xBC4f20DAf4E05c17E93676D2CeC39769506b8219'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usdce-atoken-gnosis
  contract_id: usdce-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0xA34DB0ee8F84C4B90ed268dF5aBbe7Dcd3c277ec'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usdce-stable-debt-token-gnosis
  contract_id: usdce-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0xC5dfde524371F9424c81F453260B2CCd24936c15'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: usdce-debt-token-gnosis
  contract_id: usdce-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x397b97b572281d0b3e3513BD4A7B38050a75962b'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: usdt-atoken-gnosis
  contract_id: usdt-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x08B0cAebE352c3613302774Cd9B82D08afd7bDC4'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: usdt-stable-debt-token-gnosis
  contract_id: usdt-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x4cB3F681B5e393947BD1e5cAE84764f5892923C2'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: usdt-debt-token-gnosis
  contract_id: usdt-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x3A98aBC6F46CA2Fc6c7d06eD02184D63C55e19B2'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: eure-atoken-gnosis
  contract_id: eure-atoken
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x6dc304337BF3EB397241d1889cAE7da638e6e782'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: eure-stable-debt-token-gnosis
  contract_id: eure-stable-debt-token
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x80F87B8F9c1199e468923D8EE87cEE311690FDA6'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: eure-debt-token-gnosis
  contract_id: eure-debt-token
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x0b33480d3FbD1E2dBE88c82aAbe191D7473759D5'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: a-token-impl-gnosis
  contract_id: a-token-impl
  contract_name: AToken
  status: live
  chain: Gnosis
  address: '0x856900aa78e856a5df1a2665eE3a66b2487cD68f'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/AToken.sol
    contract_name: AToken
- id: pool-configurator-impl-gnosis
  contract_id: pool-configurator-impl
  contract_name: PoolConfigurator
  status: live
  chain: Gnosis
  address: '0x6175ddEc3B9b38c88157C10A01ed4A3fa8639cC6'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/PoolConfigurator.sol
    contract_name: PoolConfigurator
- id: pool-impl-gnosis
  contract_id: pool-impl
  contract_name: Pool
  status: live
  chain: Gnosis
  address: '0xCF86A65779e88bedfF0319FE13aE2B47358EB1bF'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/pool/Pool.sol
    contract_name: Pool
- id: stable-debt-token-impl-gnosis
  contract_id: stable-debt-token-impl
  contract_name: StableDebtToken
  status: live
  chain: Gnosis
  address: '0x4370D3b6C9588E02ce9D22e684387859c7Ff5b34'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/StableDebtToken.sol
    contract_name: StableDebtToken
- id: variable-debt-token-impl-gnosis
  contract_id: variable-debt-token-impl
  contract_name: VariableDebtToken
  status: live
  chain: Gnosis
  address: '0x0ee554F6A1f7a4Cb4f82D4C124DdC2AD3E37fde1'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/protocol/tokenization/VariableDebtToken.sol
    contract_name: VariableDebtToken
- id: protocol-data-provider-gnosis
  contract_id: protocol-data-provider
  contract_name: AaveProtocolDataProvider
  status: live
  chain: Gnosis
  address: '0x2a002054A06546bB5a264D57A81347e23Af91D18'
  implementation:
    codebase: sparklend-v1-core
    submodule_path: "./codebases/sparklend-v1-core/branch-master"
    source_path: contracts/misc/AaveProtocolDataProvider.sol
    contract_name: AaveProtocolDataProvider
```

## Audit Reports

```yaml
audit_reports:
- id: chainsecurity-sparklend-advanced-audit
  auditor: ChainSecurity
  report_title: SparkLend Advanced Audit
  current_version: v160
  versions:
  - id: v160
    reference_refs:
    - chainsecurity-sparklend-advanced-audit-v160
    version_label: v160
    status: current
    audited_codebases:
    - sparklend-advanced
    audited_sources:
    - codebase: sparklend-advanced
      path: src/SSRRateSource.sol
    covered_contracts:
    - id: ssr-rate-source
      name: SSRRateSource
- id: chainsecurity-sparklend-cap-automator-audit
  auditor: ChainSecurity
  report_title: SparkLend Cap Automator Audit
  current_version: v110
  versions:
  - id: v110
    reference_refs:
    - chainsecurity-sparklend-cap-automator-audit-v110
    version_label: v110
    status: current
    audited_codebases:
    - sparklend-cap-automator
    audited_sources:
    - codebase: sparklend-cap-automator
      path: src/CapAutomator.sol
    covered_contracts:
    - id: cap-automator
      name: CapAutomator
- id: chainsecurity-sparklend-core-updates-audit
  auditor: ChainSecurity
  report_title: SparkLend Core Updates Audit
  current_version: final
  versions:
  - id: final
    reference_refs:
    - chainsecurity-sparklend-core-updates-audit-final
    version_label: Final
    status: current
    audited_codebases:
    - sparklend-v1-core
    audited_sources:
    - codebase: sparklend-v1-core
      path: contracts/misc/AaveOracle.sol
    - codebase: sparklend-v1-core
      path: contracts/misc/AaveProtocolDataProvider.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/configuration/ACLManager.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/configuration/PoolAddressesProvider.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/configuration/PoolAddressesProviderRegistry.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/BorrowLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/BridgeLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/EModeLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/FlashLoanLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/LiquidationLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/PoolLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/libraries/logic/SupplyLogic.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/pool/Pool.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/pool/PoolConfigurator.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/tokenization/AToken.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/tokenization/StableDebtToken.sol
    - codebase: sparklend-v1-core
      path: contracts/protocol/tokenization/VariableDebtToken.sol
    covered_contracts:
    - id: a-token
      name: AToken
    - id: aave-oracle
      name: AaveOracle
    - id: aave-protocol-data-provider
      name: AaveProtocolDataProvider
    - id: acl-manager
      name: ACLManager
    - id: borrow-logic
      name: BorrowLogic
    - id: bridge-logic
      name: BridgeLogic
    - id: e-mode-logic
      name: EModeLogic
    - id: flash-loan-logic
      name: FlashLoanLogic
    - id: liquidation-logic
      name: LiquidationLogic
    - id: pool
      name: Pool
    - id: pool-addresses-provider
      name: PoolAddressesProvider
    - id: pool-addresses-provider-registry
      name: PoolAddressesProviderRegistry
    - id: pool-configurator
      name: PoolConfigurator
    - id: pool-logic
      name: PoolLogic
    - id: stable-debt-token
      name: StableDebtToken
    - id: supply-logic
      name: SupplyLogic
    - id: variable-debt-token
      name: VariableDebtToken
- id: chainsecurity-sparklend-freezer-audit
  auditor: ChainSecurity
  report_title: SparkLend Freezer Audit
  current_version: final
  versions:
  - id: final
    reference_refs:
    - chainsecurity-sparklend-freezer-audit-final
    version_label: Final
    status: current
    audited_codebases:
    - sparklend-freezer
    audited_sources:
    - codebase: sparklend-freezer
      path: src/SparkLendFreezerMom.sol
    - codebase: sparklend-freezer
      path: src/spells/EmergencySpell_SparkLend_FreezeAllAssets.sol
    - codebase: sparklend-freezer
      path: src/spells/EmergencySpell_SparkLend_FreezeSingleAsset.sol
    - codebase: sparklend-freezer
      path: src/spells/EmergencySpell_SparkLend_PauseAllAssets.sol
    - codebase: sparklend-freezer
      path: src/spells/EmergencySpell_SparkLend_PauseSingleAsset.sol
    - codebase: sparklend-freezer
      path: src/spells/EmergencySpell_SparkLend_RemoveMultisig.sol
    covered_contracts:
    - id: emergency-spell-spark-lend-freeze-all-assets
      name: EmergencySpell_SparkLend_FreezeAllAssets
    - id: emergency-spell-spark-lend-freeze-single-asset
      name: EmergencySpell_SparkLend_FreezeSingleAsset
    - id: emergency-spell-spark-lend-pause-all-assets
      name: EmergencySpell_SparkLend_PauseAllAssets
    - id: emergency-spell-spark-lend-pause-single-asset
      name: EmergencySpell_SparkLend_PauseSingleAsset
    - id: emergency-spell-spark-lend-remove-multisig
      name: EmergencySpell_SparkLend_RemoveMultisig
    - id: spark-lend-freezer-mom
      name: SparkLendFreezerMom
- id: chainsecurity-sparklend-kill-switch-audit
  auditor: ChainSecurity
  report_title: SparkLend Kill Switch Audit
  current_version: final
  versions:
  - id: final
    reference_refs:
    - chainsecurity-sparklend-kill-switch-audit-final
    version_label: Final
    status: current
    audited_codebases:
    - sparklend-kill-switch
    audited_sources:
    - codebase: sparklend-kill-switch
      path: src/KillSwitchOracle.sol
    covered_contracts:
    - id: kill-switch-oracle
      name: KillSwitchOracle
- id: cantina-sparklend-advanced-audit
  auditor: Cantina
  report_title: SparkLend Advanced Audit
  current_version: v160
  versions:
  - id: v160
    reference_refs:
    - cantina-sparklend-advanced-audit-v160
    version_label: v160
    status: current
    audited_codebases:
    - sparklend-advanced
    audited_sources:
    - codebase: sparklend-advanced
      path: src/SSRRateSource.sol
    covered_contracts:
    - id: ssr-rate-source
      name: SSRRateSource
- id: cantina-sparklend-cap-automator-audit
  auditor: Cantina
  report_title: SparkLend Cap Automator Audit
  current_version: v110
  versions:
  - id: v110
    reference_refs:
    - cantina-sparklend-cap-automator-audit-v110
    version_label: v110
    status: current
    audited_codebases:
    - sparklend-cap-automator
    audited_sources:
    - codebase: sparklend-cap-automator
      path: src/CapAutomator.sol
    covered_contracts:
    - id: cap-automator
      name: CapAutomator
- id: certora-aave-v3-formal-verification
  auditor: Certora
  report_title: Aave V3 Formal Verification
  current_version: v2023-03
  versions:
  - id: v2023-03
    reference_refs:
    - certora-aave-v3-formal-verification-2023-03
    version_label: March 2023
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
- id: openzeppelin-aave-v3-audit
  auditor: OpenZeppelin
  report_title: Aave V3 Audit
  current_version: v2021-11-01
  versions:
  - id: v2021-11-01
    reference_refs:
    - openzeppelin-aave-v3-audit-2021-11-01
    version_label: 2021-11-01
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
- id: trail-of-bits-aave-v3-audit
  auditor: Trail of Bits
  report_title: Aave V3 Audit
  current_version: v2022-01-07
  versions:
  - id: v2022-01-07
    reference_refs:
    - trail-of-bits-aave-v3-audit-2022-01-07
    version_label: 2022-01-07
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
- id: peckshield-aave-v3-audit
  auditor: PeckShield
  report_title: Aave V3 Audit
  current_version: v2022-12-09
  versions:
  - id: v2022-12-09
    reference_refs:
    - peckshield-aave-v3-audit-2022-12-09
    version_label: 2022-12-09
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
- id: sigma-prime-aave-v3-audit
  auditor: Sigma Prime
  report_title: Aave V3 Audit
  current_version: v2023-04-19
  versions:
  - id: v2023-04-19
    reference_refs:
    - sigma-prime-aave-v3-audit-2023-04-19
    version_label: 2023-04-19
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
- id: abdk-aave-v3-audit
  auditor: ABDK
  report_title: Aave V3 Audit
  current_version: v2022-01-27
  versions:
  - id: v2022-01-27
    reference_refs:
    - abdk-aave-v3-audit-2022-01-27
    version_label: 2022-01-27
    status: current
    audited_codebases:
    - sparklend-v1-core
    scope_notes: Upstream Aave V3 report committed in the pinned sparklend-v1-core codebase.
references:
- id: chainsecurity-sparklend-advanced-audit-v160
  type: audit_report
  title: ChainSecurity SparkLend Advanced Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-advanced/cf5bc269af45b7a3b7a8e4e07ee5bbb0f65e5f76/audits/v160-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-sparklend-advanced-audit-v160.pdf
  date_checked: '2026-06-09'
  content_sha256: d4eef363c1cd8859283b8b4f20905094431fa07daf934063876fb812d91db6b7
- id: chainsecurity-sparklend-cap-automator-audit-v110
  type: audit_report
  title: ChainSecurity SparkLend Cap Automator Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-cap-automator/5c054cfddf4b8f21281ea4c23db3f0495f9aa8c5/audits/v110-chainsecurity-audit.pdf
  path: audit-reports/chainsecurity-sparklend-cap-automator-audit-v110.pdf
  date_checked: '2026-06-09'
  content_sha256: 336aedc7c51b1fefc15aa6fafdb53a1d1a5bb7a0ca44dca07d1dafba6f496ec8
- id: chainsecurity-sparklend-core-updates-audit-final
  type: audit_report
  title: ChainSecurity SparkLend Core Updates Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/ChainSecurity_Sparklend_Core_Updates_audit.pdf
  path: audit-reports/chainsecurity-sparklend-core-updates-audit-final.pdf
  date_checked: '2026-06-09'
  content_sha256: 7e68bdb5120fc3aebacde5d8a57745f5c211b767c1b0e23ae81a6f4aec19ec15
- id: chainsecurity-sparklend-freezer-audit-final
  type: audit_report
  title: ChainSecurity SparkLend Freezer Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-freezer/f87388bad3302b83d4ca9b92b9219527181f0586/audits/ChainSecurity_MakerDAO_SparkLend_Freezer_audit.pdf
  path: audit-reports/chainsecurity-sparklend-freezer-audit-final.pdf
  date_checked: '2026-06-09'
  content_sha256: f2e6a13f010e8b3742ec13a4615057693f644f89e5a9c48a273ac9a367154273
- id: chainsecurity-sparklend-kill-switch-audit-final
  type: audit_report
  title: ChainSecurity SparkLend Kill Switch Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-kill-switch/12cf956146bfb16498db961a8399d9c5fdf34e20/audits/ChainSecurity_Sparklend_Kill_Switch_audit.pdf
  path: audit-reports/chainsecurity-sparklend-kill-switch-audit-final.pdf
  date_checked: '2026-06-09'
  content_sha256: d8a89059b404f32d7ce9c903e79cb950361ac9137745508c0447afce0c898d70
- id: cantina-sparklend-advanced-audit-v160
  type: audit_report
  title: Cantina SparkLend Advanced Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-advanced/cf5bc269af45b7a3b7a8e4e07ee5bbb0f65e5f76/audits/v160-cantina-audit.pdf
  path: audit-reports/cantina-sparklend-advanced-audit-v160.pdf
  date_checked: '2026-06-09'
  content_sha256: 44f6b5578267c7be6dfbaa380a715cea3ace491bcc88a87cfc865a6a2a9c323a
- id: cantina-sparklend-cap-automator-audit-v110
  type: audit_report
  title: Cantina SparkLend Cap Automator Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-cap-automator/5c054cfddf4b8f21281ea4c23db3f0495f9aa8c5/audits/v110-cantina-audit.pdf
  path: audit-reports/cantina-sparklend-cap-automator-audit-v110.pdf
  date_checked: '2026-06-09'
  content_sha256: ee84088a66669321f12a109dd4e05a006d4727351c9a8aa0075990c46e34c39c
- id: certora-aave-v3-formal-verification-2023-03
  type: audit_report
  title: Certora Aave V3 Formal Verification
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/certora/Aave_V3.0.2_PR_820_Report_Mar2023.pdf
  path: audit-reports/certora-aave-v3-formal-verification-2023-03.pdf
  date_checked: '2026-06-09'
  content_sha256: 1920283191eb78cdc4bf40123249593f6458dbc50fc03d03de43eeb75e981594
- id: openzeppelin-aave-v3-audit-2021-11-01
  type: audit_report
  title: OpenZeppelin Aave V3 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/01-11-2021_OpenZeppelin_AaveV3.pdf
  path: audit-reports/openzeppelin-aave-v3-audit-2021-11-01.pdf
  date_published: '2021-11-01'
  date_checked: '2026-06-09'
  content_sha256: 7669e4e27cfa6ef25217e19a1f765d898edeb16d33b8ba00bc72ead0fe98395a
- id: trail-of-bits-aave-v3-audit-2022-01-07
  type: audit_report
  title: Trail of Bits Aave V3 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/07-01-2022_TrailOfBits_AaveV3.pdf
  path: audit-reports/trail-of-bits-aave-v3-audit-2022-01-07.pdf
  date_published: '2022-01-07'
  date_checked: '2026-06-09'
  content_sha256: 5e1e02bfa0497a09156b5e14105583c4f32d46c40427844103c7c5156829b32e
- id: peckshield-aave-v3-audit-2022-12-09
  type: audit_report
  title: PeckShield Aave V3 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/09-12-2022_PeckShield_AaveV3-0-1.pdf
  path: audit-reports/peckshield-aave-v3-audit-2022-12-09.pdf
  date_published: '2022-12-09'
  date_checked: '2026-06-09'
  content_sha256: 59b63d0916b3ab9a3c10c200f47119e88fe58a6fbd02f2a1f99a50e670bec88f
- id: sigma-prime-aave-v3-audit-2023-04-19
  type: audit_report
  title: Sigma Prime Aave V3 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/19-04-2023_SigmaPrime_AaveV3-0-2.pdf
  path: audit-reports/sigma-prime-aave-v3-audit-2023-04-19.pdf
  date_published: '2023-04-19'
  date_checked: '2026-06-09'
  content_sha256: 421ea17a333ad3ca0bfbec79edd4b2e2c524aa05cad32c0442e1c5f0427a6295
- id: abdk-aave-v3-audit-2022-01-27
  type: audit_report
  title: ABDK Aave V3 Audit
  url: https://raw.githubusercontent.com/sparkdotfi/sparklend-v1-core/8120e495061dc3315f0a86f682f4ca645a418bf7/audits/27-01-2022_ABDK_AaveV3.pdf
  path: audit-reports/abdk-aave-v3-audit-2022-01-27.pdf
  date_published: '2022-01-27'
  date_checked: '2026-06-09'
  content_sha256: 39d229b72646c80009af1e51893d6e56f0b18097a0e8713c4f4edae0b590763f
```

## Notes
