# Hiero Contributor Identity Verification — POC

This is a proof-of-concept GitHub Action demonstrating automated
contributor identity verification on pull requests.

## What This Demonstrates
- Automatically triggers on every PR opened in this repository
- Checks contributor verification status against a registry
- Posts a detailed comment explaining verification result
- Sets a GitHub commit status check (green/red)

## How It Works
1. PR is opened → GitHub Action triggers
2. Action reads `verified-contributors.json` registry
3. Checks if PR author is verified
4. Posts automated comment + sets commit status

## Full Implementation
This POC uses a JSON file as the registry. The full implementation
(LFX Mentorship 2026) will replace this with:
- Hedera-anchored DIDs via `did:hedera`
- Verifiable Credentials issued by Heka Identity Service
- OID4VP verification sessions
- GitHub username → DID registry lookup

## Live Demo
Open any PR on this repository to see the verification in action.
