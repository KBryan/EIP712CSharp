# EIP712CSharp
EIP712 in C#

# EIP712 Ethereum Standard Overview

The code provided demonstrates the usage of the EIP712 (Ethereum Improvement Proposal 712) standard in the context of signing and verifying typed data on the Ethereum blockchain. The purpose of EIP712 is to provide a standardized way to define and sign structured data in a secure manner. This standard is particularly useful for applications that require message signing and verification, such as decentralized applications (dApps).

## Classes and Their Usage

### `EIP712` Class

This class contains the `Main` method, which serves as the entry point of the program. It demonstrates how to create and sign typed data using the EIP712 standard.

### `Account` Class

The `Account` class is part of the `Nethereum` library, which is used to manage Ethereum accounts. It takes a private key as a parameter and creates an account object. In the provided code, the private key is represented by the placeholder `ADD_PRIVATE_KEY`. It is important to replace this placeholder with an actual private key for the code to work correctly.

### `TypedData` Class

The `TypedData` class represents the structured data that will be signed using the EIP712 standard. It consists of the following properties:

- `Domain`: Represents the domain-specific metadata for the typed data, including the name, version, chain ID, and verifying contract address.
- `Types`: Defines the types and their respective members used in the structured data.
- `PrimaryType`: Specifies the primary type of the data structure. In this case, it is "Mail".
- `Message`: Contains the actual data to be signed, structured according to the defined types.

### `Domain` Class

The `Domain` class represents the domain-specific metadata for the typed data. It includes properties such as the name, version, chain ID, and verifying contract address. These properties help provide context and prevent cross-domain attacks.

### `MemberDescription` Class

The `MemberDescription` class represents a member (field or property) of a type. It defines the name and type of each member within the `Types` property of the `TypedData` class.

### `MemberValue` Class

The `MemberValue` class represents the value of a member within the `Message` property of the `TypedData` class. It includes the type name and the actual value.

### `Eip712TypedDataSigner` Class

The `Eip712TypedDataSigner` class is part of the `Nethereum.Signer.EIP712` namespace and provides the functionality to sign the typed data using the EIP712 standard. In the provided code, it is used to sign the `typedData` object with the private key of the `account` object.

### `EthECKey` Class

The `EthECKey` class is part of the `Nethereum.Signer` namespace and represents an Ethereum elliptic curve key. It is used to create an `EthECKey` object with the private key of the `account` object, which is then passed to the `SignTypedData` method of the `Eip712TypedDataSigner` class.

### `Signature` Class

The `Signature` class represents the parsed signature obtained from signing the typed data. It has three properties: `R`, `S`, and `V`, which correspond to the signature components.

### `ParseSignature` Method

The `ParseSignature` method takes the full signature string as input, extracts the signature components (`R`, `S`, and `V`), and returns a `Signature` object. It assumes that the signature string is in the format without the "0x" prefix. The method converts the components to the correct format before returning the `Signature` object.

##
