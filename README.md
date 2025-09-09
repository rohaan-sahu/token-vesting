# token-vesting

This is a Next.js app containing:

- Tailwind CSS setup for styling
- Useful wallet UI elements setup using [@solana/web3.js](https://www.npmjs.com/package/@solana/web3.js)

## Getting Started

### Installation

#### Download the template

```shell
npx create solana-dapp@latest -t gh:solana-foundation/templates/web3js/token-vesting
```

#### Install Dependencies

```shell
npm install
```

## Apps

### anchor

This is a Solana program written in Rust using the Anchor framework.

#### Commands

#### Sync the program id:

Running this command will create a new keypair in the `anchor/target/deploy` directory and save the address to the
Anchor config file and update the `declare_id!` macro in the `./src/lib.rs` file of the program.

You will manually need to update the constant in `anchor/lib/counter-exports.ts` to match the new program id.

```shell
npm anchor keys sync
```

#### Build the program:

```shell
npm anchor-build
```

#### Start the test validator on a different terminal. Make sure 'solana-test-validator' is installed':

```shell
solana-test-validator
```

#### Run the tests

```shell
npm anchor-test
```

#### Deploy to Devnet

```shell
npm anchor deploy --provider.cluster devnet
```

### web

This is a React app that uses the Anchor generated client to interact with the Solana program.

#### Commands

Start the web app

```shell
npm run dev
```

Build the web app

```shell
pnpm build
```
