# BlockSign E-Sign — Revised Milestone 2 Proof of Delivery

## Reviewer access and important product boundaries

BlockSign E-Sign is available under the BlockSign and former Docufi3d branding. `blocksign.io` and `docufi3d.com` refer to the same continuously developed product. The project and company history is:

> IAMX AG (project initiator) → Docufi3d UG (haftungsbeschränkt) → BlockSign GmbH

Interactive functions require a free user account. Public information pages and public demonstration videos do not require login.

Reviewers can test paid functions without making a real payment by using reviewer voucher codes supplied with the review instructions. Voucher redemption follows the same checkout and entitlement process as a verified payment. Vouchers are single-use and restricted to their configured purpose (FES, QES, document payment, or all supported purposes).

### Important distinction between payment, onboarding and signing

Payment or voucher redemption grants the account-specific entitlement to start the selected FES or QES process. It does **not** itself create a regulated identity or signature.

Swisscom Trust Services performs the provider-side identity, credential and cryptographic signature process. The Swisscom onboarding is started from an actual signature request for a document. It is therefore expected that, immediately after payment, the profile can show:

> Paid — onboarding pending

The user then signs a document configured for the purchased signature level and legal framework. The matching Swisscom onboarding begins in that signing process.

FES and QES are available through separate Swisscom-backed paths for:

- **eIDAS**, using the supported EU identity-document path; and
- **ZertES**, using the supported Swiss identity-document path.

Entitlements and provider evidence are kept separate by legal framework. An eIDAS identity or entitlement does not automatically grant ZertES capability, and vice versa.

### Important distinction concerning biometrics

BlockSign biometrics is an optional **second authentication factor (2FA/MFA)** for account and signature authorisation. It is not described as the identity-proofing provider and does not independently create FES or QES status.

Regulated FES/QES onboarding and identity evidence are provided through Swisscom Trust Services. A biometric factor, verified phone number, legacy KYC flag, payment or voucher does not replace the required matching Swisscom evidence.

---

# A. Product Development

## Output 1 — Know Your Customer process implemented

The regulated identity and onboarding process for personal FES and QES is integrated with the qualified trust service provider Swisscom Trust Services.

The implementation supports provider onboarding for both configured legal frameworks:

- eIDAS FES and QES for the supported EU identity-document path;
- ZertES FES and QES for the supported Swiss identity-document path.

The process is initiated when the user signs a document configured for the corresponding signature level and legal framework. BlockSign creates and correlates the signing context; Swisscom performs the provider-side onboarding, identity and credential process. Successful provider evidence is stored separately for the applicable legal framework and signature level.

Biometrics in BlockSign is available as an optional second authentication factor. It strengthens account or signature authorisation but is not presented as a substitute for Swisscom identity proofing.

**Functional evidence**

1. Sign in to a reviewer account.
2. Open `https://blocksign.io/profile#workflows`.
3. Review the separate eIDAS and ZertES FES/QES readiness cards.
4. If necessary, authorise the selected level through checkout using the supplied reviewer voucher.
5. Upload a non-sensitive test PDF and create a signature request using the authorised legal framework and signature level.
6. Open the request as the signer and start signing.
7. Observe that Swisscom onboarding/authorisation begins inside the signature process.

**Evidence links**

- https://blocksign.io/profile#workflows — account and legal-framework-specific readiness; login required
- https://blocksign.io/videos/BlockSign-QES-Biometrics.mp4 — public product demonstration

The video demonstrates a product flow. Where its terminology differs from this revised PoD, the boundary above controls: Swisscom provides regulated identity evidence; BlockSign biometrics is a second authentication factor.

## Output 2 — Qualified Electronic Signature feature implemented

BlockSign implements document signing at AES, FES and QES levels. Personal FES and QES use the integrated Swisscom Trust Services process.

The currently implemented provider combinations are:

| Legal framework | FES | QES |
|---|---:|---:|
| eIDAS | Implemented through Swisscom onboarding/signing | Implemented through Swisscom onboarding/signing |
| ZertES | Implemented through Swisscom onboarding/signing | Implemented through Swisscom onboarding/signing |

The user first receives or creates a concrete document signature request. When the request requires FES or QES, BlockSign verifies access, payment entitlement, selected legal framework and available provider evidence. If matching evidence is not yet available, the signing action starts the corresponding Swisscom onboarding. The user then completes the provider interaction and the document-signing process.

Payment is not proof of identity and does not itself produce a signature. The purchased entitlement remains available until it can be used for the matching provider-backed workflow.

**Functional evidence**

1. Upload a non-sensitive PDF.
2. Add the reviewer account as a signer.
3. Select eIDAS or ZertES and FES or QES.
4. Complete checkout with a reviewer voucher if the account has no matching entitlement.
5. Open the invitation/signature request as the signer.
6. Start signing and complete the Swisscom flow.
7. Download the resulting signed PDF.

**Evidence links**

- https://blocksign.io/profile — legal-framework readiness and paid entitlements; login required
- https://blocksign.io/videos/Sign-AES.mp4 — public AES workflow demonstration
- https://blocksign.io/videos/Sign-QES-Biometrics-Available.mp4 — public QES workflow demonstration
- https://blocksign.io/videos/Login-AES-QES-Verification.mp4 — public signing and verification demonstration

## Output 3 — Signature verification feature implemented

At `https://blocksign.io/verification_upload`, an authenticated user can upload a signed PDF for verification. Verification is not restricted to documents created by BlockSign.

The verification workflow evaluates the evidence available in the uploaded PDF, including embedded signatures, document integrity and signer/certificate information. Provider-independent integrity evidence remains usable even when optional external evidence is unavailable.

**Evidence links**

- https://blocksign.io/verification_upload — login required
- https://blocksign.io/videos/Login-AES-QES-Verification.mp4 — public demonstration
  - approximately 01:43–01:53: AES verification in PDF-XChange Editor
  - approximately 03:05–03:15: QES verification in PDF-XChange Editor

## Output 4 — User-friendly access points integrated

The profile provides a central self-service overview of:

- FES/QES readiness separated into eIDAS and ZertES;
- available paid upgrades;
- completed payment entitlements;
- missing or active Swisscom provider evidence;
- the explanation that provider onboarding begins in a matching document-signing process;
- phone verification where required; and
- optional biometric 2FA/MFA.

The checkout supports verified payment methods and single-use voucher redemption. Voucher scope is enforced:

- an FES upgrade accepts an `fes` or `all` voucher;
- a QES upgrade accepts a `qes` or `all` voucher;
- a document-only voucher cannot be used for an account FES/QES upgrade.

This gives reviewers a usable route through the same entitlement logic without requiring a real payment.

**Evidence**

- https://blocksign.io/profile — login required
- checkout reached from the relevant eIDAS/ZertES FES/QES card

## Output 5 — Access to legal and regulatory requirements

The public compliance page explains the legal and regulatory context, including eIDAS, GDPR, ISO 27001, electronic-signature levels and relevant German/EU requirements.

The product does not claim that choosing a signature level automatically satisfies every statutory form requirement. The suitability of AES, FES or QES depends on the document, applicable law and required form.

**Evidence**

- https://blocksign.io/co
- https://blocksign.io/trust-center

## Output 6 — Free reviewer trial access

Review access is implemented through scoped, single-use voucher codes used in the normal checkout. This allows reviewers to test document payments and the configured FES/QES entitlement paths without making a real payment.

The reviewer voucher does not bypass product security or provider requirements. It settles only the permitted checkout scope. Swisscom onboarding and identity evidence remain necessary when the reviewer starts the corresponding FES/QES document-signing process.

Public pricing information remains available at:

- https://blocksign.io/pricing

Reviewer voucher codes and login details should be delivered privately with the submission and must not be published in the PoD.

## Output 7 — ISO 27001 certification

BlockSign GmbH operates an ISO 27001:2022-certified information security management system. The public trust centre provides the certificate information and independent verification route.

**Evidence**

- https://blocksign.io/trust-center

---

# B. Marketing and Visibility

## Output 8 — Public video presentation

Public product videos demonstrate the document, signing, identity and verification workflows:

- https://blocksign.io/videos/BlockSign-QES-Biometrics.mp4
- https://blocksign.io/videos/Demo.mp4
- https://blocksign.io/videos/Sign-AES.mp4
- https://blocksign.io/videos/Sign-QES-Biometrics-Available.mp4
- https://blocksign.io/videos/Login-AES-QES-Verification.mp4

These videos are supporting demonstrations. Reviewers can verify the current implementation directly through the functional steps in Outputs 1–4.

## Output 9 — Publications, press releases and case studies

- Digital identity and qualified signatures:  
  https://www.linkedin.com/pulse/digital-identity-qualified-signatures-why-compliance-matters-1qste
- Milestone progress:  
  https://www.linkedin.com/pulse/docufi3d-achieves-first-project-catalyst-milestone-prepares-okize/?published=t
- BlockSign product post:  
  https://x.com/BlockSign_io/status/2041852509489152453
- Docufi3d milestone post:  
  https://x.com/docufi3d/status/1973396841816273282
- Swisscom Trust Services post:  
  https://www.linkedin.com/posts/swisscom-trust-services_digitaltrust-electronicsignature-qualifiedelectronicsignature-activity-7382314553600008193-GpWK
- Public product demonstration:  
  https://blocksign.io/videos/Demo.mp4

---

# C. Case Studies and Client Pilots

## Output 10 — Collaboration with Hausakte24

The public Hausakte24 communication documents the pilot collaboration and launch of the digital solution.

**Evidence**

- https://www.linkedin.com/posts/hausakte24_meilenstein-erreicht-ab-anfang-2026-digitale-activity-7406633316189327360-u3c8

## Output 11 — Swisscom and Docufi3d/BlockSign presentation

The public product demonstration shows the branded end-to-end signing context and the integration of BlockSign/Docufi3d with Swisscom Trust Services.

**Evidence**

- https://blocksign.io/videos/Demo.mp4
- https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services

The Swisscom partner listing uses the former Docufi3d/IAMX name. The project-history statement at the beginning of this PoD explains the continuous project and company succession.

## Output 12 — Presentation at a qualified industry event

The integration was presented in connection with Swisscom Trust Up 2025:

- Event: Swisscom Trust Up 2025
- Venue: Prime Tower / Clouds Bar, Maagplatz 5, 8005 Zurich
- Date: 29 September 2025

**Evidence**

- Swisscom partner listing:  
  https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services
- Event communication:  
  https://x.com/BlockSign_io/status/1978768209219084707
- Swisscom event video:  
  https://www.youtube.com/watch?v=OSNYPxfguE4
- LinkedIn communication:  
  https://www.linkedin.com/posts/digitalidentity-blockchaincompliance-qes-share-7350803243607724034-KC2T/

---

# Supplementary technical reference — not required to verify this PoD

The following document describes the current product architecture, trust boundaries, legal-framework separation, paid onboarding model, document workflow, Swisscom integration, storage, evidence and security controls:

**BlockSign E-Sign — Technical Product Description V1.0**  
https://github.com/Docufi3d/Fund-13/blob/main/M2/BlockSign%20ESign%20%E2%80%94%20Technical%20Product%20Description%20V1.0.pdf

This document is supplied only as a supporting technical reference. Reviewers do **not** need to read it in order to execute or verify the milestone outputs. The live application steps, public evidence links and reviewer voucher access described above form the Proof of Delivery.

---

# Recommended private reviewer instructions

The following information should accompany the submission privately and should not be included in the public PoD:

1. reviewer account or account-creation instructions;
2. one or more valid, unused voucher codes with their scope clearly labelled;
3. a non-sensitive sample PDF;
4. the exact test combination to use, for example `ZertES / FES`;
5. a note that payment completion is followed by “Paid — onboarding pending” until the reviewer starts the matching signature request;
6. any Swisscom test-environment limitations or supported identity-document requirements; and
7. a contact route for resetting a consumed reviewer voucher.
