# Project 02 – Healthcare Conditional Access Baseline

## Executive Summary

This project documents a healthcare-focused Conditional Access baseline in Microsoft Entra ID.

The goal is to demonstrate how Conditional Access can reduce identity risk while preserving emergency access and healthcare operational continuity.

## Business Scenario

Front Range Health Partners requires Conditional Access policies to protect workforce identities, privileged administrators, and Azure management access.

The environment must support:

- MFA enforcement
- Break Glass account exclusions
- Trusted hospital network locations
- Legacy authentication blocking
- Report-only testing before enforcement

## Policies Included

| Policy | Purpose | Mode |
|---|---|---|
| CA-001 – Require MFA for Admins | Protect privileged accounts | Report-only |
| CA-002 – Require MFA for All Users | Protect workforce users | Report-only |
| CA-003 – Block Legacy Authentication | Prevent insecure authentication | Report-only |
| CA-004 – Require MFA for Azure Management | Protect admin portals | Report-only |
| CA-005 – Require MFA Outside Trusted Locations | Protect external access | Report-only |