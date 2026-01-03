
# tx-router (Stateless Transaction Relay)

The tx-router is a stateless middleware service used to broadcast
pre-signed transactions to BNB Smart Chain.

## Purpose

End-user devices should not be required to manage RPC credentials
or maintain direct blockchain connectivity. The tx-router provides
a simple broadcast endpoint that accepts signed transaction payloads
and submits them to the network.

## Security Model

- No private keys are accepted or stored
- Transactions must be fully signed client-side
- The router does not modify transaction payloads
- No custody or authorization logic exists server-side

## Design Goals

- Stateless request handling
- Replaceable RPC backends
- Rate limiting and abuse protection
