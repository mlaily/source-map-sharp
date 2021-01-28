# Source Map Sharp

![Tests status](https://github.com/delneg/source-map-sharp/workflows/source-map-sharp-action/badge.svg?branch=master)
## About

This is a direct rewrite (meaning, the goal was not to write 'idiomatic' F# code, but to resemble inital JS code as close as possible) of source map generation tool https://github.com/mozilla/source-map

Which is originally written in JS. The initial purpose is to use it with https://github.com/fable-compiler/Fable project

See https://github.com/fable-compiler/Fable/issues/2166 - "Bring back source map support"

UPD: The issue above was closed, and this project is now being used by Fable to generated Source Maps. Hooray!


P.S. If you're a user that needs netstandard2.0 (as opposed to current netstandard2.1), please file an issue.

### Files - status

Legend:

😊 - Everything fine

🤨 - Everything fine except minor details (or not important right now details)

😴 - Not needed / won't do

😨 - Should be done, but isn't

🤯 - Done but no tested

1. 😊 `ArraySet` - Done & tested
2. 😊 `Base64` - Done & tested
3. 😊 `Base64-vlq` - Done & tested
4. 😴 `binary-search` - Not done, probably won't need
5. 🤨 `mapping-list` - Done, not tested specifically, coverage shows 95% via other tessts
6. 😴 `mapping.wasm` - Not done, probably won't need
7. 😴 `read-wasm-browser` - Not done, probably won't need
8. 😴 `read-wasm` - Not done, probably won't need
9. 😨 `source-map-consumer` - Not done, Don't know if will need it or not at the moment
10. 😊 `source-map-generator` - Done except the `consumer` parts, tested except `consumer` parts
11. 😊 `source-node` - Done except the `consumer` parts, tested except `consumer` parts
12. 😴 `url-browser` - Not done, probably won't need
13. 😴 `url` - Not done, probably won't need
14. 🤨 `util` - Done partially, what's needed
15. 😴 `wasm` - Not done, probably won't need

#### "SourceMapConsumer"-related stuff

Not done at the moment: 

1. SourceNode `fromStringWithSourceMap` function
2. SourceMapGenerator `fromSourceMap` function
3. SourceMapConsumer module
4. SourceMapNode, SourceMapGenerator - `consumer`-related tests
5. Article by the author of WASM - https://hacks.mozilla.org/2018/01/oxidizing-source-maps-with-rust-and-webassembly/

### Help needed

1. Source map consumer
2. Documentation & usage examples
3. Decisions on WASM stuff - Rust repo https://github.com/fitzgen/source-map-mappings
