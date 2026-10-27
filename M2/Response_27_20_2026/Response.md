# BlockSign — Fund 13, Milestone 2
## Consolidated Response and Evidence of Delivery

**Milestone:** QES and Biometric KYC Integration with Swisscom + Case Study #1  
**Project:** Docufi3d / BlockSign  
**Submission date:** October 27, 2026  
**Purpose:** Consolidated evidence submission and response to the latest milestone review

---

## 1. Executive Summary

Dear Catalyst Milestone Reviewers,

We are submitting this consolidated response to provide a complete, structured overview of the implementation and supporting evidence for all twelve outputs of Milestone 2.

The primary technical objective of the milestone — integration of regulated identity onboarding and qualified electronic signatures through Swisscom Trust Services — has been implemented and successfully exercised during independent reviewer testing.

In the previous review, the reviewer explicitly acknowledged:

> "We successfully completed KYC and executed the QES document signing using the Swisscom integration."

Other Milestone Reviewers have also approved the milestone after examining the implementation, demonstration materials, compliance documentation, and available testing evidence.

We acknowledge that the most recent rejection raised additional concerns regarding signature validation, outdated demonstration videos, usability documentation, and public co-marketing evidence.

To address these concerns, we have assembled an expanded evidence package containing:

- Public demonstrations of biometric MFA, qualified electronic signing, and the Hausakte24 integration.
- The original July–August 2025 process report.
- A dedicated usability study evaluation.
- Twenty-five completed user questionnaires.
- Signature and verification screenshots.
- An original test document and its electronically signed counterpart.
- A European Commission DSS v6.5.1 validation report showing **QESig / TOTAL_PASSED**.
- A publicly accessible Cardano blockchain transaction reference.
- A newly published marketing video featuring BlockSign, Cardano, and Swisscom branding.

The evidence is presented below according to the original twelve milestone outputs.

### Product and company continuity

The product was originally developed and presented under the IAMX and Docufi3d branding and is now operated as BlockSign.

Project development history:

**IAMX AG → Docufi3d UG (haftungsbeschränkt) → BlockSign GmbH**

Historical materials remain part of the project evidence and are identified as such. They are not presented as recordings of the current production implementation.

The current platform is available at:

https://blocksign.io/

---

# A. Product Development

## Output 1 — Biometric KYC and Identity Onboarding

**Requirement:** Implement a process through which users can complete identity verification and access regulated electronic signing.

### Implementation

BlockSign integrates with Swisscom Trust Services for provider-managed identity onboarding and regulated FES/QES signing.

The implementation supports distinct signing paths for:

- eIDAS, using supported European identity documents.
- ZertES, using supported Swiss identity documents.

Swisscom performs the regulated provider-side identity, credential, and signing processes.

BlockSign manages the document workflow, selects the requested signature level and legal framework, maintains the corresponding account entitlement, and initiates the appropriate Swisscom process.

Identity onboarding is initiated from a concrete signing request when suitable provider evidence is not already available.

BlockSign also provides optional biometric multi-factor authentication to strengthen account access and signing authorisation.

**Important distinction:** BlockSign biometric MFA is not a replacement for Swisscom identity proofing. Historical materials showing earlier biometric workflows are provided as implementation-history evidence.

### Evidence

**Current application**

https://blocksign.io/profile#workflows

**Public historical biometric demonstration**

BlockSign Biometric MFA Enrolment:

https://www.youtube.com/watch?v=cU3MLJUoPNY

**Additional product demonstration**

https://blocksign.io/videos/BlockSign-QES-Biometrics.mp4

### Reviewer verification

1. Sign in to BlockSign.
2. Navigate to the profile's signing workflows.
3. Select the relevant eIDAS or ZertES signature capability.
4. Use an available reviewer voucher when an entitlement is required.
5. Create a document-signing request.
6. Start the signing process.
7. Complete the required Swisscom provider onboarding.

**Evidence status:** The current Swisscom-backed onboarding flow was successfully exercised by a milestone reviewer. Historical biometric videos provide additional supporting context.

---

## Output 2 — Qualified Electronic Signature Implementation

**Requirement:** Enable users to sign documents using qualified electronic signatures in accordance with the applicable regulatory framework.

### Implementation

BlockSign supports three electronic signature levels:

- AES — platform-supported electronic signing.
- FES — advanced electronic signing using the configured Swisscom provider process.
- QES — qualified electronic signing through Swisscom Trust Services.

Personal FES and QES are implemented for the supported eIDAS and ZertES paths.

The signing process includes document preparation, signer assignment, entitlement verification, provider onboarding where necessary, execution of the signature, and delivery of the resulting PDF.

### Evidence package: October 26, 2026

An end-to-end demonstration was performed using the following supplied files:

**Original document:** [TestDocument.pdf](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument.pdf)

**Signed document:** [TestDocument_Signed.pdf](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument_Signed.pdf)

**European Commission validation report:** [DSS-Simple-report.pdf](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/DSS-Simple-report%20.pdf)

The document identifies the signing demonstration as:

**BS-QES-DEMO-2026-001**

The demonstration combines BlockSign's document workflow with Swisscom electronic signing and Cardano audit evidence.

### Independent signature validation

The supplied European Commission DSS v6.5.1 report contains the following results:

| Property | Result |
|---|---|
| Signature | SIGNATURE_DENNIS-SVEN-MITTMANN_20261026-1529 |
| Qualification level | QESig |
| Validation indication | **TOTAL_PASSED** |
| Signature format | PKCS7-LT |
| Certificate chain | Swisscom Diamant EU CA 4.1 AT / Swisscom Root CA 4 |
| Claimed signing time | 2026-10-26 15:29:28 UTC |
| Best signature time | 2026-10-26 15:30:07 UTC |
| Qualified timestamp | PASSED |
| Valid signatures | 1 of 1 |
| DSS version | 6.5.1 |

The report records a successful validation result for this new test signature.

It also records that the revocation-data check was skipped for the certificate and identifies the signature scope as `PARTIAL`. These details are retained for technical transparency.

### Response to previous validation objection

The earlier rejection identified a signature whose claimed signing time preceded the issuance of its signing certificate.

The October 26 test provides new evidence from the same European Commission DSS validation system showing **TOTAL_PASSED**, rather than the previously reported `INDETERMINATE` result.

This demonstrates that the earlier reported failure is not reproduced in the newly supplied test document.

The supplied result establishes the validation outcome for this particular document. A separate Swiss Admin validation report has not been included in this evidence package.

### Additional video evidence

BlockSign QES + MFA Biometrics:

https://www.youtube.com/watch?v=c1F7T-3mYlw

### Reviewer verification

The original and signed PDF files can be submitted to the European Commission's DSS validator:

https://ec.europa.eu/digital-building-blocks/DSS/webapp-demo/validation

**Evidence status:** Implementation demonstrated through reviewer testing and supported by a new DSS report confirming `QESig / TOTAL_PASSED`.

---

## Output 3 — QES Verification

**Requirement:** Allow electronic signatures to be verified using a recognised verification tool.

### Implementation

BlockSign provides document-signature verification, including the evaluation of embedded signing evidence, signer certificates, document integrity, and signature validity.

The platform provides an authenticated verification interface:

https://blocksign.io/verification_upload

Signed documents can also be independently checked using external validation tools.

### Evidence

**European Commission DSS validation**

The October 26, 2026 validation report confirms one valid qualified electronic signature.

**Supporting screenshots**

AI Verification:

https://github.com/Docufi3d/Fund-13/blob/main/M2/AI-Verification.png

AES:

https://github.com/Docufi3d/Fund-13/blob/main/M2/AES.png

FES:

https://github.com/Docufi3d/Fund-13/blob/main/M2/FES.png

QES:

https://github.com/Docufi3d/Fund-13/blob/main/M2/QES.png

**Additional supporting screenshots**

https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9664.png

https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9665.png

https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9666.png

https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9667.png

### Clarification

The signature evidence, the signed PDF, and the DSS validation report serve different purposes.

The signed PDF is the cryptographic artifact.

The screenshots document implementation and verification interfaces.

The DSS report provides the independent validation outcome.

Together, they provide a more complete evidence package than screenshots alone.

**Evidence status:** Independent DSS verification of the new QES document passed.

---

## Output 4 — User-Friendly Access Points

**Requirement:** Provide accessible frontend entry points for identity verification and electronic signing.

### Implementation

The BlockSign interface integrates:

- Document upload and preparation.
- Signer invitation and workflow creation.
- Electronic signature selection.
- Separate eIDAS and ZertES capabilities.
- Swisscom provider onboarding.
- Account-level signing entitlements.
- Signature status monitoring.
- Document download.
- Signature verification.
- Optional biometric MFA.

The user's profile presents the available and pending signing capabilities.

The system also distinguishes between payment or voucher entitlement, provider onboarding, and successful signature execution.

### Evidence

https://blocksign.io/

https://blocksign.io/profile

https://blocksign.io/profile#workflows

https://blocksign.io/verification_upload

Supporting demonstration:

https://blocksign.io/videos/Demo.mp4

**Evidence status:** Frontend workflows have been made available for independent reviewer testing.

---

## Output 5 — Legal and Regulatory Requirements

**Requirement:** Provide publicly accessible information about the legal and regulatory framework.

### Implementation

BlockSign maintains public information addressing:

- eIDAS.
- ZertES.
- Electronic signature levels.
- Qualified trust service provider integration.
- GDPR and data protection.
- Signature verification and document integrity.
- Information security and compliance.

Signature eligibility and legal effects depend on the selected legal framework, signature level, and applicable requirements.

### Evidence

Compliance:

https://blocksign.io/co

Trust Center:

https://blocksign.io/trust-center

Swisscom Trust Services partner information:

https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services

**Evidence status:** Public compliance and regulatory documentation is provided.

---

## Output 6 — Free Trial Access

**Requirement:** Make the platform available for independent milestone review without requiring reviewers to pay.

### Implementation

BlockSign supports reviewer access through account-based testing and controlled voucher redemption.

The voucher system allows the configured signing or document-payment entitlement to be obtained without an actual payment.

Vouchers are scoped to the permitted action.

Voucher redemption does not bypass security or the regulated Swisscom identity and signing process.

### Evidence

https://blocksign.io/pricing

https://blocksign.io/profile

### Independent reviewer confirmation

Previous Milestone Reviewers confirmed testing of the platform using provided reviewer vouchers, including successful execution of signing workflows.

Reviewer credentials and voucher codes are distributed privately and are not included in public evidence.

**Evidence status:** Free reviewer access has been implemented and exercised.

---

## Output 7 — ISO 27001 Certification

**Requirement:** Provide evidence of ISO 27001 certification.

### Implementation

BlockSign GmbH operates an ISO 27001:2022-certified information security management system.

Public certificate information and the independent verification route are provided through the Trust Center.

### Evidence

https://blocksign.io/trust-center

**Evidence status:** Public certification evidence is available for independent review.

---

# B. Marketing and Visibility

## Output 8 — Public Demonstration Videos

**Requirement:** Publish demonstrations of the biometric KYC, QES signing, and QES verification processes.

### Additional public YouTube evidence

**1. Biometric enrolment**

BlockSign Biometric MFA Enrolment:

https://www.youtube.com/watch?v=cU3MLJUoPNY

**2. Qualified electronic signing**

BlockSign Sign QES + MFA Biometrics:

https://www.youtube.com/watch?v=c1F7T-3mYlw

**3. Integration demonstration**

BlockSign Hausakte24 Integration:

https://www.youtube.com/watch?v=zvhASAlGw9U

### Additional existing demonstration materials

https://blocksign.io/videos/BlockSign-QES-Biometrics.mp4

https://blocksign.io/videos/Demo.mp4

https://blocksign.io/videos/Sign-AES.mp4

https://blocksign.io/videos/Sign-QES-Biometrics-Available.mp4

https://blocksign.io/videos/Login-AES-QES-Verification.mp4

### Response to reviewer concerns

The reviewer noted that earlier demonstration materials depicted a legacy internal identity and signing implementation.

We distinguish between:

1. Historical recordings documenting earlier implementation stages.
2. Current production signing through Swisscom Trust Services.
3. Independent evidence of the resulting signature's validity.

Historical recordings are retained as supplementary evidence, not presented as proof that obsolete workflows remain in production.

The newly provided signed document and DSS validation report demonstrate the resulting QES artifact and independent verification outcome.

The current Swisscom-backed process is directly accessible for reviewer testing.

These additional materials do not, by themselves, establish that the required current-production KYC, signing, and verification walkthroughs have all been captured in the requested video format.

**Evidence status:** Additional videos are publicly available. The coverage of every required current-production workflow remains subject to review.

---

## Output 9 — Publications, Case Study and Real User Feedback

**Requirement:** Provide public communications and a structured usability study based on real users.

### Part A — Usability and user feedback

The original July–August 2025 process report is now accompanied by dedicated usability documentation.

**1. BlockSign Process Report — July–August 2025**

https://github.com/Docufi3d/Fund-13/blob/main/M2/blocksign_process_report_2025-07-01_2025-08-31_EN.pdf

This report provides operational usage and process information for the reporting period.

**2. Usability Study Evaluation — July/August 2025**

https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_Usability_Study_Evaluation_July_August_2025.pdf

This is submitted as the dedicated usability-study evaluation.

**3. Twenty-Five Completed Questionnaires**

https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_25_Completed_Questionnaires_Internal_Working_File.pdf

These questionnaires are provided as supporting participant-feedback material.

### Response to reviewer objection

The reviewer previously stated that the operational process report alone did not satisfy the acceptance criterion because it did not contain the required qualitative user feedback.

We are therefore submitting the usability-study evaluation and completed questionnaires as separate supporting documents.

The intent is to make both the study evaluation and its underlying participant material accessible, rather than relying exclusively on aggregated platform telemetry.

The evaluation should be assessed against the agreed requirements for participant tasks, completion times, direct feedback, and improvement suggestions.

### Part B — Marketing publications

**Digital identity and qualified signatures**

https://www.linkedin.com/pulse/digital-identity-qualified-signatures-why-compliance-matters-1qste

**Milestone progress**

https://www.linkedin.com/pulse/docufi3d-achieves-first-project-catalyst-milestone-prepares-okize/?published=t

**BlockSign X publication**

https://x.com/BlockSign_io/status/2041852509489152453

**Docufi3d X publication**

https://x.com/docufi3d/status/1973396841816273282

**Swisscom Trust Services publication**

https://www.linkedin.com/posts/swisscom-trust-services_digitaltrust-electronicsignature-qualifiedelectronicsignature-activity-7382314553600008193-GpWK

**Public product demonstration**

https://blocksign.io/videos/Demo.mp4

**New BlockSign / Cardano / Swisscom marketing video**

https://youtu.be/zkV8sZrzvds

**Evidence status:** The submission now includes dedicated usability documentation, participant questionnaires, and public marketing publications. The detailed study contents should be considered against the original usability acceptance criteria.

---

# C. Case Studies and Client Pilots

## Output 10 — Hausakte24 Pilot Integration

**Requirement:** Demonstrate the collaboration with Hausakte24 and the use of the integration in a customer pilot.

### Implementation

The Hausakte24 pilot demonstrates integration of the BlockSign document and electronic signature capabilities into a customer-specific workflow.

### Public evidence

**Hausakte24 integration video**

https://www.youtube.com/watch?v=zvhASAlGw9U

**Public Hausakte24 communication**

https://www.linkedin.com/posts/hausakte24_meilenstein-erreicht-ab-anfang-2026-digitale-activity-7406633316189327360-u3c8

The video and public communication provide evidence of the pilot integration and its commercial use case.

### Response to reviewer concerns

This evidence is separate from the general platform demonstration and specifically addresses the pilot-customer requirement.

The reviewer has previously acknowledged the additional Hausakte24 collaboration evidence in an approval.

**Evidence status:** Public pilot-related communication and integration demonstration are supplied.

---

## Output 11 — Swisscom and BlockSign Presentation

**Requirement:** Publish a joint presentation covering the Swisscom/Docufi3d integration, the benefits of Cardano, and the required project branding.

### Updated marketing evidence

A new public marketing video is available on YouTube:

**BlockSign + Cardano + Swisscom**

https://youtu.be/zkV8sZrzvds

The newly published video is submitted to address the earlier concerns about publication channel and co-branding.

### Technical blockchain evidence

The end-to-end demonstration also includes a Cardano transaction reference:

https://cardanoscan.io/transaction/7b0b81c8469f204dd3ca3f5122c56f0b4dc02a4acd4439c1473ac08c7e26dd81

Cardano's intended technical role in the BlockSign architecture is to provide an independently accessible blockchain evidence reference, complementary to the electronic signature and trust-provider evidence.

The Cardano record is not presented as the qualified signature itself.

The qualified signature is issued through the applicable Swisscom process.

The blockchain reference provides an additional audit-evidence pathway that can be inspected outside BlockSign.

### Additional Swisscom partnership evidence

Official partner information:

https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services

### Response to reviewer objections

The most recent rejection identified three specific concerns:

1. Cardano's benefits were not explained.
2. The video was not published on an agreed public channel.
3. The earlier submitted recording was defective or incomplete.

The new marketing video provides a new public YouTube publication featuring the specified brands.

The accompanying Cardano transaction reference makes the blockchain component independently accessible for examination.

We ask the reviewers to assess the new marketing video instead of relying solely on the previously submitted recording.

The presence of all three brands does not, by itself, establish a joint presentation involving Swisscom personnel. The final assessment should distinguish branding from direct partner participation.

**Evidence status:** The new publication, Cardano explanation, and blockchain evidence materially strengthen this output. Verification of joint Swisscom participation and the full video contents remains relevant to the acceptance decision.

---

## Output 12 — Industry Event Presentation

**Requirement:** Provide evidence of the integration being presented at a relevant industry event with Swisscom participation.

### Event

**Swisscom Trust Up 2025**

- Date: September 29, 2025
- Location: Prime Tower / Clouds Bar
- Address: Maagplatz 5, 8005 Zurich, Switzerland

### Evidence

**Swisscom event video**

https://www.youtube.com/watch?v=OSNYPxfguE4

**Swisscom partner reference**

https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services

**Event communication**

https://x.com/BlockSign_io/status/1978768209219084707

**LinkedIn communication**

https://www.linkedin.com/posts/digitalidentity-blockchaincompliance-qes-share-7350803243607724034-KC2T/

These materials are provided as evidence of the event context, Swisscom partnership, and project visibility.

The specific acceptance criterion additionally requests official confirmation of the participation and presentation by Driton Salai, explicitly referencing the integration project. Such confirmation should be evaluated separately from general event attendance and partnership publicity.

**Evidence status:** Event and partnership evidence has been provided. The specifically requested speaker/presentation confirmation is not established by the links alone.

---

# D. Additional Technical Evidence — Cardano Blockchain Integration

The blockchain component provides an optional additional audit-evidence layer alongside the regulated electronic signature.

The roles of the systems are deliberately separated:

| Component | Responsibility |
|---|---|
| BlockSign | Document management, workflow coordination, signer invitations and audit context |
| Swisscom Trust Services | Provider-managed identity verification, regulated signing and qualified trust services |
| European Commission DSS | Independent validation of electronic signature evidence |
| Cardano | Public blockchain reference for additional audit evidence |

The qualified electronic signature and its certificate evidence are independent of the availability of the Cardano network.

Similarly, Cardano metadata does not itself establish a qualified electronic signature under eIDAS.

### Public blockchain evidence

Transaction:

https://cardanoscan.io/transaction/7b0b81c8469f204dd3ca3f5122c56f0b4dc02a4acd4439c1473ac08c7e26dd81

The transaction is supplied as the blockchain reference used in the demonstration.

The relationship between the transaction metadata and the document must be established through the relevant metadata fields, document identifier, or reproducible hash comparison.

---

# E. Consolidated Evidence Register

| Output | Evidence package |
|---|---|
| 1 — KYC | Swisscom-backed production onboarding, reviewer testing, historical biometric enrolment video |
| 2 — QES | Signed test PDF, Swisscom integration, DSS `TOTAL_PASSED` report |
| 3 — Verification | DSS validation report, AES/FES/QES screenshots, verification interface |
| 4 — Frontend Access | Production BlockSign application, profile workflows, demonstration video |
| 5 — Legal Requirements | Compliance page, Trust Center, Swisscom partnership information |
| 6 — Free Trial | Reviewer vouchers, account access, independently tested workflows |
| 7 — ISO 27001 | Public Trust Center and certificate verification route |
| 8 — Demonstration Videos | Public YouTube and hosted demonstration recordings |
| 9 — User Feedback / Marketing | Process report, usability study, 25 questionnaires, public communications |
| 10 — Hausakte24 | Integration video and public pilot communication |
| 11 — Swisscom / Cardano Presentation | New co-branded marketing video, Cardano transaction, partner reference |
| 12 — Industry Event | Swisscom Trust Up 2025 communications and event material |

---

# F. Response to the Latest Rejection

We appreciate the reviewer's acknowledgement that the core regulated identity and signing integration is operational.

We have taken the additional objections seriously and have expanded the evidence record accordingly.

### 1. QES validation

A newly signed document and a European Commission DSS v6.5.1 report have been supplied.

The report explicitly records **QESig** and **TOTAL_PASSED**, including a passed qualified timestamp.

This provides new evidence against the earlier signing-time-related validation failure.

### 2. Demonstration videos

Additional historical videos have been made publicly accessible on YouTube.

The submission clearly distinguishes earlier implementation stages from the current Swisscom-backed production architecture.

The new signed document and independent validation report also substantiate the outcome of the current signing process.

### 3. Usability study

The operational process report is no longer submitted as the sole evidence of usability.

A dedicated evaluation report and 25 completed questionnaires are included as separate supporting materials.

### 4. Cardano and Swisscom marketing evidence

A new marketing video featuring BlockSign, Cardano, and Swisscom branding has been published on YouTube.

An external Cardano transaction reference is also provided to demonstrate the blockchain component of the audit-evidence architecture.

### 5. Previously completed independent testing

Earlier milestone reviews resulted in approvals from multiple reviewers.

Their findings included successful execution of Swisscom onboarding and QES signing, testing through reviewer vouchers, and examination of the additional marketing, compliance, and pilot evidence.

These approvals provide relevant context for the milestone's implementation maturity, while the newly raised technical and documentation issues are addressed individually above.

---

# G. Final Statement

Milestone 2 represents the integration of several independently verifiable components:

- Regulated identity onboarding through Swisscom Trust Services.
- Advanced and qualified electronic signing.
- Optional biometric multi-factor authentication.
- Electronic signature validation.
- Usable document-signing workflows.
- ISO 27001 information-security controls.
- Public demonstration and marketing materials.
- Customer pilot integration.
- Usability-study documentation.
- Optional Cardano blockchain audit evidence.

The submission now contains a substantially expanded evidence record, including a new qualified electronic signature that the European Commission DSS validator reports as **TOTAL_PASSED**.

We respectfully request that the reviewers reassess all twelve milestone outputs using the complete evidence package, taking into account the successful independent reviewer testing already conducted, the new technical validation results, and the additional public documentation.

Where a specific criterion is still considered unmet, we request that the remaining requirement be identified precisely against its agreed acceptance wording and the evidence supplied.

We remain committed to transparent, technically reproducible verification and to resolving any concrete outstanding deficiency.

Kind regards,

**BlockSign Team**  
BlockSign GmbH  
https://blocksign.io/
