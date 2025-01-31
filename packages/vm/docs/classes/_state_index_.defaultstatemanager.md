[@ethereumjs/vm](../README.md) › ["state/index"](../modules/_state_index_.md) › [DefaultStateManager](_state_index_.defaultstatemanager.md)

# Class: DefaultStateManager

Interface for getting and setting data from an underlying
state trie.

## Hierarchy

* **DefaultStateManager**

## Implements

* [StateManager](../interfaces/_state_index_.statemanager.md)

## Index

### Constructors

* [constructor](_state_index_.defaultstatemanager.md#constructor)

### Properties

* [_accessedStorage](_state_index_.defaultstatemanager.md#_accessedstorage)
* [_accessedStorageReverted](_state_index_.defaultstatemanager.md#_accessedstoragereverted)
* [_cache](_state_index_.defaultstatemanager.md#_cache)
* [_checkpointCount](_state_index_.defaultstatemanager.md#_checkpointcount)
* [_common](_state_index_.defaultstatemanager.md#_common)
* [_originalStorageCache](_state_index_.defaultstatemanager.md#_originalstoragecache)
* [_storageTries](_state_index_.defaultstatemanager.md#_storagetries)
* [_touched](_state_index_.defaultstatemanager.md#_touched)
* [_touchedStack](_state_index_.defaultstatemanager.md#_touchedstack)
* [_trie](_state_index_.defaultstatemanager.md#_trie)

### Methods

* [_clearOriginalStorageCache](_state_index_.defaultstatemanager.md#_clearoriginalstoragecache)
* [_getStorageTrie](_state_index_.defaultstatemanager.md#private-_getstoragetrie)
* [_lookupStorageTrie](_state_index_.defaultstatemanager.md#private-_lookupstoragetrie)
* [_modifyContractStorage](_state_index_.defaultstatemanager.md#private-_modifycontractstorage)
* [accountExists](_state_index_.defaultstatemanager.md#accountexists)
* [accountIsEmpty](_state_index_.defaultstatemanager.md#accountisempty)
* [addWarmedAddress](_state_index_.defaultstatemanager.md#addwarmedaddress)
* [addWarmedStorage](_state_index_.defaultstatemanager.md#addwarmedstorage)
* [checkpoint](_state_index_.defaultstatemanager.md#checkpoint)
* [cleanupTouchedAccounts](_state_index_.defaultstatemanager.md#cleanuptouchedaccounts)
* [clearContractStorage](_state_index_.defaultstatemanager.md#clearcontractstorage)
* [clearOriginalStorageCache](_state_index_.defaultstatemanager.md#clearoriginalstoragecache)
* [clearWarmedAccounts](_state_index_.defaultstatemanager.md#clearwarmedaccounts)
* [commit](_state_index_.defaultstatemanager.md#commit)
* [copy](_state_index_.defaultstatemanager.md#copy)
* [deleteAccount](_state_index_.defaultstatemanager.md#deleteaccount)
* [dumpStorage](_state_index_.defaultstatemanager.md#dumpstorage)
* [generateAccessList](_state_index_.defaultstatemanager.md#generateaccesslist)
* [generateCanonicalGenesis](_state_index_.defaultstatemanager.md#generatecanonicalgenesis)
* [generateGenesis](_state_index_.defaultstatemanager.md#generategenesis)
* [getAccount](_state_index_.defaultstatemanager.md#getaccount)
* [getContractCode](_state_index_.defaultstatemanager.md#getcontractcode)
* [getContractStorage](_state_index_.defaultstatemanager.md#getcontractstorage)
* [getOriginalContractStorage](_state_index_.defaultstatemanager.md#getoriginalcontractstorage)
* [getStateRoot](_state_index_.defaultstatemanager.md#getstateroot)
* [hasGenesisState](_state_index_.defaultstatemanager.md#hasgenesisstate)
* [isWarmedAddress](_state_index_.defaultstatemanager.md#iswarmedaddress)
* [isWarmedStorage](_state_index_.defaultstatemanager.md#iswarmedstorage)
* [putAccount](_state_index_.defaultstatemanager.md#putaccount)
* [putContractCode](_state_index_.defaultstatemanager.md#putcontractcode)
* [putContractStorage](_state_index_.defaultstatemanager.md#putcontractstorage)
* [revert](_state_index_.defaultstatemanager.md#revert)
* [setStateRoot](_state_index_.defaultstatemanager.md#setstateroot)
* [touchAccount](_state_index_.defaultstatemanager.md#touchaccount)

## Constructors

###  constructor

\+ **new DefaultStateManager**(`opts`: [DefaultStateManagerOpts](../interfaces/_state_statemanager_.defaultstatemanageropts.md)): *[DefaultStateManager](_state_index_.defaultstatemanager.md)*

*Defined in [state/stateManager.ts:66](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L66)*

Instantiate the StateManager interface.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`opts` | [DefaultStateManagerOpts](../interfaces/_state_statemanager_.defaultstatemanageropts.md) | {} |

**Returns:** *[DefaultStateManager](_state_index_.defaultstatemanager.md)*

## Properties

###  _accessedStorage

• **_accessedStorage**: *Map‹string, Set‹string››[]*

*Defined in [state/stateManager.ts:62](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L62)*

___

###  _accessedStorageReverted

• **_accessedStorageReverted**: *Map‹string, Set‹string››[]*

*Defined in [state/stateManager.ts:66](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L66)*

___

###  _cache

• **_cache**: *Cache*

*Defined in [state/stateManager.ts:48](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L48)*

___

###  _checkpointCount

• **_checkpointCount**: *number*

*Defined in [state/stateManager.ts:51](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L51)*

___

###  _common

• **_common**: *Common*

*Defined in [state/stateManager.ts:45](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L45)*

___

###  _originalStorageCache

• **_originalStorageCache**: *Map‹AddressHex, Map‹AddressHex, Buffer››*

*Defined in [state/stateManager.ts:52](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L52)*

___

###  _storageTries

• **_storageTries**: *object*

*Defined in [state/stateManager.ts:47](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L47)*

#### Type declaration:

* \[ **key**: *string*\]: Trie

___

###  _touched

• **_touched**: *Set‹AddressHex›*

*Defined in [state/stateManager.ts:49](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L49)*

___

###  _touchedStack

• **_touchedStack**: *Set‹AddressHex›[]*

*Defined in [state/stateManager.ts:50](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L50)*

___

###  _trie

• **_trie**: *Trie*

*Defined in [state/stateManager.ts:46](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L46)*

## Methods

###  _clearOriginalStorageCache

▸ **_clearOriginalStorageCache**(): *void*

*Defined in [state/stateManager.ts:269](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L269)*

Clears the original storage cache. Refer to [getOriginalContractStorage](_state_index_.defaultstatemanager.md#getoriginalcontractstorage)
for more explanation.

**Returns:** *void*

___

### `Private` _getStorageTrie

▸ **_getStorageTrie**(`address`: Address): *Promise‹Trie›*

*Defined in [state/stateManager.ts:201](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L201)*

Gets the storage trie for an account from the storage
cache or does a lookup.

**Parameters:**

Name | Type |
------ | ------ |
`address` | Address |

**Returns:** *Promise‹Trie›*

___

### `Private` _lookupStorageTrie

▸ **_lookupStorageTrie**(`address`: Address): *Promise‹Trie›*

*Defined in [state/stateManager.ts:187](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L187)*

Creates a storage trie from the primary storage trie
for an account and saves this in the storage cache.

**Parameters:**

Name | Type |
------ | ------ |
`address` | Address |

**Returns:** *Promise‹Trie›*

___

### `Private` _modifyContractStorage

▸ **_modifyContractStorage**(`address`: Address, `modifyTrie`: function): *Promise‹void›*

*Defined in [state/stateManager.ts:287](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L287)*

Modifies the storage trie of an account.

**Parameters:**

▪ **address**: *Address*

Address of the account whose storage is to be modified

▪ **modifyTrie**: *function*

Function to modify the storage trie of the account

▸ (`storageTrie`: Trie, `done`: Function): *void*

**Parameters:**

Name | Type |
------ | ------ |
`storageTrie` | Trie |
`done` | Function |

**Returns:** *Promise‹void›*

___

###  accountExists

▸ **accountExists**(`address`: Address): *Promise‹boolean›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:586](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L586)*

Checks if the `account` corresponding to `address`
exists

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the `account` to check  |

**Returns:** *Promise‹boolean›*

___

###  accountIsEmpty

▸ **accountIsEmpty**(`address`: Address): *Promise‹boolean›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:576](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L576)*

Checks if the `account` corresponding to `address`
is empty or non-existent as defined in
EIP-161 (https://eips.ethereum.org/EIPS/eip-161).

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address to check  |

**Returns:** *Promise‹boolean›*

___

###  addWarmedAddress

▸ **addWarmedAddress**(`address`: Buffer): *void*

*Defined in [state/stateManager.ts:619](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L619)*

Add a warm address in the current context

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Buffer | The address (as a Buffer) to check  |

**Returns:** *void*

___

###  addWarmedStorage

▸ **addWarmedStorage**(`address`: Buffer, `slot`: Buffer): *void*

*Defined in [state/stateManager.ts:652](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L652)*

Mark the storage slot in the address as warm in the current context

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Buffer | The address (as a Buffer) to check |
`slot` | Buffer | The slot (as a Buffer) to check  |

**Returns:** *void*

___

###  checkpoint

▸ **checkpoint**(): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:360](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L360)*

Checkpoints the current state of the StateManager instance.
State changes that follow can then be committed by calling
`commit` or `reverted` by calling rollback.

**Returns:** *Promise‹void›*

___

###  cleanupTouchedAccounts

▸ **cleanupTouchedAccounts**(): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:732](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L732)*

Removes accounts form the state trie that have been touched,
as defined in EIP-161 (https://eips.ethereum.org/EIPS/eip-161).

**Returns:** *Promise‹void›*

___

###  clearContractStorage

▸ **clearContractStorage**(`address`: Address): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:348](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L348)*

Clears all storage entries for the account corresponding to `address`.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address to clear the storage of  |

**Returns:** *Promise‹void›*

___

###  clearOriginalStorageCache

▸ **clearOriginalStorageCache**(): *void*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:277](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L277)*

Clears the original storage cache. Refer to [getOriginalContractStorage](_state_index_.defaultstatemanager.md#getoriginalcontractstorage)
for more explanation. Alias of the internal _clearOriginalStorageCache

**Returns:** *void*

___

###  clearWarmedAccounts

▸ **clearWarmedAccounts**(): *void*

*Defined in [state/stateManager.ts:666](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L666)*

Clear the warm accounts and storage. To be called after a transaction finished.

**Returns:** *void*

___

###  commit

▸ **commit**(): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:396](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L396)*

Commits the current change-set to the instance since the
last call to checkpoint.

**Returns:** *Promise‹void›*

___

###  copy

▸ **copy**(): *[StateManager](../interfaces/_state_index_.statemanager.md)*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:94](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L94)*

Copies the current instance of the `StateManager`
at the last fully committed point, i.e. as if all current
checkpoints were reverted.

**Returns:** *[StateManager](../interfaces/_state_index_.statemanager.md)*

___

###  deleteAccount

▸ **deleteAccount**(`address`: Address): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:129](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L129)*

Deletes an account from state under the provided `address`. The account will also be removed from the state trie.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the account which should be deleted  |

**Returns:** *Promise‹void›*

___

###  dumpStorage

▸ **dumpStorage**(`address`: Address): *Promise‹[StorageDump](../interfaces/_state_interface_.storagedump.md)›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:504](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L504)*

Dumps the RLP-encoded storage values for an `account` specified by `address`.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | The address of the `account` to return storage for |

**Returns:** *Promise‹[StorageDump](../interfaces/_state_interface_.storagedump.md)›*

- The state of the account as an `Object` map.
Keys are are the storage keys, values are the storage values as strings.
Both are represented as hex strings without the `0x` prefix.

___

###  generateAccessList

▸ **generateAccessList**(`addressesRemoved`: Address[], `addressesOnlyStorage`: Address[]): *AccessList*

*Defined in [state/stateManager.ts:688](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L688)*

Generates an EIP-2930 access list

Note: this method is not yet part of the `StateManager` interface.
If not implemented, `runTx()` is not allowed to be used with the
`reportAccessList` option and will instead throw.

Note: there is an edge case on accessList generation where an
internal call might revert without an accessList but pass if the
accessList is used for a tx run (so the subsequent behavior might change).
This edge case is not covered by this implementation.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`addressesRemoved` | Address[] | [] | List of addresses to be removed from the final list |
`addressesOnlyStorage` | Address[] | [] | List of addresses only to be added in case of present storage slots  |

**Returns:** *AccessList*

- an [@ethereumjs/tx](https://github.com/ethereumjs/ethereumjs-monorepo/packages/tx) `AccessList`

___

###  generateCanonicalGenesis

▸ **generateCanonicalGenesis**(): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:540](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L540)*

Generates a canonical genesis state on the instance based on the
configured chain parameters. Will error if there are uncommitted
checkpoints on the instance.

**Returns:** *Promise‹void›*

___

###  generateGenesis

▸ **generateGenesis**(`initState`: any): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:555](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L555)*

Initializes the provided genesis state into the state trie

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`initState` | any | Object (address -> balance)  |

**Returns:** *Promise‹void›*

___

###  getAccount

▸ **getAccount**(`address`: Address): *Promise‹Account›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:105](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L105)*

Gets the account associated with `address`. Returns an empty account if the account does not exist.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the `account` to get  |

**Returns:** *Promise‹Account›*

___

###  getContractCode

▸ **getContractCode**(`address`: Address): *Promise‹Buffer›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:173](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L173)*

Gets the code corresponding to the provided `address`.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address to get the `code` for |

**Returns:** *Promise‹Buffer›*

-  Resolves with the code corresponding to the provided address.
Returns an empty `Buffer` if the account has no associated code.

___

###  getContractStorage

▸ **getContractStorage**(`address`: Address, `key`: Buffer): *Promise‹Buffer›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:221](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L221)*

Gets the storage value associated with the provided `address` and `key`. This method returns
the shortest representation of the stored value.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the account to get the storage for |
`key` | Buffer | Key in the account's storage to get the value for. Must be 32 bytes long. |

**Returns:** *Promise‹Buffer›*

- The storage value for the account
corresponding to the provided address at the provided key.
If this does not exist an empty `Buffer` is returned.

___

###  getOriginalContractStorage

▸ **getOriginalContractStorage**(`address`: Address, `key`: Buffer): *Promise‹Buffer›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:240](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L240)*

Caches the storage value associated with the provided `address` and `key`
on first invocation, and returns the cached (original) value from then
onwards. This is used to get the original value of a storage slot for
computing gas costs according to EIP-1283.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the account to get the storage for |
`key` | Buffer | Key in the account's storage to get the value for. Must be 32 bytes long.  |

**Returns:** *Promise‹Buffer›*

___

###  getStateRoot

▸ **getStateRoot**(`force`: boolean): *Promise‹Buffer›*

*Defined in [state/stateManager.ts:457](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L457)*

Gets the state-root of the Merkle-Patricia trie representation
of the state of this StateManager. Will error if there are uncommitted
checkpoints on the instance.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`force` | boolean | false | If set to `true`, force a cache flush even if there are uncommited checkpoints (this is set to `true` pre-Byzantium in order to get intermediate state roots for the receipts) |

**Returns:** *Promise‹Buffer›*

- Returns the state-root of the `StateManager`

___

###  hasGenesisState

▸ **hasGenesisState**(): *Promise‹boolean›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:530](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L530)*

Checks whether the current instance has the canonical genesis state
for the configured chain parameters.

**Returns:** *Promise‹boolean›*

- Whether the storage trie contains the
canonical genesis state for the configured chain parameters.

___

###  isWarmedAddress

▸ **isWarmedAddress**(`address`: Buffer): *boolean*

*Defined in [state/stateManager.ts:605](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L605)*

Returns true if the address is warm in the current context

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Buffer | The address (as a Buffer) to check  |

**Returns:** *boolean*

___

###  isWarmedStorage

▸ **isWarmedStorage**(`address`: Buffer, `slot`: Buffer): *boolean*

*Defined in [state/stateManager.ts:633](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L633)*

Returns true if the slot of the address is warm

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Buffer | The address (as a Buffer) to check |
`slot` | Buffer | The slot (as a Buffer) to check  |

**Returns:** *boolean*

___

###  putAccount

▸ **putAccount**(`address`: Address, `account`: Account): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:115](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L115)*

Saves an account into state under the provided `address`.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address under which to store `account` |
`account` | Account | The account to store  |

**Returns:** *Promise‹void›*

___

###  putContractCode

▸ **putContractCode**(`address`: Address, `value`: Buffer): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:152](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L152)*

Adds `value` to the state trie as code, and sets `codeHash` on the account
corresponding to `address` to reference this.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address of the `account` to add the `code` for |
`value` | Buffer | The value of the `code`  |

**Returns:** *Promise‹void›*

___

###  putContractStorage

▸ **putContractStorage**(`address`: Address, `key`: Buffer, `value`: Buffer): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:318](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L318)*

Adds value to the state trie for the `account`
corresponding to `address` at the provided `key`.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`address` | Address | Address to set a storage value for |
`key` | Buffer | Key to set the value at. Must be 32 bytes long. |
`value` | Buffer | Value to set at `key` for account corresponding to `address`. Cannot be more than 32 bytes. Leading zeros are stripped. If it is a empty or filled with zeros, deletes the value.  |

**Returns:** *Promise‹void›*

___

###  revert

▸ **revert**(): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:420](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L420)*

Reverts the current change-set to the instance since the
last call to checkpoint.

**Returns:** *Promise‹void›*

___

###  setStateRoot

▸ **setStateRoot**(`stateRoot`: Buffer): *Promise‹void›*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:473](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L473)*

Sets the state of the instance to that represented
by the provided `stateRoot`. Will error if there are uncommitted
checkpoints on the instance or if the state root does not exist in
the state trie.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`stateRoot` | Buffer | The state-root to reset the instance to  |

**Returns:** *Promise‹void›*

___

###  touchAccount

▸ **touchAccount**(`address`: Address): *void*

*Implementation of [StateManager](../interfaces/_state_index_.statemanager.md)*

*Defined in [state/stateManager.ts:142](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/vm/lib/state/stateManager.ts#L142)*

Marks an account as touched, according to the definition
in [EIP-158](https://eips.ethereum.org/EIPS/eip-158).
This happens when the account is triggered for a state-changing
event. Touched accounts that are empty will be cleared
at the end of the tx.

**Parameters:**

Name | Type |
------ | ------ |
`address` | Address |

**Returns:** *void*
