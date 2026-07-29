# Fin-Co / StegFinCo / StegCustody Boundary

## Purpose

This document prevents three distinct responsibilities from being collapsed into one system.

## Fin-Co

Fin-Co is the constitutional financial coherence specification.

It defines the constraints that any compatible financial system must obey. It does not hold assets, execute payments, maintain bank accounts, or act as the custody system for organizational records.

## StegFinCo

StegFinCo is the governed financial execution layer.

It evaluates proposed financial transitions against current authority, required evidence, applicable limits, and Fin-Co constraints. Its output is an admissibility result and execution receipt.

StegFinCo does not become the owner or custodian of an asset merely because it evaluates or authorizes a transition.

## StegCustody

StegCustody records the state of custody and responsibility before, during, and after a transition.

It distinguishes:

- legal ownership;
- custody or possession;
- operational control;
- payment source;
- beneficial use;
- authority;
- liability;
- intended transfer state;
- evidence supporting each claim.

## Organizational separation

The emerging StegVerse public and commercial roles require records that distinguish at least:

```text
public-purpose asset or obligation
commercial asset or obligation
personal asset used for StegVerse
shared or unresolved asset
```

StegCustody records the present state without prematurely declaring that a transfer, reimbursement, contribution, assignment, or license has occurred.

## Example

```json
{
  "record_id": "SC-EXAMPLE-001",
  "item_type": "domain",
  "item_name": "stegverse.com",
  "current_legal_owner": "personal",
  "current_operator": "StegVerse commercial operations",
  "current_payer": "personal account",
  "current_beneficiary": "commercial operations",
  "current_liability_holder": "pending legal review",
  "intended_entity": "commercial entity",
  "custody_status": "TRANSFER_APPROVED",
  "transition_method": "assignment",
  "evidence_refs": [],
  "review_required": true
}
```

This example does not prove a transfer. It proves that the current and intended states are being distinguished.

## Records and sensitive data

StegCustody should store hashes, redacted references, receipt identifiers, and classification records. It should not store:

- banking credentials;
- complete account or card numbers;
- tax identifiers;
- private keys;
- passwords;
- unredacted personal legal documents;
- confidential customer data.

## Decision chain

```text
StegCustody records current state
→ organizational governance defines intended treatment
→ StegFinCo evaluates any financial transition
→ authorized operator performs the external action
→ StegCustody records evidence and resulting state
```

No repository name or domain alone establishes a legal entity, ownership transfer, tax treatment, or liability separation. Those outcomes require the corresponding legal and operational acts.
