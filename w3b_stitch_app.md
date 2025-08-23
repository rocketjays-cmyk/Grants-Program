# Name of your Project:W3b-Stitch

> [!NOTE]
> This document will be part of the terms and conditions of your agreement and, therefore, needs to contain all the required information about the project. Don't remove any of the mandatory parts presented in bold letters or as headlines (except for the title)! Lines starting with a `>` (such as this one) should be removed. Please use markdown instead of HTML (e.g., `![](image.png)` instead of `<img>`).
>
> See the [Grants Program Process](https://grants.web3.foundation/docs/process) on how to submit a proposal.

- **Team Name:** W3b Stitch Technologies L.L.C
- **Payment Details:**
  - **DOT**: 15mNcGQnJVKv9PXLhWEQWcz4VeBJESLDrgvsU7FN9bw1XAmB
  - **Payment**:(USDC) 15mNcGQnJVKv9PXLhWEQWcz4VeBJESLDrgvsU7FN9bw1XAmB
- **[Level](https://grants.web3.foundation/docs/Introduction/levels):** 1, 2 or 3

> [!IMPORTANT]
> *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*

## Project Overview :page_facing_up:W3b Stitch is a decentralized trust engine designed to make digital interactions verifiable, transparent, and secure. The application provides an MVP credential and media verification service, enabling users and organizations to anchor proofs of authenticity on-chain and verify them seamlessly through a simple web interface. By combining decentralized identifiers (DIDs), verifiable credentials, and blockchain anchoring, W3b Stitch empowers individuals, enterprises, and communities to validate the integrity of content, credentials, and identities without relying on centralized intermediaries.

The short-term focus of the app is to demonstrate a working prototype that allows users to upload digital content or credentials, generate a verifiable proof, and confirm authenticity against an immutable ledger. In the long term, W3b Stitch aims to evolve into a scalable trust layer supporting cross-industry use cases—from media verification and academic credentialing to supply chain integrity and decentralized reputation systems.
If this application is in response to an RFP, please indicate this on the first line of this section.

If this is an application for a follow-up grant (the continuation of an earlier, successful W3F grant), please provide the name and/or pull request of said grant on the first line of this section.

### Overview

Tagline

W3b Stitch — a decentralized trust engine for verifying media, credentials, and identities across blockchains.

Brief Description

W3b Stitch provides a platform for creating and verifying proofs of authenticity for digital content and credentials. Through a simple web app, users can anchor proofs on-chain and confirm integrity without relying on centralized authorities. The project bridges decentralized identifiers (DIDs), verifiable credentials, and blockchain anchoring into a unified, user-friendly application.

Integration with Substrate / Polkadot / Kusama

The Polkadot ecosystem is a natural fit for W3b Stitch due to its focus on interoperability and scalability. W3b Stitch can be extended as a Substrate pallet for credential verification, enabling parachains to integrate authenticity checks directly into their logic. Using XCM, proofs of authenticity can move seamlessly between parachains, making W3b Stitch a cross-ecosystem trust layer. Deployment on Kusama would allow for rapid iteration and testing, while Polkadot provides the long-term scalable environment for production use.

Team Interest

Our team is deeply motivated to solve the growing challenge of digital misinformation and unverifiable credentials. We believe that trust is a missing layer in Web3, and Polkadot’s architecture uniquely supports our vision of decentralized, interoperable, and scalable verification. By building W3b Stitch within this ecosystem, we can contribute to the broader mission of creating a trustworthy, open, and user-centric internet.
### Project Details

We expect the teams to already have a solid idea about your project's expected final state. Therefore, we ask the teams to submit (where relevant):
ockups / Designs of UI Components

The initial MVP will feature a web-based dashboard with the following core components:

Upload & Verification Panel – simple drag-and-drop for documents/media with instant verification results.

Credential Viewer – allows users to inspect verifiable credentials (VCs) and DID metadata.

Proof History – displays anchored transactions and status checks.
(Mockups available upon request; early wireframes demonstrate minimal but intuitive interactions for verification and credential anchoring.)

Data Models / API Specifications

Data Model:

Credential object (issuer, subject, metadata, proof hash).

ProofRecord object (hash, timestamp, anchor transaction ID, verification status).

Core APIs:

POST /anchor → submit hash for anchoring.

GET /verify/{hash} → confirm existence and validity on-chain.

GET /credential/{id} → retrieve credential metadata and verification record.

Technology Stack Overview

Frontend: Next.js (React) with Tailwind for styling.

Backend: NestJS (TypeScript) REST API.

Blockchain Layer: Substrate-based parachain integration for on-chain anchoring, starting with test deployments (Kusama/Westend).

Storage: IPFS for decentralized storage of optional proofs.

Identity: W3C DIDs & VCs for credential modeling.

Documentation of Core Components / Architecture

Core Components:

Credential Authentication & Provenance Module (CAPM).

Media Verification & Curation Module (MVCM).

Decentralized Identity & Reputation Module (DIRM).

Protocols: W3C Verifiable Credentials, Decentralized Identifiers, and Polkadot’s XCM for cross-parachain interoperability.

Architecture: Modular services built around a verification pipeline → input (media/credential) → hashing → on-chain anchoring (Substrate pallet) → verification response.

PoC / MVP or Prior Work

A WordPress-based prototype (news verification bot) has been deployed to demonstrate concept feasibility.

Core repo includes hash anchoring on EVM testnets (Sepolia) to validate workflow.

Whitepaper and provisional patent filed, outlining system architecture and long-term trust engine roadmap.

What the Project Will Not Provide

W3b Stitch is not a storage platform for raw media files; it anchors proofs, not content itself.

It will not replace existing identity providers; rather, it complements them via interoperability with DID/VC standards.

It will not deliver a public blockchain from scratch; instead, it leverages Substrate and Polkadot’s ecosystem.

It is not intended as a moderation tool for social platforms but as a verification layer they can integrate.
Things that shouldn’t be part of the application (see also our [FAQ](../docs/faq.md)):

- The (future) tokenomics of your project
- For non-infrastructure projects—deployment and hosting costs, maintenance or audits
- Business-oriented activities (marketing, business planning), events or outreach

### Ecosystem Fit

Help us locate your project in the Polkadot/Substrate/Kusama landscape and what problems it tries to solve by answering each of these questions:

Where and how does your project fit into the ecosystem?

W3b Stitch fits into the Polkadot ecosystem as a decentralized trust layer. By providing verifiable proofs for media, credentials, and identity, it can integrate with parachains, wallets, and dapps that need authenticated data flows. Using Substrate, a verification pallet can be implemented to make trust primitives available across parachains, and XCM can ensure that proofs are portable and interoperable. In this way, Polkadot serves as the base layer for trust, and W3b Stitch extends that value across the ecosystem.

Who is your target audience?

Developers building parachains, dapps, and wallets who need verifiable credentialing and media authenticity services.

Enterprises seeking Web3-based solutions for credential authentication, compliance, and fraud prevention.

End users who want confidence that the content they consume or credentials they rely on are authentic.

The wider Polkadot ecosystem, where trust and verification primitives can be reused by multiple teams.

What need(s) does your project meet?

W3b Stitch addresses the urgent need for everyday digital trust in Web3. It creates the infrastructure for verifying the authenticity of media, credentials, and identities in a scalable and decentralized way. With misinformation, fraud, and unverifiable credentials becoming systemic issues, W3b Stitch provides a standards-based solution built on DIDs, VCs, and blockchain anchoring.

How did you identify these needs?

The project began as an on-chain news aggregator and evolved as research and experimentation revealed broader applications. The architecture was expanded to cover media authenticity, identity, credentials, and security — ultimately forming the W3b Stitch trust engine. A provisional patent filed with the USPTO secures the novel architecture. Market research and analysis of digital trust trends confirmed the gravity and scale of the problem: misinformation and identity fraud already cost billions annually, and existing centralized solutions fail to meet Web3’s interoperability and transparency needs.

Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?

No. After extensive research, there appear to be no projects in the ecosystem that combine the robust flows and modular architecture of W3b Stitch. While some projects address decentralized identity or verifiable credentials in isolation, none integrate media verification, credential authentication, and decentralized identity into a cohesive trust layer.

If not, why might such a project not have been possible or attempted before?

Until recently, Web3 infrastructure was focused primarily on DeFi and token economies. The combination of standards (DIDs, VCs), maturing Substrate tooling, and Polkadot’s cross-chain messaging now makes it possible to deliver a scalable, multi-domain trust engine. Earlier attempts outside Polkadot likely failed due to siloed design, lack of interoperability, and limited adoption of trust standards.

Are there any projects similar to yours in related ecosystems?

No direct equivalents exist. While certain ecosystems (e.g., Ethereum, Solana) have experiments in identity or credentialing, none provide the modular, multi-domain trust architecture proposed by W3b Stitch. This novelty, combined with Polkadot’s interoperability and governance model, makes the project uniquely positioned to succeed here.
## Team :busts_in_silhouette:

> [!IMPORTANT]
> Please note that the data provided in this section is for administrative and informational purposes only. All beneficiaries of a grant must also be listed in the KYC/KYB process during the application phase. See our [FAQ](https://grants.web3.foundation/docs/faq#what-is-kyckyb-and-why-do-i-have-to-provide-this-data) for more info.

### Team members

- Name of team leader: Jayden C. Saliby
- Names of team members: 

### Contact

- **Contact Name:** Jayden C. Saliby
- **Contact Email:** Jaydencs@w3bstitch.com
- **Website:** WWW.w3bstitch.com

### Legal Structure

- **Registered Address:** 414 w whitehall street Allentown, pennsylvania, USA
- **Registered Legal Entity:** W3b Stitch Technologies L.L.C

### Team's experience

Team’s Relevant Experience

Our team brings together a mix of blockchain development, web application engineering, and applied research in digital identity and media verification. The founder has led the design of the W3b Stitch trust architecture, filed as a provisional patent with the USPTO, which outlines novel workflows for verifiable credentials, decentralized identity, and cross-chain media verification.

Relevant past work includes:

Prototype development of a news-verification aggregator integrated with blockchain proof anchoring.

Hash anchoring on EVM testnets (Sepolia) to validate proof-of-concept workflows.

Experience with modern web stacks (Next.js, NestJS, IPFS integration) for scalable MVP development.

Open-source contributions and research into decentralized identity standards (DIDs, VCs) and how they can be applied to real-world problems of digital trust.

Past Applications to Web3 Foundation

This is our first submission to the Web3 Foundation. No prior grants have been applied for under this project or related entities.

### Team Code Repos

-(https://github.com/rocketjays-cmyk/w3b-stitch)
- https://github.com/{your_organisation}/{project_2}

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/rocketjays-cmyk
- https://github.com/{team_member_2}

### Team LinkedIn Profiles (if available)

- www.linkedin.com/in/w3bstitch
- https://www.linkedin.com/{person_2}


## Development Status :open_book:

If you've already started implementing your project or it is part of a larger repository, please provide a link and www.linkedin.com/in/


- links to improvement proposals or [RFPs](https://grants.web3.foundation/docs/rfps) (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- references to conversations you might have had related to this project with anyone from the Web3 Foundation,
- previous interface iterations, such as mock-ups and wireframes.

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. To assist you in defining it, we have created a document with examples for some grant categories [here](../docs/Support%20Docs/grant_guidelines_per_category.md). Since these will be part of the agreement, it helps to describe *the functionality we should expect in as much detail as possible*, plus how we can verify and test that functionality. Whenever milestones are delivered, we refer to this document to ensure that everything has been delivered as expected.

Below we provide an **example roadmap**. In the descriptions, it should be clear how your project is related to Substrate, Kusama or Polkadot. We *recommend* that teams structure their roadmap as 1 milestone ≈ 1 month.

> [!CAUTION]
> If any of your deliverables are based on somebody else's work, make sure you work and publish *under the terms of the license* of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! **Projects that submit other people's work without proper attribution will be immediately terminated.**

### Overview

- **Total Estimated Duration:** 2-3 months
- **Full-Time Equivalent (FTE):** 1.5 FTE
- **Total Costs:** 25000-30000
- **DOT %:** Percentage of Total Costs to be paid in (vested) DOT (≥ 50%) 

### Milestone 1 Example — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 10,000 USD
Functional MVP with credential anchoring and verification flow

Basic web dashboard (upload, verify, proof history)

API endpoints for anchor and verify

Documentation of core architecture and integration points
> [!NOTE]
> **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one.

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense. See the [delivery guidelines](https://grants.web3.foundation/docs/Support%20Docs/milestone-deliverables-guidelines#license) for details. |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. See the [delivery guidelines](https://grants.web3.foundation/docs/Support%20Docs/milestone-deliverables-guidelines#documentation) for details. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. See the [delivery guidelines](https://grants.web3.foundation/docs/Support%20Docs/milestone-deliverables-guidelines#testing-guide) for details. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language, and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) |
| 2. | Substrate module: Y | The Y Substrate module will... |
| 3. | Substrate module: Z | The Z Substrate module will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1,5
- **Costs:** 10,000 USD
Extended dashboard functionality (credential viewer, proof history with filtering).

Implementation of decentralized storage integration (e.g., IPFS) for optional off-chain proof metadata.

Expanded API endpoints:

GET /credential/{id} to retrieve credential metadata.

Enhanced verification responses with more detailed status.

Draft Substrate pallet prototype for proof anchoring to demonstrate Polkadot ecosystem integration.

Updated documentation and user guide.


## Future Plans

Financing Long-Term Maintenance and Development

We intend to finance long-term maintenance primarily through a combination of subscription-based services, ecosystem grants, and partnerships. Our initial focus is on building a sustainable revenue model via credential verification and media authenticity services, while strategically applying for ecosystem grants (e.g., Web3 Foundation, Solana, Polygon) to accelerate development without compromising ownership. As adoption grows, revenues from enterprise integrations and SaaS subscriptions will finance ongoing maintenance and expansion.

Short-Term Use, Enhancement, and Promotion

In the short term, we will prioritize completing the MVP and demonstrating clear utility for media verification and credential authentication. This includes iterative improvements to the protocol, expanding open-source components, and actively promoting the project through community engagement, developer outreach, and partnerships with early adopters. We will also showcase progress via GitHub updates, technical blogs, and social channels to build early trust and attract contributors.

Long-Term Team Plans and Intentions

Our long-term plan is to establish W3b Stitch Technologies LLC as the steward of the project, maintaining core development while fostering an open ecosystem of contributors. We intend to evolve W3b Stitch into a cross-industry trust layer for verifiable credentials and digital interactions. Over time, we plan to decentralize governance and invite community participation in shaping roadmap priorities, while ensuring professional maintenance, security audits, and integration support remain ongoing.

## Referral Program (optional) :moneybag:

You can find more information about the program [here](https://grants.web3.foundation/docs/referral-program).

- **Referrer:** Name of the Polkadot Ambassador or GitHub account of the Web3 Foundation grantee
- **Payment Address:**

## Additional Information :heavy_plus_sign: The white paper is also available on www.w3bstitch.com

**How did you hear about the Grants Program?**  Was actively seeking connection for the w3b-stitch project on github. 

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
- Previous grants you may have applied for.
