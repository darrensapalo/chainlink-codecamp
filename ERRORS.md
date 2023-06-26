# Errors

## Source file requires different compiler version

Sometimes you might encounter this error while compiling your solidity code.

`ParserError: Source file requires different compiler version (current compiler is 0.8.7+commit.e28d00a7.Emscripten.clang)`

Fix:

> An easy solution is to change your code to require v0.6 as well and compile with this version.
> 
> pragma solidity ^0.6.0;
> 
> [Source](https://stackoverflow.com/questions/70905645/parsererror-source-file-requires-different-compiler-version-current-compiler-i)