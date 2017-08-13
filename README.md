# Avalon tokens

## Features and design goals

- Best practices: Smart contracts are written with the latest best practices of Ethereum community
- Separation of concerns: Token minting and crowdsale lie in separate contracts and are managed by different companies that are assembled together
- Testable: We aim for 100% branch code coverage by automated test suite
- Auditable: Our tool chain supports verifiable EtherScan.io contract builds
- No inflation: The capped limit of 10M chips is hardcoded in the contract. This limit can never be crossed
- Build upon a foundation: Instead of building everything from scratch, OpenZeppelin contracts are used as much as possible as they are the gold standard of Solidity development

## Security
Avalon undertakes to provide secure, tested and community-audited code.
If you find a security issue, please email [security@avalon.nu](mailto:security@avalon.nu)

## Contract source verified

Smart contract is available on Etherscan to be auditable.
- Avalon tokens: [0xeD247980396B10169BB1d36f6e278eD16700a60f](https://etherscan.io/address/0xed247980396b10169bb1d36f6e278ed16700a60f#code)

## User Resources

Built with OpenZeppelin contracts.
- Read documentation: [zeppelin-solidity.readthedocs.io](http://zeppelin-solidity.readthedocs.io/en/latest/)

---

# Multi signatures tokens wallet

## Features and design goals

- Managing tokens of an ERC20 contract using a multi signatures wallet
- Allow the addition and removal of an owner (if the quorum is reached)
- Allow the quorum to be modified (if the quorum is reached)

## Instructions

- Update the ERC20 contract address at the beginning of the script
- Deploy the contract with the following constructor parameters \[\"\<address_owner_1\>\", "\<\address_owner_2\>\",...\],\<Quorum\>
- Transfer eventually some tokens to the contract address
- Submit an action with public **submitAction** function. Parameters are \<address\>, \<value\>, \<action\> where the action is
  - 0: Transfer \<value\> tokens to address
  - 1: Add owner whose address is \<address\>
  - 2: Remove owner whose address is \<address\>    
  - 3: Modify quorum with the new value \<value\>
  - 4: Delete a previous action that is not already executed. The ID of this action is \<value\>
- All previous actions have to be confirmed to reach the quorum with the public **confirmAction** function (parameter: Action ID). Confirmation can be cancelled with the **revokeCofirmation** function
- Once the quorum is reached, the action can be executed with the public **excecuteAction** function (parameter : Action ID) 

## Security

Multi signatures token wallet contract is WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. This contract was created for the internal needs of Avalon Platform and it is still in Beta test stage. Its use is at your own risk

## Deployed instances with significant funds

- Avalon Platform [available soon](https://etherscan.io/)

