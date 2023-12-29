# Contract Deployment Tool

This tool is a command line tool that allows you to deploy contracts to multiple chains determinitically with a single command. It uses the [ZeroDev](https://zerodev.app) service to deploy contracts.

## Configuration

1. Inside the `cli` directory, create a `.env` file and fill it out by refering to `.env.example.`
2. Run `pnpm install` to install all the necessary dependencies.
3. Run `pnpm build` to build the project.
4. Run `pnpm link --global` to make the command accessible globally.
5. Test the installation by running `zerodev -h`. If you see a guide for the command, it means the installation was successful.

## Available Commands

All commands should be prefixed with `zerodev`

- `-h`, `--help`: Show help
- `chains`: Show the list of available chains
- `compute-address <path-to-bytecode> <salt>`: Compute the address to be deployed
- `get-deployer-address`: Get the deployer's address
- `get-balance`: Get the deployer USDC balance
- `deploy [options] <path-to-bytecode> <salt>`: Deploy contracts deterministically using CREATE2, in order of the chains specified
- `create-session-key`: Create a session key authorized to deploy contracts
- `help [command]`: display help for command

## Supported Networks

This tool supports all network supported by ZeroDev. Check details [here](https://docs.zerodev.app/supported-networks)
