# Authenticated vs. Unauthenticated Vulnerability Assessment

## Windows & Linux | Tenable Vulnerability Management

## Project Overview

This project evaluates how authentication and credential privileges affect
vulnerability assessment visibility across Windows and Linux virtual machines
hosted in Microsoft Azure.

Using Tenable Vulnerability Management, I compared unauthenticated and
authenticated assessments to evaluate differences in host-level visibility,
credential validation, assessment coverage, and security findings.

The Linux assessment also evaluates how account privilege affects the depth
of credentialed vulnerability scanning.

## Technologies

- Tenable Vulnerability Management
- Microsoft Azure
- Windows Virtual Machine
- Ubuntu Linux Virtual Machine
- SSH
- Azure Network Security Groups (NSG)

## Assessment Scope

The project consists of two comparative assessments:

### Windows Assessment
- Unauthenticated vulnerability assessment
- Authenticated vulnerability assessment
- Credential-status validation
- Comparison of assessment visibility

### Linux Assessment
- Unauthenticated vulnerability assessment
- Authenticated assessment using standard-user credentials
- Authenticated assessment using elevated/root credentials
- Credential and privilege validation
- Comparison of assessment visibility

## Windows Assessment Results

| Assessment | Credential Status | Findings |
|---|---|---:|
| Unauthenticated | No credentials provided | 46 |
| Authenticated | Valid credentials provided | 79 |

Authenticated scanning identified 33 additional findings and provided
substantially greater host-level visibility than the unauthenticated
assessment.

Although valid credentials were confirmed, the authenticated assessment
also demonstrated that successful authentication does not necessarily
guarantee complete assessment coverage.

