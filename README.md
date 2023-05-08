![Ethereum Waffle](https://raw.githubusercontent.com/EthWorks/Waffle/master/docs/source/logo.png)

This is a fork of [@ethereum-waffle/compiler](https://github.com/TrueFiEng/Waffle), but without typechain.

# waffle-compiler

Compile solidity without the hassle.

## Installation

```
npm i github:DeepDoge/waffle-compiler#1.0.0 -D
```

### Compilation

This package exposes programmatic api for compiling solidity smart contracts.

Examples:

```ts
// Compilation with a config file
import { compileProject } from "waffle-compiler"

main()
async function main() {
	await compileProject("path/to/waffle.json")
}
```

```ts
// Compilation with js config
import { compileAndSave, compile } from "waffle-compiler"

main()
async function main() {
	const config = { sourceDirectory: "contracts", nodeModulesDirectory: "node_modules" }

	// compile and save the output
	await compileAndSave(config)

	// just compile
	const output = await compile(config)
	console.log(output)
}
```

### Linking

Example:

```ts
import { link } from ("waffle-compiler");
```
