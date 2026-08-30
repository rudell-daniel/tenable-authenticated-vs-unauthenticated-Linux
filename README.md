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

## Linux Assessment Results

| Assessment | Credential Status | Findings |
|---|---|---:|
| Unauthenticated | No credentials provided | 22 |
| Authenticated - Standard User | Valid credentials / insufficient privilege | 57 |
| Authenticated - Root | Valid credentials / no credential issues | 61 |

The unauthenticated assessment identified 22 findings and reported that
OS security patch assessment was not available.

Valid standard-user credentials increased visibility to 57 findings and
made OS security patch assessment available. However, Tenable identified
insufficient privileges and reported that some SSH commands required
privilege escalation.

Using root credentials increased visibility to 61 findings and eliminated
the credential privilege issue.

## Key Findings

### Authentication Increased Assessment Visibility

Both Windows and Linux authenticated assessments produced substantially
greater host-level visibility than their unauthenticated counterparts.

### Valid Credentials Do Not Guarantee Complete Coverage

The assessments demonstrated that successful authentication should be
validated separately from assessment completeness.

### Linux Privilege Level Affected Assessment Depth

The standard Linux account successfully authenticated, but Tenable reported
insufficient privileges for some assessment operations. Root-level
authentication eliminated the credential privilege issue and provided
additional host-level information.

### Credential Validation Is Critical

Credential status plugins were reviewed to verify whether authentication
succeeded before interpreting the results as authenticated assessments.

## Linux Assessment Evidence

### Unauthenticated Assessment

![Linux unauthenticated assessment](linux/screenshots/01-unauthenticated-results.png)

### Standard-User Authenticated Assessment

![Linux standard-user authenticated assessment](linux/screenshots/02-standard-user-authenticated-results.png)

### Standard-User Credential Validation

![Linux insufficient privilege validation](linux/screenshots/03-standard-user-credential-validation.png)

### Root Authenticated Assessment

![Linux root authenticated assessment](linux/screenshots/04-root-authenticated-results.png)

### Root Credential Validation

![Linux root credential validation](linux/screenshots/05-root-credential-validation.png)

## Skills Demonstrated

- Tenable Vulnerability Management
- Vulnerability Assessment
- Authenticated Vulnerability Scanning
- Credential Validation
- Vulnerability Analysis
- Assessment Coverage Analysis
- Linux Privilege Analysis
- Windows and Linux Security
- Microsoft Azure
- Azure Virtual Machines
- Network Security Groups
- SSH
