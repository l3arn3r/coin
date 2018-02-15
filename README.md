# coin

Transaction class that represents a ScroogeCoin transaction and has inner classes Transaction.Output and Transaction.Input.

A transaction output consists of a value and a public key to which it is being paid. For the public keys, we use the built-in Java PublicKey class.

A transaction input consists of the hash of the transaction that contains the corresponding output, the index of this output in that transaction (indices are simply integers starting from 0), and a digital signature. For the input to be valid, the signature it contains must be a valid signature over the current transaction with the public key in the spent output. More specifically, the raw data that is signed is obtained from the getRawDataToSign(int index) method.
