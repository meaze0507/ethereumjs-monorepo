[@ethereumjs/tx](../README.md) › ["index"](_index_.md)

# Module: "index"

## Index

### Classes

* [AccessListEIP2930Transaction](../classes/_index_.accesslisteip2930transaction.md)
* [Transaction](../classes/_index_.transaction.md)
* [TransactionFactory](../classes/_index_.transactionfactory.md)

### Interfaces

* [AccessListEIP2930TxData](../interfaces/_index_.accesslisteip2930txdata.md)
* [JsonTx](../interfaces/_index_.jsontx.md)
* [TxOptions](../interfaces/_index_.txoptions.md)

### Type aliases

* [AccessList](_index_.md#accesslist)
* [AccessListBuffer](_index_.md#accesslistbuffer)
* [AccessListBufferItem](_index_.md#accesslistbufferitem)
* [AccessListEIP2930ValuesArray](_index_.md#accesslisteip2930valuesarray)
* [AccessListItem](_index_.md#accesslistitem)
* [TxData](_index_.md#txdata)
* [TypedTransaction](_index_.md#typedtransaction)

### Variables

* [N_DIV_2](_index_.md#const-n_div_2)

### Functions

* [isAccessList](_index_.md#isaccesslist)
* [isAccessListBuffer](_index_.md#isaccesslistbuffer)

## Type aliases

###  AccessList

Ƭ **AccessList**: *[AccessListItem](_index_.md#accesslistitem)[]*

*Defined in [types.ts:48](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L48)*

___

###  AccessListBuffer

Ƭ **AccessListBuffer**: *[AccessListBufferItem](_index_.md#accesslistbufferitem)[]*

*Defined in [types.ts:47](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L47)*

___

###  AccessListBufferItem

Ƭ **AccessListBufferItem**: *[Buffer, Buffer[]]*

*Defined in [types.ts:46](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L46)*

___

###  AccessListEIP2930ValuesArray

Ƭ **AccessListEIP2930ValuesArray**: *[Buffer, Buffer, Buffer, Buffer, Buffer, Buffer, Buffer, [AccessListBuffer](_index_.md#accesslistbuffer), undefined | Buffer‹›, undefined | Buffer‹›, undefined | Buffer‹›]*

*Defined in [types.ts:140](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L140)*

Buffer values array for EIP2930 transaction

___

###  AccessListItem

Ƭ **AccessListItem**: *object*

*Defined in [types.ts:38](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L38)*

#### Type declaration:

* **address**: *PrefixedHexString*

* **storageKeys**: *PrefixedHexString[]*

___

###  TxData

Ƭ **TxData**: *object*

*Defined in [types.ts:69](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L69)*

#### Type declaration:

* **data**? : *BufferLike*

* **gasLimit**? : *BNLike*

* **gasPrice**? : *BNLike*

* **nonce**? : *BNLike*

* **r**? : *BNLike*

* **s**? : *BNLike*

* **to**? : *AddressLike*

* **v**? : *BNLike*

* **value**? : *BNLike*

___

###  TypedTransaction

Ƭ **TypedTransaction**: *[Transaction](../classes/_index_.transaction.md) | [AccessListEIP2930Transaction](../classes/_eip2930transaction_.accesslisteip2930transaction.md)*

*Defined in [types.ts:67](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L67)*

## Variables

### `Const` N_DIV_2

• **N_DIV_2**: *BN‹›* = new BN(
  '7fffffffffffffffffffffffffffffff5d576e7357a4501ddfe92f46681b20a0',
  16
)

*Defined in [types.ts:177](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L177)*

A const defining secp256k1n/2

## Functions

###  isAccessList

▸ **isAccessList**(`input`: [AccessListBuffer](_index_.md#accesslistbuffer) | [AccessList](_index_.md#accesslist)): *input is AccessList*

*Defined in [types.ts:63](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L63)*

**Parameters:**

Name | Type |
------ | ------ |
`input` | [AccessListBuffer](_index_.md#accesslistbuffer) &#124; [AccessList](_index_.md#accesslist) |

**Returns:** *input is AccessList*

___

###  isAccessListBuffer

▸ **isAccessListBuffer**(`input`: [AccessListBuffer](_index_.md#accesslistbuffer) | [AccessList](_index_.md#accesslist)): *input is AccessListBuffer*

*Defined in [types.ts:50](https://github.com/ethereumjs/ethereumjs-monorepo/blob/master/packages/tx/src/types.ts#L50)*

**Parameters:**

Name | Type |
------ | ------ |
`input` | [AccessListBuffer](_index_.md#accesslistbuffer) &#124; [AccessList](_index_.md#accesslist) |

**Returns:** *input is AccessListBuffer*
