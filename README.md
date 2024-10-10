# Symbiotic CLI (symb)

Simple CLI tool for fetching data from symbiotic core smart contracts.

## Install

```bash
pip3 install -r requirements.txt
```

## Usage

```
$ python3 symb.py
Usage: symb.py [OPTIONS] COMMAND [ARGS]...

Options:
  --provider        TEXT  Ethereum provider URL [http(s)]
  --help                  Show this message and exit.
  --private-key     TEXT  Private key to sign transactions with (only for write functionality).
  --ledger                Flag if to use a ledger to sign transactions (only for write functionality). Make sure to install Ledger Live, open the Ethereum app, and enable the blind signing first.
  --ledger-address  TEXT  Address of the ledger's account to use to sign transactions (only for write functionality).


Commands:
  --- for general use (related to Networks) ---

  isnet                        Check if address is network.
  middleware                   Get network middleware address.
  nets                         List all networks.
  netops                       List all operators opted in network.
  netstakes                    Show stakes of all operators in network.

  --- for general use (related to Operators) ---

  isop                         Check if address is operator.
  ops                          List all operators.
  opnets                       List all networks where operator is opted in.
  op-vault-net-stake           Get operator stake in vault for network (includes data about the operator's shares if NetworkRestakeDelegator).
  opstakes                     Show operator stakes in all networks.

  --- for general use (related to Vaults) ---

  isvault                      Check if address is vault.
  vaults                       List all vaults.
  vaultnets                    List all networks associated with the given vault.
  vaultops                     List all operators opted into the given vault.
  vaultnetsops                 List all operators and their associated networks for the given vault.

  --- for Networks ---

  register-network             Register the signer as a network.
  set-max-network-limit        Set a maximum network limit at the vault's delegator.
  pending-resolver             Get a current resolver for a subnetwork in a vault.
  resolver                     Get a pending resolver for a subnetwork in a vault.
  set-resolver                 Set a resolver for a subnetwork at VetoSlasher.

  --- for Operators ---

  register-operator            Register the signer as an operator.
  check-opt-in-network         Check if operator is opted in to a network.
  check-opt-in-vault           Check if is opted in to a vault.
  opt-in-network               Opt-in to a network.
  opt-in-vault                 Opt-in to a vault.
  opt-out-network              Opt-out from a network.
  opt-out-vault                Opt-out from a vault.

  --- for Vault Curators ---

  set-network-limit            Set a network limit at the vault's delegator.
  set-operator-network-limit   Set an operator-network limit at the vault's delegator.
  set-operator-network-shares  Set an operator-network shares at the vault's delegator.
```
