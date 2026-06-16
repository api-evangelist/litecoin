# Litecoin (litecoin)

Litecoin is a peer-to-peer cryptocurrency network based on the Bitcoin protocol, offering faster block times (2.5 minutes) and lower transaction fees. It exposes a JSON-RPC interface via Litecoin Core for direct node interaction, a built-in unauthenticated REST interface for public blockchain queries, and a Litecoin Space block explorer REST and WebSocket API (mempool.space-compatible) for querying transactions, addresses, blocks, UTXO data, mempool state, and fee estimates.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/apis.yml)

## Tags

- Cryptocurrency
- Blockchain
- Litecoin
- LTC
- Payments
- Decentralized Finance
- Block Explorer
- JSON-RPC

## Timestamps

- **Created:** 2026-06-14
- **Modified:** 2026-06-14

## APIs

### Litecoin Core JSON-RPC API

The primary programmatic interface to a Litecoin Core node. Clients send HTTP POST requests with JSON-RPC 2.0 payloads to interact with the node. Methods cover blockchain state, block and transaction retrieval, mempool inspection, network peers, mining, UTXO queries, address validation, raw transaction construction and broadcast, and fee estimation. The daemon listens on port 9332 (mainnet), 19332 (testnet), and 19443 (regtest). Authentication is required via cookie file or rpcauth credentials.

- **Human URL:** [https://github.com/litecoin-project/litecoin/blob/master/doc/JSON-RPC-interface.md](https://github.com/litecoin-project/litecoin/blob/master/doc/JSON-RPC-interface.md)
- **Base URL:** `http://localhost:9332`

#### Tags

- JSON-RPC
- Blockchain
- Litecoin Core
- Node
- Transactions
- Blocks
- Mempool
- UTXO
- Mining

#### Properties

- [Documentation](https://github.com/litecoin-project/litecoin/blob/master/doc/JSON-RPC-interface.md)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/openapi/litecoin-core-json-rpc.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/plans/litecoin-core-json-rpc.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/rate-limits/litecoin-core-json-rpc.yml)
- [Fin Ops](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/finops/litecoin-core-json-rpc.yml)

### Litecoin Core REST API

An unauthenticated, read-only HTTP REST interface built into Litecoin Core and enabled with the -rest flag. Supports retrieval of transactions, full blocks, block headers, block hash by height, chain information, UTXO set queries (per BIP64), and mempool statistics and contents. Responses are available in binary, hex-encoded, or JSON format depending on the file extension (.bin, .hex, .json) appended to each path. Runs on the same port as JSON-RPC (default 9332 mainnet).

- **Human URL:** [https://github.com/litecoin-project/litecoin/blob/master/doc/REST-interface.md](https://github.com/litecoin-project/litecoin/blob/master/doc/REST-interface.md)
- **Base URL:** `http://localhost:9332`

#### Tags

- REST
- Blockchain
- Litecoin Core
- Transactions
- Blocks
- UTXO
- Mempool
- Read-Only

#### Properties

- [Documentation](https://github.com/litecoin-project/litecoin/blob/master/doc/REST-interface.md)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/openapi/litecoin-core-rest.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/plans/litecoin-core-rest.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/rate-limits/litecoin-core-rest.yml)
- [Fin Ops](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/finops/litecoin-core-rest.yml)

### Litecoin Space REST API

A public REST API provided by the Litecoin Space block explorer (litecoinspace.org), a mempool.space-compatible service for the Litecoin network. Endpoints cover addresses (details, transactions, UTXOs, validation), blocks (details, headers, height, raw data, transactions), transactions (details, hex, raw, Merkle proofs, output spend status, broadcast), mempool (statistics, transaction IDs, recent transactions), fee recommendations, mining pool statistics, and network hashrate and difficulty data. No authentication required for public endpoints.

- **Human URL:** [https://litecoinspace.org/docs/api/rest](https://litecoinspace.org/docs/api/rest)
- **Base URL:** `https://litecoinspace.org/api`

#### Tags

- REST
- Block Explorer
- Litecoin Space
- Transactions
- Blocks
- Addresses
- UTXO
- Mempool
- Fees
- Mining
- Public

#### Properties

- [Documentation](https://litecoinspace.org/docs/api/rest)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/openapi/litecoin-space-rest.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Plans](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/plans/litecoin-space-rest.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/rate-limits/litecoin-space-rest.yml)
- [Fin Ops](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/finops/litecoin-space-rest.yml)

### Litecoin Space WebSocket API

A real-time WebSocket API provided by Litecoin Space (litecoinspace.org) for subscribing to live Litecoin network events. Clients connect to the WebSocket endpoint and subscribe to channels including new blocks, mempool block projections, live 2-hour fee rate charts, and network stats. Address tracking is supported to receive push notifications for new mempool and block-confirmed transactions involving a specific address.

- **Human URL:** [https://litecoinspace.org/docs/api/websocket](https://litecoinspace.org/docs/api/websocket)
- **Base URL:** `wss://litecoinspace.org/api/v1/ws`

#### Tags

- WebSocket
- Block Explorer
- Litecoin Space
- Real-Time
- Blocks
- Mempool
- Address Tracking
- Fees

#### Properties

- [Documentation](https://litecoinspace.org/docs/api/websocket)
- [Plans](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/plans/litecoin-space-websocket.yml)
- [Rate Limits](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/rate-limits/litecoin-space-websocket.yml)
- [Fin Ops](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/finops/litecoin-space-websocket.yml)

## Common Properties

- [J S O N Ld](https://raw.githubusercontent.com/api-evangelist/litecoin/refs/heads/main/json-ld/litecoin.json) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Git Hub Org](https://github.com/litecoin-project)
- [Git Hub Org](https://github.com/litecoin-foundation)
- [Website](https://litecoin.org)
- [Blog](https://blog.litecoin.org)
- [Explorer](https://litecoinspace.org)
- [Source Code](https://github.com/litecoin-project/litecoin)
- [Changelog](https://github.com/litecoin-project/litecoin/releases)

## Maintainers

**FN:** API Evangelist
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
