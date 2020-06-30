# base91-deno
more space efficient encoding than base64

[![Deno CI](https://github.com/oplik0/base91-deno/workflows/Deno%20CI/badge.svg)](https://github.com/oplik0/base91-deno/actions)

## Getting started

Encoding:

```ts
import { encode } from "https://raw.githubusercontent.com/oplik0/base91-deno/master/base91.ts";
const encoder = new TextEncoder(); //converts utf-8 string to Uint8Array
const input = encoder.encode("test"); //Uint8Array(4) [ 116, 101, 115, 116 ] 
const result = encode(input); //"fPNKd"
```

Decoding:
```ts
import { decode } from "https://raw.githubusercontent.com/oplik0/base91-deno/master/base91.ts";
const decoder = new TextDecoder("utf-8"); //used to convert Uint8Array to utf-8 string
const result = decode("fPNKd"); //Uint8Array(4) [ 116, 101, 115, 116 ]
const output = decoder.decode(result); //"test"
```

## Development

Run tests:

```bash
deno test
```