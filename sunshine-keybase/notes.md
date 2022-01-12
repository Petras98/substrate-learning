# Identity

## Client.rs

`identiy/client/src/client.rs`

API for a user/client
manages:

- identity
- claims
- accounts
- paper keys
- keys
- password

## Github.rs

`identiy/client/src/github.rs`

API to connect and search Github.

- `find_proofs`  
  provide username as parameter. Returns found proofs from the user's github/gists.
- `verify`  
  verifies the generated signature matches the found proof in the user's github.
- `proof`  
  populates the `github-proof-template.md` and returns the proof

## Service.rs

`identiy/client/src/service.rs`

Wrapper/Interface for specific services (right now just Github, we could extend to other services).
Has functions to create proof, verify proof, get what service is there, get the specific service's username, etc.

## Claim.rs

`identiy/client/src/claim.rs`

- `UnsignedClaim`, and `Claim` (Signed Claim)
- `UnsignedClaim`'s have an expiration until signed

## Subxt.rs

`identiy/client/src/subxt.rs`  
Subxt = Submit Extrinsics  
https://github.com/paritytech/subxt

# Faucet

What is a "Faucet":
https://medium.com/geekculture/
what-are-crypto-faucets-how-to-earn-some-crypto-for-free-79ef7cbca225
