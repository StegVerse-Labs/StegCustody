# StegCustody

StegCustody is the reconstructable custody and responsibility record layer for the StegVerse ecosystem.

It records the current and historical relationship between an item or obligation and the parties that own, possess, operate, pay for, benefit from, control, transfer, license, or bear liability for it.

StegCustody began with physical-item custody. Its scope now includes physical, digital, financial, legal, intellectual-property, and operational assets where those roles may differ.

## Core distinction

Custody is not the same as ownership.

Payment is not the same as ownership.

Operation is not the same as authority.

Use is not the same as liability.

A single asset may therefore have different values for:

```text
legal owner
physical or logical custodian
operator
payer
beneficiary
authority holder
liability holder
intended transferee
```

StegCustody preserves those distinctions instead of collapsing them into one field.

## Relationship to Fin-Co and StegFinCo

```text
Fin-Co
= constitutional financial constraint layer

StegFinCo
= governed financial execution layer

StegCustody
= evidence and transition record for custody, control, ownership,
  payment, use, transfer, and liability
```

Fin-Co determines the constraints that financial systems must obey.

StegFinCo evaluates whether a proposed financial action may become effect-capable.

StegCustody records the actual present state, approved transition, evidence, and resulting custody state of the affected asset or obligation.

## Initial organizational-separation use case

StegCustody is the evidentiary layer for separating StegVerse commercial operations from personally funded or personally held assets.

Examples include:

- domains currently registered personally but intended for commercial operation;
- subscriptions currently paid from personal accounts;
- cloud services used by StegVerse projects;
- repositories and credentials operated for public or commercial purposes;
- equipment acquired personally but used by the ecosystem;
- expenses awaiting classification, reimbursement, contribution, transfer, or retention;
- contracts, licenses, and insurance policies assigned to a specific operating entity.

The repository records current truth first. It does not presume that an intended transfer has already occurred.

## Transition model

```text
discover
→ record current custody truth
→ classify intended role
→ authorize treatment
→ transfer, license, reimburse, contribute, or retain
→ append evidence
→ record resulting state
```

## Canonical status vocabulary

```text
PERSONAL_UNCLASSIFIED
PERSONAL_FOR_BUSINESS
PUBLIC_ENTITY
COMMERCIAL_ENTITY
SHARED_PENDING_REVIEW
TRANSFER_APPROVED
TRANSFER_IN_PROGRESS
TRANSFERRED
LICENSED_NOT_TRANSFERRED
REIMBURSEMENT_PENDING
RETAINED_PERSONALLY
```

## Canonical record fields

```text
record_id
item_type
item_name
current_legal_owner
current_custodian
current_operator
current_payer
current_beneficiary
current_authority_holder
current_liability_holder
intended_entity
custody_status
transition_method
effective_date
evidence_refs
review_required
notes
```

See `docs/FINCO_STEGCUSTODY_BOUNDARY.md` for the formal operational distinction and `schemas/custody-record.schema.json` for the initial machine-readable record shape.

## Safety and record handling

This repository may define schemas, classifications, and non-secret evidence references. It should not contain bank credentials, tax identifiers, private keys, passwords, full account numbers, or unredacted private legal records.

Sensitive originals belong in an access-controlled records system. StegCustody stores only the minimum references and hashes required to reconstruct custody and transition claims.
