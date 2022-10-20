ocaml-multicodec
----------------

This library provides OCaml values and types derived from the
[mutlicodec](https://github.com/multiformats/multicodec) definition.

```ocaml
# #require "multicodec";;
```

Multicodec is an agreed upon codec table, essentially providing a means to
encode some value as a number. For example, a number for hashes that are
generated with SHA256.

```ocaml
# Multicodec.multihash_to_code;;
- : Multicodec.multihash -> int = <fun>
# Multicodec.multihash_to_code `Sha2_256;;
- : int = 18
# Multicodec.multihash_of_code 18;;
- : Multicodec.multihash option = Some `Sha2_256
```

Other encoded values include common addressing schemes, such as DNS.

```ocaml
# Multicodec.multiaddr_to_code `Dns;;
- : int = 53
```

Find out more about multicodec at the [multiformats
websites](https://multiformats.io).
