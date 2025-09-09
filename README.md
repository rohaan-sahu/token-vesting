# token-vesting

This app was build by following projet8 from the video tutorial on Solana's youtube channel.
[Name: Solana Bootcamp 2024 - Project 1-9](https://youtu.be/amAq-WHAFs8?t=20896)

I have managed to use the following packages an make it work.
  "@coral-xyz/anchor": "^0.30.0",
  "anchor-bankrun": "^0.5.0",
  "solana-bankrun": "^0.4.0",
  "spl-token-bankrun": "^0.2.5",

CLI tooling version:
  - solana-cli 2.2.19 (src:74a35e19; feat:3073396398, client:Agave)
  - anchor-cli 0.31.1
  - cargo 1.88.0 (873a06493 2025-05-10)
  - node (v24.0.2)

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
