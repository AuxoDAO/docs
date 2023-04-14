---
description: This page details the main smart contract addresses for the Auxo Protocol
---

# Deployed Smart Contracts

## Mainnet Addresses

| Name                    | Contract Address                           | Description                                              |
| ----------------------- | ------------------------------------------ | -------------------------------------------------------- |
| Governor                | 0xB320Fc09B272D1658E99488ADc614E4645B1d83c | Auxo Governor Contract                                   |
| TimelockController      | 0xdC554207e4EE62bB05AeC99b3D2C6ab2106D6442 | Auxo Governance Timelock                                 |
| Auxo                    | 0xff030228a046F640143Dab19be00009606C89B1d | Auxo ERC20 Token                                         |
| ARV                     | 0x069c0Ed12dB7199c1DdAF73b94de75AAe8061d33 | Auxo Active Rewards Vault ERC20                          |
| TokenLocker\*           | 0x3E70FF09C8f53294FFd389a7fcF7276CC3d92e64 | Auxo Locker that mints ARV                               |
| Oracle                  | 0xe568B2d96a139126B2042a4e0c9fA1755bf5FB70 | ARV Rewards Boost                                        |
| MerkleDistributor ARV\* | 0x727a21924D9267E49D025a48464324edfcD215B5 | Reward Distribution Contract for ARV holders             |
| PRV\*                   | 0xc72fbD264b40D88E445bcf82663D63FF21e722AF | Auxo Passive Rewards Vault ERC20                         |
| RollStaker\*            | 0x096b4F2253a430F33edc9B8e6A8e1d2fb4faA317 | PRV Staking contract for rewards                         |
| PRV Router              | 0xEE2b00267188c60aaF1d46EA5c8f4B36006FA6Cc | Utility Contract for PRV Staking                         |
| MerkleDistributor PRV\* | 0x06c88C0FD7296717083C0A449C854005218095c5 | Reward Distribution Contract for PRV holders             |
| MerkleVerifier\*        | 0x8213f2C1e0BBd8891632EAA5f9A324560ECc394B | PRV Withdrawal Manager                                   |
| ClaimHelper             | 0x2cd92e3a127A476b14451a62A1BFF16f24A3aedd | Utility contract for claiming rewards across ARV and PRV |

\*_This contract is upgradeable, the address provided points to the Proxy contract. The current implementation can be fetched from the proxy._&#x20;

## Migration Contracts

_Temporary contracts used in the Auxo migration_

|          |                                            |                          |
| -------- | ------------------------------------------ | ------------------------ |
| Upgrador | 0x02f4573F7b332fa73E219759f4E06b3Ed10A0ae1 | Auxo Bridge from veDOUGH |
