# Litecoin (litecoin)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
