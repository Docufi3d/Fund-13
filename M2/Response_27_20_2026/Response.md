# BlockSign — Fund 13, Milestone 2
## Consolidated Response and Evidence of Delivery — Revised October 27, 2026

**Milestone:** QES and Biometric KYC Integration with Swisscom + Case Study #1  
**Project:** Docufi3d / BlockSign  
**Purpose:** Response to the latest milestone review, covering all twelve agreed outputs and the supplemental evidence package.

Dear Catalyst Milestone Reviewers,

This revised submission consolidates the evidence for all twelve Milestone 2 outputs and specifically addresses the latest objections concerning QES validation (Outputs 2–3), current-workflow videos (Output 8), user-feedback documentation (Output 9), and the Swisscom/Cardano presentation (Output 11).

A reviewer has confirmed: **“We successfully completed KYC and executed the QES document signing using the Swisscom integration.”** Three other review responses approved the milestone. The new materials described below are intended to respond to the remaining concrete evidentiary objections; previous approvals are contextual support, not a substitute for meeting each acceptance criterion.

**Branding continuity:** IAMX AG (project initiator) → Docufi3d UG (haftungsbeschränkt) → BlockSign GmbH. Historical videos retain former branding and are clearly distinguished from the current Swisscom-backed production implementation.

## Evidence overview — key new submissions

- **Current production workflow, QES signing, verification and Cardano integration:** [New YouTube demonstration / co-branded video](https://www.youtube.com/watch?v=zkV8sZrzvds). This is submitted under **both Output 8 and Output 11**.
- **External provider onboarding/authentication:** supporting Swisscom **Nect and Mobile ID screenshots**: [IMG_9664](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9664.png), [IMG_9665](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9665.png), [IMG_9666](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9666.png), [IMG_9667](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9667.png). The screenshots supplement the current video and the reviewer's own successful KYC test; they are not claimed to be a continuous video of all Nect identity-proofing screens.
- **Reproducible signature evidence:** [original PDF](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument.pdf), [signed PDF](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument_Signed.pdf), [DSS v6.5.1 validation report](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/DSS-Simple-report%20.pdf).
- **Cardano public audit reference:** [transaction 7b0b81c8…c7e26dd81](https://cardanoscan.io/transaction/7b0b81c8469f204dd3ca3f5122c56f0b4dc02a4acd4439c1473ac08c7e26dd81).
- **Usability evidence:** [July–August 2025 process report](https://github.com/Docufi3d/Fund-13/blob/main/M2/blocksign_process_report_2025-07-01_2025-08-31_EN.pdf), [usability evaluation](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_Usability_Study_Evaluation_July_August_2025.pdf), and [25 completed questionnaires](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_25_Completed_Questionnaires_Internal_Working_File.pdf).

---

# A. Product Development

## Output 1 — Biometric KYC and Identity Onboarding

**Requirement:** Implement user identity verification and an accessible regulated onboarding process.

**Implementation.** BlockSign integrates Swisscom Trust Services provider-side onboarding, identity and credential processes for the configured eIDAS and ZertES FES/QES workflows. When a signer initiates a matching document-signature request and lacks appropriate provider evidence, the signing flow starts the corresponding Swisscom onboarding. BlockSign's optional biometric MFA is an additional account/signature authentication factor, **not** a substitute for regulated Swisscom KYC.

**Evidence:**

- [Current account / framework-specific readiness](https://blocksign.io/profile#workflows) (login required).
- [Historical BlockSign Biometric MFA enrolment video](https://www.youtube.com/watch?v=cU3MLJUoPNY).
- Swisscom/Nect and Mobile ID screenshots: [9664](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9664.png), [9665](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9665.png), [9666](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9666.png), [9667](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9667.png).
- Reviewer's independent confirmation of successful KYC and QES signing.

**Reviewer reproduction:** Sign in, select the relevant eIDAS or ZertES readiness card, upload a non-sensitive test PDF, create a FES/QES request, and start signing to trigger Swisscom onboarding as needed. A reviewer voucher can settle the entitlement without bypassing identity checks.

## Output 2 — Qualified Electronic Signature Implementation

**Requirement:** Produce regulated qualified electronic signatures.

**Implementation.** BlockSign coordinates document upload, signer invitation, legal-framework selection, entitlement checking and Swisscom-backed FES/QES execution. Payment or voucher redemption is an account entitlement, not KYC or a signature. The eIDAS and ZertES paths maintain separate corresponding evidence.

**Current production demonstration:** [BlockSign / Swisscom / Cardano video](https://www.youtube.com/watch?v=zkV8sZrzvds).  
**Historical supporting video:** [QES + MFA biometrics](https://www.youtube.com/watch?v=c1F7T-3mYlw).

**October 26, 2026 reproducible test evidence:**

1. [Original TestDocument.pdf](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument.pdf)
2. [Swisscom-signed TestDocument_Signed.pdf](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument_Signed.pdf)
3. [European Commission DSS validation report](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/DSS-Simple-report%20.pdf)

The supplied **DSS v6.5.1** report records signature `SIGNATURE_DENNIS-SVEN-MITTMANN_20261026-1529`, qualification **QESig**, indication **TOTAL_PASSED**, signature format `PKCS7-LT`, **1 valid signature out of 1**, and a qualified timestamp **PASSED**. It records a claimed signing time of **2026-10-26 15:29:28 UTC** and a best signature time of **2026-10-26 15:30:07 UTC**, through the Swisscom certificate chain.

**Response to the previous timestamp defect.** The reviewer reported a prior `INDETERMINATE` signature, where its declared signing time preceded certificate issuance. The fresh document produces **TOTAL_PASSED** in DSS, demonstrating that the prior objection was **not reproduced in this particular test**. For transparency, this report also notes that the certificate revocation-data check was skipped and the signature scope is reported as `PARTIAL`. A fresh Swiss Admin Validator report is **not included**; the DSS result should not be described as proving all validators will always pass.

## Output 3 — Independent QES Verification

**Requirement:** Verify a signed document in a recognised validation tool.

**Implementation.** An authenticated user can upload PDFs to [BlockSign's verification interface](https://blocksign.io/verification_upload). The independently usable signed artifact and its DSS validation report provide direct external evidence, rather than requiring acceptance of a platform screenshot alone.

**Evidence:** [Signed PDF](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument_Signed.pdf), [DSS result](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/DSS-Simple-report%20.pdf), [EU DSS validation site](https://ec.europa.eu/digital-building-blocks/DSS/webapp-demo/validation), and historical supporting screenshots: [AI verification](https://github.com/Docufi3d/Fund-13/blob/main/M2/AI-Verification.png), [AES](https://github.com/Docufi3d/Fund-13/blob/main/M2/AES.png), [FES](https://github.com/Docufi3d/Fund-13/blob/main/M2/FES.png), [QES](https://github.com/Docufi3d/Fund-13/blob/main/M2/QES.png).

The [current production demonstration](https://www.youtube.com/watch?v=zkV8sZrzvds) also covers document verification and the external validation result. The DSS file gives the actual test-level conclusion: **QESig / TOTAL_PASSED**.

## Output 4 — User-Friendly Access Points

**Requirement:** Provide intuitive frontend access to KYC, signing and verification.

**Implementation and evidence:** [BlockSign](https://blocksign.io/), [profile](https://blocksign.io/profile), [workflows](https://blocksign.io/profile#workflows), and [verification](https://blocksign.io/verification_upload). The application provides upload, invitation, signature level and legal-framework selection, profile readiness, provider onboarding, download and verification. The [new end-to-end video](https://www.youtube.com/watch?v=zkV8sZrzvds) shows the present interface; [earlier demo](https://blocksign.io/videos/Demo.mp4) documents the product's development history.

## Output 5 — Legal and Regulatory Requirements

**Requirement:** Public legal and compliance documentation.

**Evidence:** [Compliance page](https://blocksign.io/co), [Trust Center](https://blocksign.io/trust-center), and [Swisscom Trust Services partner reference](https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services). The documentation covers eIDAS, GDPR, signing levels, trust services and information security. Selecting a signing level does not automatically establish suitability for every statutory form requirement.

## Output 6 — Free Reviewer Trial Access

**Requirement:** Allow independent testing without a real payment.

**Implementation.** Scoped single-use vouchers provide authorised test entitlements using the ordinary checkout process. They do not replace Swisscom onboarding or signing. Previous reviewers tested the platform using provided vouchers.

**Evidence:** [Pricing](https://blocksign.io/pricing), [profile](https://blocksign.io/profile). Voucher codes and credentials are supplied privately to reviewers, not in this public statement.

## Output 7 — ISO 27001 Certification

**Requirement:** Provide independently accessible ISO 27001 certification evidence.

**Evidence:** [BlockSign Trust Center](https://blocksign.io/trust-center), including the publicly provided ISO 27001:2022 certification and its verification route.

---

# B. Marketing and Visibility

## Output 8 — Public Video Demonstrations of KYC, QES Signing and QES Verification

**Requirement:** Public demonstrations covering KYC, QES execution, and signature verification.

### Primary, current-production evidence

**[New end-to-end BlockSign / Swisscom / Cardano video — YouTube](https://www.youtube.com/watch?v=zkV8sZrzvds)**

This video is submitted under **Output 8 as well as Output 11**. It shows the current BlockSign workflow: document upload and preparation, invitation/signing interactions, Swisscom signing authorisation, completed signing, BlockSign verification, Cardano audit-evidence reference and European Commission DSS verification. In particular, it supersedes reliance on old recordings for evidence of the **current QES signing and verification workflows**.

### Complementary evidence for the external Swisscom KYC stage

The separate Swisscom **Nect** identity-proofing and **Mobile ID** authentication/authorisation stages occur in provider-controlled environments. The following screenshots support the provider-side flow shown or referred to in the demonstration:

- [IMG_9664.png](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9664.png)
- [IMG_9665.png](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9665.png)
- [IMG_9666.png](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9666.png)
- [IMG_9667.png](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9667.png)

**Evidence distinction:** Nect identity verification and Mobile ID signing authorisation are not interchangeable. These screenshots are provided as **supplementary provider-process records**, rather than claimed to be an uninterrupted recording of every step of a new identity enrolment. We also reference the reviewer's own statement confirming that they completed KYC and QES signing successfully using the Swisscom integration.

In the latest resolution, the reviewer explicitly offered acceptance of external third-party handoffs as a **“black box”** when accompanied by a written explanation of what happens there and why capturing it in a continuous product recording may not be possible. This paragraph provides that distinction; the screenshots provide complementary observable evidence.

### Historical videos (development record, not proof of the present provider flow)

- [BlockSign Biometric MFA Enrolment](https://www.youtube.com/watch?v=cU3MLJUoPNY)
- [BlockSign Sign QES + MFA Biometrics](https://www.youtube.com/watch?v=c1F7T-3mYlw)
- [BlockSign Hausakte24 Integration](https://www.youtube.com/watch?v=zvhASAlGw9U)
- [Earlier QES biometrics video](https://blocksign.io/videos/BlockSign-QES-Biometrics.mp4)
- [Earlier general demonstration](https://blocksign.io/videos/Demo.mp4)
- [Earlier AES signing](https://blocksign.io/videos/Sign-AES.mp4)
- [Earlier QES signing](https://blocksign.io/videos/Sign-QES-Biometrics-Available.mp4)
- [Earlier login and verification recording](https://blocksign.io/videos/Login-AES-QES-Verification.mp4)

**Response to the latest Output 8 objection:** The new video supplies current signing and verification footage in place of relying on obsolete workflows. The Nect/Mobile ID screenshots and the reviewer's own independent KYC result supplement the external identity-provider portion. The historical recordings are labelled to avoid suggesting their deprecated architecture remains in production.

## Output 9 — Usability Study, User Feedback and Public Communications

**Requirement:** A structured small-group usability study with task completion time, feedback, quotes and improvement suggestions; plus milestone-specific publications.

### Usability package

- [BlockSign Process Report, July–August 2025](https://github.com/Docufi3d/Fund-13/blob/main/M2/blocksign_process_report_2025-07-01_2025-08-31_EN.pdf) — operational usage/process data.
- [Usability Study Evaluation, July/August 2025](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_Usability_Study_Evaluation_July_August_2025.pdf) — dedicated study evaluation.
- [25 Completed Questionnaires](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_25_Completed_Questionnaires_Internal_Working_File.pdf) — supporting participant feedback.

The latest reviewer correctly distinguished telemetry from qualitative user feedback. The **process report is not offered as the sole usability study**; the evaluation and questionnaires are included specifically to address that criticism. Reviewers should assess whether these documents contain the required specific scenarios, completion times, participant quotations and actionable suggestions. No unverified study statistics or participant quotations are invented here.

### Public communications

- [Digital identity / qualified signatures LinkedIn article](https://www.linkedin.com/pulse/digital-identity-qualified-signatures-why-compliance-matters-1qste)
- [Milestone progress LinkedIn article](https://www.linkedin.com/pulse/docufi3d-achieves-first-project-catalyst-milestone-prepares-okize/?published=t)
- [BlockSign X post](https://x.com/BlockSign_io/status/2041852509489152453)
- [Docufi3d X post](https://x.com/docufi3d/status/1973396841816273282)
- [Swisscom Trust Services LinkedIn post](https://www.linkedin.com/posts/swisscom-trust-services_digitaltrust-electronicsignature-qualifiedelectronicsignature-activity-7382314553600008193-GpWK)
- [New co-branded public video](https://www.youtube.com/watch?v=zkV8sZrzvds)

---

# C. Case Studies and Client Pilots

## Output 10 — Hausakte24 Pilot Collaboration

**Requirement:** Show integration and usage in a customer pilot with public confirmation.

**Evidence:** [Hausakte24 integration video](https://www.youtube.com/watch?v=zvhASAlGw9U) and [Hausakte24's public pilot communication](https://www.linkedin.com/posts/hausakte24_meilenstein-erreicht-ab-anfang-2026-digitale-activity-7406633316189327360-u3c8). This is pilot-specific evidence, separate from the general product walkthrough.

## Output 11 — Swisscom / BlockSign Presentation and Cardano Benefits

**Requirement:** A publicly accessible co-branded presentation covering the integration and Cardano's benefits, on one of the agreed publication channels, including the required participation by Swisscom.

**Primary new public video (also Output 8):** [BlockSign + Cardano + Swisscom on YouTube](https://www.youtube.com/watch?v=zkV8sZrzvds).

**Public on-chain evidence:** [Cardano transaction](https://cardanoscan.io/transaction/7b0b81c8469f204dd3ca3f5122c56f0b4dc02a4acd4439c1473ac08c7e26dd81).

**Official partnership reference:** [Swisscom Trust Services — Docufi3d/IAMX partner page](https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services).

The technical division of responsibilities is important:

| Component | Role |
|---|---|
| BlockSign | Document management, signer workflows and audit context |
| Swisscom Trust Services | Regulated identity/credential process and signature trust services |
| European Commission DSS | Independent examination and validation of the electronic signature |
| Cardano | Publicly inspectable additional blockchain audit reference |

Cardano supplies **independent audit-evidence anchoring**; the Cardano transaction is **not itself a qualified electronic signature**. Its precise relationship to the signed document should be checked through the transaction metadata and matching document/hash evidence.

**Response to the previous Output 11 objections:** The new video replaces reliance on the previously reported defective/black-screen recording, is hosted on **YouTube**, and is described as featuring **BlockSign, Cardano and Swisscom co-branding**. The Cardano transaction and explanation above articulate the intended blockchain benefit. To meet the distinct **joint presentation** condition, direct Swisscom participation must be demonstrated by the video or separate corroboration; co-branding alone does not prove that a Swisscom representative jointly presented it. The final playback and narration should also be checked against the criterion.

## Output 12 — Relevant Industry Event Presentation

**Requirement:** Industry-event evidence referencing the integration, including the specified Swisscom participant and required co-branding.

**Event:** Swisscom Trust Up 2025, **September 29, 2025**, Prime Tower / Clouds Bar, Maagplatz 5, 8005 Zurich.

**Evidence:**

- [Swisscom Trust Up event video](https://www.youtube.com/watch?v=OSNYPxfguE4)
- [Swisscom partner listing](https://trustservices.swisscom.com/de/docufi3d-von-iamx-ein-partner-von-swisscom-trust-services)
- [Event communication on X](https://x.com/BlockSign_io/status/1978768209219084707)
- [LinkedIn event communication](https://www.linkedin.com/posts/digitalidentity-blockchaincompliance-qes-share-7350803243607724034-KC2T/)

These links document the event context and partnership. The acceptance criterion additionally calls for official confirmation of **Driton Salai's participation and presentation** referencing this specific integration; general event publicity should not be misrepresented as that exact proof.

---

# D. Consolidated Reviewer Response to the Latest Resolution

| Reviewer issue | New or clarified evidence | Scope and qualification |
|---|---|---|
| **Outputs 2 & 3 — claimed signing time earlier than certificate issuance** | [Fresh signed document](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/TestDocument_Signed.pdf) and [DSS `QESig / TOTAL_PASSED` report](https://github.com/Docufi3d/Fund-13/blob/main/M2/Response_27_20_2026/DSS-Simple-report%20.pdf) | The prior error was not reproduced for this new document. A Swiss Admin validation report is not yet supplied. |
| **Output 8 — obsolete videos, missing current QES verification** | [New production video](https://www.youtube.com/watch?v=imFomYJnVn8) showing current signing and verification | Earlier recordings clearly marked historical. |
| **Output 8 — external Swisscom KYC stage** | [Nect/Mobile ID screenshots](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9664.png) ([2](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9665.png), [3](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9666.png), [4](https://github.com/Docufi3d/Fund-13/blob/main/M2/IMG_9667.png)), external-provider explanation, reviewer's successful test | Provider screenshots plus black-box explanation, not a continuous KYC video. |
| **Output 9 — aggregated usage data insufficient** | [Dedicated usability evaluation](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_Usability_Study_Evaluation_July_August_2025.pdf) and [25 questionnaires](https://github.com/Docufi3d/Fund-13/blob/main/M2/B/docufi3d_25_Completed_Questionnaires_Internal_Working_File.pdf) | Separate qualitative sources; precise task times/quotes must be evaluated against the files. |
| **Output 11 — video branding, platform and Cardano benefits** | [New YouTube video](https://www.youtube.com/watch?v=imFomYJnVn8), [Cardano transaction](https://cardanoscan.io/transaction/7b0b81c8469f204dd3ca3f5122c56f0b4dc02a4acd4439c1473ac08c7e26dd81) and explicit division of system responsibilities | Direct Swisscom presenter participation and full video content remain separate questions. |

## Final request

The primary Swisscom identity and qualified-signature integration has been independently tested by a reviewer. This response now links a new signed artifact and successful DSS report, a current-production public video usable for **both Outputs 8 and 11**, the **Nect/Mobile ID supporting screenshots**, and the dedicated usability-study evidence.

We respectfully request a renewed evaluation against the agreed acceptance criteria, taking the updated, independently inspectable materials together rather than treating historical demonstrations as the present implementation. If a criterion remains unfulfilled, please identify the precise missing evidence and acceptance wording so it can be addressed without ambiguity.

Kind regards,  
**BlockSign Team**  
BlockSign GmbH — https://blocksign.io/
