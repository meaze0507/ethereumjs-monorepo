[@ethereumjs/tx](../README.md) › ["eip2930Transaction"](../modules/_eip2930transaction_.md) › [AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)

# Class: AccessListEIP2930Transaction

Typed transaction with optional access lists

- TransactionType: 1
- EIP: [EIP-2930](https://eips.ethereum.org/EIPS/eip-2930)

## Hierarchy

* [BaseTransaction](_basetransaction_.basetransaction.md)‹[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)›

  ↳ **AccessListEIP2930Transaction**

## Index

### Constructors

* [constructor](_eip2930transaction_.accesslisteip2930transaction.md#constructor)

### Properties

* [AccessListJSON](_eip2930transaction_.accesslisteip2930transaction.md#accesslistjson)
* [accessList](_eip2930transaction_.accesslisteip2930transaction.md#accesslist)
* [chainId](_eip2930transaction_.accesslisteip2930transaction.md#chainid)
* [common](_eip2930transaction_.accesslisteip2930transaction.md#common)
* [data](_eip2930transaction_.accesslisteip2930transaction.md#data)
* [gasLimit](_eip2930transaction_.accesslisteip2930transaction.md#gaslimit)
* [gasPrice](_eip2930transaction_.accesslisteip2930transaction.md#gasprice)
* [nonce](_eip2930transaction_.accesslisteip2930transaction.md#nonce)
* [r](_eip2930transaction_.accesslisteip2930transaction.md#optional-r)
* [s](_eip2930transaction_.accesslisteip2930transaction.md#optional-s)
* [to](_eip2930transaction_.accesslisteip2930transaction.md#optional-to)
* [v](_eip2930transaction_.accesslisteip2930transaction.md#optional-v)
* [value](_eip2930transaction_.accesslisteip2930transaction.md#value)

### Accessors

* [senderR](_eip2930transaction_.accesslisteip2930transaction.md#senderr)
* [senderS](_eip2930transaction_.accesslisteip2930transaction.md#senders)
* [transactionType](_eip2930transaction_.accesslisteip2930transaction.md#transactiontype)
* [yParity](_eip2930transaction_.accesslisteip2930transaction.md#yparity)

### Methods

* [_processSignature](_eip2930transaction_.accesslisteip2930transaction.md#_processsignature)
* [getBaseFee](_eip2930transaction_.accesslisteip2930transaction.md#getbasefee)
* [getDataFee](_eip2930transaction_.accesslisteip2930transaction.md#getdatafee)
* [getMessageToSign](_eip2930transaction_.accesslisteip2930transaction.md#getmessagetosign)
* [getMessageToVerifySignature](_eip2930transaction_.accesslisteip2930transaction.md#getmessagetoverifysignature)
* [getSenderAddress](_eip2930transaction_.accesslisteip2930transaction.md#getsenderaddress)
* [getSenderPublicKey](_eip2930transaction_.accesslisteip2930transaction.md#getsenderpublickey)
* [getUpfrontCost](_eip2930transaction_.accesslisteip2930transaction.md#getupfrontcost)
* [hash](_eip2930transaction_.accesslisteip2930transaction.md#hash)
* [isSigned](_eip2930transaction_.accesslisteip2930transaction.md#issigned)
* [raw](_eip2930transaction_.accesslisteip2930transaction.md#raw)
* [serialize](_eip2930transaction_.accesslisteip2930transaction.md#serialize)
* [sign](_eip2930transaction_.accesslisteip2930transaction.md#sign)
* [toCreationAddress](_eip2930transaction_.accesslisteip2930transaction.md#tocreationaddress)
* [toJSON](_eip2930transaction_.accesslisteip2930transaction.md#tojson)
* [validate](_eip2930transaction_.accesslisteip2930transaction.md#validate)
* [verifySignature](_eip2930transaction_.accesslisteip2930transaction.md#verifysignature)
* [fromRlpSerializedTx](_eip2930transaction_.accesslisteip2930transaction.md#static-fromrlpserializedtx)
* [fromSerializedTx](_eip2930transaction_.accesslisteip2930transaction.md#static-fromserializedtx)
* [fromTxData](_eip2930transaction_.accesslisteip2930transaction.md#static-fromtxdata)
* [fromValuesArray](_eip2930transaction_.accesslisteip2930transaction.md#static-fromvaluesarray)

## Constructors

###  constructor

\+ **new AccessListEIP2930Transaction**(`txData`: [AccessListEIP2930TxData](../interfaces/_index_.accesslisteip2930txdata.md), `opts`: [TxOptions](../interfaces/_index_.txoptions.md)): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[constructor](_basetransaction_.basetransaction.md#constructor)*

*Defined in [eip2930Transaction.ts:131](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L131)*

This constructor takes the values, validates them, assigns them and freezes the object.

It is not recommended to use this constructor directly. Instead use
the static factory methods to assist in creating a Transaction object from
varying data types.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`txData` | [AccessListEIP2930TxData](../interfaces/_index_.accesslisteip2930txdata.md) | - |
`opts` | [TxOptions](../interfaces/_index_.txoptions.md) | {} |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)*

## Properties

###  AccessListJSON

• **AccessListJSON**: *[AccessList](../modules/_index_.md#accesslist)*

*Defined in [eip2930Transaction.ts:38](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L38)*

___

###  accessList

• **accessList**: *[AccessListBuffer](../modules/_index_.md#accesslistbuffer)*

*Defined in [eip2930Transaction.ts:37](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L37)*

___

###  chainId

• **chainId**: *BN*

*Defined in [eip2930Transaction.ts:36](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L36)*

___

###  common

• **common**: *Common*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[common](_basetransaction_.basetransaction.md#common)*

*Defined in [baseTransaction.ts:27](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L27)*

___

###  data

• **data**: *Buffer*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[data](_basetransaction_.basetransaction.md#data)*

*Defined in [baseTransaction.ts:26](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L26)*

___

###  gasLimit

• **gasLimit**: *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[gasLimit](_basetransaction_.basetransaction.md#gaslimit)*

*Defined in [baseTransaction.ts:22](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L22)*

___

###  gasPrice

• **gasPrice**: *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[gasPrice](_basetransaction_.basetransaction.md#gasprice)*

*Defined in [baseTransaction.ts:23](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L23)*

___

###  nonce

• **nonce**: *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[nonce](_basetransaction_.basetransaction.md#nonce)*

*Defined in [baseTransaction.ts:21](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L21)*

___

### `Optional` r

• **r**? : *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[r](_basetransaction_.basetransaction.md#optional-r)*

*Defined in [baseTransaction.ts:30](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L30)*

___

### `Optional` s

• **s**? : *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[s](_basetransaction_.basetransaction.md#optional-s)*

*Defined in [baseTransaction.ts:31](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L31)*

___

### `Optional` to

• **to**? : *Address*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[to](_basetransaction_.basetransaction.md#optional-to)*

*Defined in [baseTransaction.ts:24](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L24)*

___

### `Optional` v

• **v**? : *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[v](_basetransaction_.basetransaction.md#optional-v)*

*Defined in [baseTransaction.ts:29](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L29)*

___

###  value

• **value**: *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[value](_basetransaction_.basetransaction.md#value)*

*Defined in [baseTransaction.ts:25](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L25)*

## Accessors

###  senderR

• **get senderR**(): *undefined | BN‹›*

*Defined in [eip2930Transaction.ts:50](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L50)*

**Returns:** *undefined | BN‹›*

___

###  senderS

• **get senderS**(): *undefined | BN‹›*

*Defined in [eip2930Transaction.ts:45](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L45)*

**Returns:** *undefined | BN‹›*

___

###  transactionType

• **get transactionType**(): *number*

*Defined in [eip2930Transaction.ts:40](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L40)*

**Returns:** *number*

___

###  yParity

• **get yParity**(): *undefined | BN‹›*

*Defined in [eip2930Transaction.ts:55](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L55)*

**Returns:** *undefined | BN‹›*

## Methods

###  _processSignature

▸ **_processSignature**(`v`: number, `r`: Buffer, `s`: Buffer): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

*Defined in [eip2930Transaction.ts:339](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L339)*

**Parameters:**

Name | Type |
------ | ------ |
`v` | number |
`r` | Buffer |
`s` | Buffer |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

___

###  getBaseFee

▸ **getBaseFee**(): *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[getBaseFee](_basetransaction_.basetransaction.md#getbasefee)*

*Defined in [baseTransaction.ts:85](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L85)*

The minimum amount of gas the tx must have (DataFee + TxFee + Creation Fee)

**Returns:** *BN*

___

###  getDataFee

▸ **getDataFee**(): *BN*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[getDataFee](_basetransaction_.basetransaction.md#getdatafee)*

*Defined in [eip2930Transaction.ts:232](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L232)*

The amount of gas paid for the data in this tx

**Returns:** *BN*

___

###  getMessageToSign

▸ **getMessageToSign**(): *Buffer‹›*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[getMessageToSign](_basetransaction_.basetransaction.md#abstract-getmessagetosign)*

*Defined in [eip2930Transaction.ts:281](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L281)*

Computes a sha3-256 hash of the serialized unsigned tx, which is used to sign the transaction.

**Returns:** *Buffer‹›*

___

###  getMessageToVerifySignature

▸ **getMessageToVerifySignature**(): *Buffer*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[getMessageToVerifySignature](_basetransaction_.basetransaction.md#abstract-getmessagetoverifysignature)*

*Defined in [eip2930Transaction.ts:300](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L300)*

Computes a sha3-256 hash which can be used to verify the signature

**Returns:** *Buffer*

___

###  getSenderAddress

▸ **getSenderAddress**(): *Address*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[getSenderAddress](_basetransaction_.basetransaction.md#getsenderaddress)*

*Defined in [baseTransaction.ts:161](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L161)*

Returns the sender's address

**Returns:** *Address*

___

###  getSenderPublicKey

▸ **getSenderPublicKey**(): *Buffer*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[getSenderPublicKey](_basetransaction_.basetransaction.md#abstract-getsenderpublickey)*

*Defined in [eip2930Transaction.ts:307](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L307)*

Returns the public key of the sender

**Returns:** *Buffer*

___

###  getUpfrontCost

▸ **getUpfrontCost**(): *BN*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[getUpfrontCost](_basetransaction_.basetransaction.md#getupfrontcost)*

*Defined in [baseTransaction.ts:110](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L110)*

The up front amount that an account must have for this transaction to be valid

**Returns:** *BN*

___

###  hash

▸ **hash**(): *Buffer*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[hash](_basetransaction_.basetransaction.md#abstract-hash)*

*Defined in [eip2930Transaction.ts:289](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L289)*

Computes a sha3-256 hash of the serialized tx

**Returns:** *Buffer*

___

###  isSigned

▸ **isSigned**(): *boolean*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[isSigned](_basetransaction_.basetransaction.md#issigned)*

*Defined in [baseTransaction.ts:140](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L140)*

**Returns:** *boolean*

___

###  raw

▸ **raw**(): *[AccessListEIP2930ValuesArray](../modules/_index_.md#accesslisteip2930valuesarray)*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[raw](_basetransaction_.basetransaction.md#abstract-raw)*

*Defined in [eip2930Transaction.ts:254](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L254)*

Returns a Buffer Array of the raw Buffers of this transaction, in order.

Use `serialize()` to add to block data for `Block.fromValuesArray()`.

**Returns:** *[AccessListEIP2930ValuesArray](../modules/_index_.md#accesslisteip2930valuesarray)*

___

###  serialize

▸ **serialize**(): *Buffer*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[serialize](_basetransaction_.basetransaction.md#abstract-serialize)*

*Defined in [eip2930Transaction.ts:273](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L273)*

Returns the serialized encoding of the transaction.

**Returns:** *Buffer*

___

###  sign

▸ **sign**(`privateKey`: Buffer): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[sign](_basetransaction_.basetransaction.md#sign)*

*Defined in [baseTransaction.ts:173](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L173)*

Signs a tx and returns a new signed tx object

**Parameters:**

Name | Type |
------ | ------ |
`privateKey` | Buffer |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)*

___

###  toCreationAddress

▸ **toCreationAddress**(): *boolean*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[toCreationAddress](_basetransaction_.basetransaction.md#tocreationaddress)*

*Defined in [baseTransaction.ts:117](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L117)*

If the tx's `to` is to the creation address

**Returns:** *boolean*

___

###  toJSON

▸ **toJSON**(): *[JsonTx](../interfaces/_index_.jsontx.md)*

*Overrides [BaseTransaction](_basetransaction_.basetransaction.md).[toJSON](_basetransaction_.basetransaction.md#abstract-tojson)*

*Defined in [eip2930Transaction.ts:365](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L365)*

Returns an object with the JSON representation of the transaction

**Returns:** *[JsonTx](../interfaces/_index_.jsontx.md)*

___

###  validate

▸ **validate**(): *boolean*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[validate](_basetransaction_.basetransaction.md#validate)*

*Defined in [baseTransaction.ts:65](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L65)*

Checks if the transaction has the minimum amount of gas required
(DataFee + TxFee + Creation Fee).

**Returns:** *boolean*

▸ **validate**(`stringError`: false): *boolean*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[validate](_basetransaction_.basetransaction.md#validate)*

*Defined in [baseTransaction.ts:66](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L66)*

**Parameters:**

Name | Type |
------ | ------ |
`stringError` | false |

**Returns:** *boolean*

▸ **validate**(`stringError`: true): *string[]*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[validate](_basetransaction_.basetransaction.md#validate)*

*Defined in [baseTransaction.ts:67](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L67)*

**Parameters:**

Name | Type |
------ | ------ |
`stringError` | true |

**Returns:** *string[]*

___

###  verifySignature

▸ **verifySignature**(): *boolean*

*Inherited from [BaseTransaction](_basetransaction_.basetransaction.md).[verifySignature](_basetransaction_.basetransaction.md#verifysignature)*

*Defined in [baseTransaction.ts:148](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/baseTransaction.ts#L148)*

Determines if the signature is valid

**Returns:** *boolean*

___

### `Static` fromRlpSerializedTx

▸ **fromRlpSerializedTx**(`serialized`: Buffer, `opts`: [TxOptions](../interfaces/_index_.txoptions.md)): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

*Defined in [eip2930Transaction.ts:96](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L96)*

Instantiate a transaction from the serialized tx.
(alias of `fromSerializedTx()`)

Note: This means that the Buffer should start with 0x01.

**`deprecated`** this constructor alias is deprecated and will be removed
in favor of the `fromSerializedTx()` constructor

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`serialized` | Buffer | - |
`opts` | [TxOptions](../interfaces/_index_.txoptions.md) | {} |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

___

### `Static` fromSerializedTx

▸ **fromSerializedTx**(`serialized`: Buffer, `opts`: [TxOptions](../interfaces/_index_.txoptions.md)): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

*Defined in [eip2930Transaction.ts:71](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L71)*

Instantiate a transaction from the serialized tx.

Note: this means that the Buffer should start with 0x01.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`serialized` | Buffer | - |
`opts` | [TxOptions](../interfaces/_index_.txoptions.md) | {} |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

___

### `Static` fromTxData

▸ **fromTxData**(`txData`: [AccessListEIP2930TxData](../interfaces/_index_.accesslisteip2930txdata.md), `opts`: [TxOptions](../interfaces/_index_.txoptions.md)): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

*Defined in [eip2930Transaction.ts:62](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L62)*

Instantiate a transaction from a data dictionary

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`txData` | [AccessListEIP2930TxData](../interfaces/_index_.accesslisteip2930txdata.md) | - |
`opts` | [TxOptions](../interfaces/_index_.txoptions.md) | {} |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

___

### `Static` fromValuesArray

▸ **fromValuesArray**(`values`: [AccessListEIP2930ValuesArray](../modules/_index_.md#accesslisteip2930valuesarray), `opts`: [TxOptions](../interfaces/_index_.txoptions.md)): *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*

*Defined in [eip2930Transaction.ts:106](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/eip2930Transaction.ts#L106)*

Create a transaction from a values array.

The format is:
chainId, nonce, gasPrice, gasLimit, to, value, data, access_list, yParity (v), senderR (r), senderS (s)

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`values` | [AccessListEIP2930ValuesArray](../modules/_index_.md#accesslisteip2930valuesarray) | - |
`opts` | [TxOptions](../interfaces/_index_.txoptions.md) | {} |

**Returns:** *[AccessListEIP2930Transaction](_eip2930transaction_.accesslisteip2930transaction.md)‹›*
