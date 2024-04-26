
# Creator X

Creator X is a blockchain project designed on the Stellar network to empower creators by issuing NFTs with embedded royalties. Utilizing the capabilities of the Soroban smart contract platform, Creator X aims to provide sustainable income for creators through royalties from secondary sales.

## Prerequisites

Before you begin, ensure you have the following installed:
- Rust (latest stable version)
- Cargo (Rust's package manager and build tool)
- Docker (for running local Stellar and Soroban environments)

## Installation

1. **Clone the Repository**

```bash
git clone https://github.com/yourusername/creatorx.git
cd creatorx
```

2. **Install Dependencies**

Navigate to your project directory and build the project:

```bash
cargo build
```

3. **Set up Local Stellar and Soroban Environments**

Using Docker, pull and run the Stellar quickstart image:

```bash
docker run --rm -it -p "8000:8000" -v "/path/to/your/data:/opt/stellar" --name stellar stellar/quickstart --testnet
```

In another terminal, initialize the Soroban local environment:

```bash
soroban env start
```

4. **Deploy Smart Contracts**

Compile and deploy your smart contracts to the local Soroban environment:

```bash
soroban deploy path/to/your/contract.wasm
```

Note the contract ID output from this command, as it will be used for front-end integration.

5. **Configure Environment Variables**

Create a `.env` file in the root directory and update it with necessary variables:

```
STELLAR_PUBLIC_NETWORK_URL=https://horizon-testnet.stellar.org
CONTRACT_ID=YourContractIDHere
```

6. **Run the Application**

To run the application, use the following command:

```bash
cargo run
```

This will start the application, allowing you to interact with your deployed smart contracts.

## Contributing

Contributions are welcome! Please feel free to submit pull requests, or open issues for bugs and feature requests.

## License

Distributed under the MIT License. See `LICENSE` for more information.
