# Avalon tokens

## Features and design goals

- Best practices: Smart contracts are written with the latest best practices of Ethereum community
- Separation of concerns: token minting and crowdsale lies in separate contracts and managed by different companies that are assembled together
- Testable: We aim for 100% branch code coverage by automated test suite
- Auditable: Our tool chain supports verifiable EtherScan.io contract builds
- No inflation: the capped limit of 10M chips is hardcoded in the contract. It will never have new tokens generated later
- Build upon a foundation: Instead of building everything from the scratch, use OpenZeppelin contracts as much as possible as they are the gold standard of Solidity development

## Security
Avalon is meant to provide secure, tested and community-audited code

If you find a security issue, please email [security@avalon.nu](mailto:security@avalon.nu).

## Contract source verified

Smart contract is available on Etherscan to be auditable.
- [Proof of Concept](https://rinkeby.etherscan.io/address/0x76d177a05b4ddc8d398e09ecd4ea51527af7d1de#code)
- Avalon tokens (soon available)

## User Resources

Built with OpenZeppelin contracts.

- Read documentation: http://zeppelin-solidity.readthedocs.io/en/latest/

