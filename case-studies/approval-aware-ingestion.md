# Approval-aware document ingestion

**Outcome** The documented pilot admitted individually approved documents to a candidate catalog, searched across them, and refused repeat admission of an existing item.

## Problem

A searchable catalog should be able to explain which version of a document it admitted and what decision authorized that version. A file can change after review, and a retry can otherwise create duplicate records.

## Design

The workflow separates selection, review, exact-version approval, admission, and retrieval. A content fingerprint binds approval to the reviewed bytes. Search validates the provenance chain and labels the result as candidate material. The closeout packet is an upstream review artifact, with its own [validation boundary](governed-artifact-closeout.md).

## Evidence and limits

The documented run showed two independently approved documents arriving in one candidate catalog. A search returned both, the historical parent receipt was checked, and a repeat admission was refused. This establishes an exercised controlled intake path at that scope. It leaves bulk backfill, recurring unattended intake, and production authority as separate work.
