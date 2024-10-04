# OP_CHECKSIG
:::info
**Opcode number:** 172  
**Byte representation:** `0xac`   
**Short Description:**  Compares the top two items from the stack and pushes a 1 if the pubkey can be created from that signature else push a 0.
:::

:::danger
This page would like some review. If you'd like to contribute, take a look at the [source code for this website]!
:::

The [`OP_CHECKSIG`](./OP_CHECKSIG.md) opcode is used to verify that the signature for a tx input is valid when compared to its scriptPubKey. OP_CHECKSIG pops two items of the stack, first the pubKey and then the scriptSig.  

## Examples
### Example 1
```shell 
# ASM script
OP_1 OP_NOP10 OP_1 

# Raw script
51b851

# Final stack
1
1
```

### Example 2
```shell
# ASM script
OP_1 OP_1 OP_NOP10 OP_ADD

# Raw script
5151b893

# Final stack
2
```

[source code for this website]: https://github.com/thunderbiscuit/opcode-explained
