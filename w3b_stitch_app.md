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
- Names of team members: potential dev companies are on stand-by awaiting funding. These include Cowchain, Node Central, etc. I also have independent contractors higly interested such as workflow automation experts.

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


Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/rocketjays-cmyk


### Team LinkedIn Profiles (if available)

- www.linkedin.com/in/w3bstitch



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
- **DOT %:** 50% DOT / 50% USDC 

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
| **0a.** | License | Apache 2.0. |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how to spin up a Substrate node, deploy the included pallets, and send test transactions, which will demonstrate the new functionality. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests (>80% coverage) to ensure functionality and robustness. In the guide, we will describe how to run these tests and interpret results. |
| **0d.** | Docker | We will provide Dockerfile(s) that can be used to spin up a local chain with the new pallets included, enabling reproducible testing of all milestone functionality. |
| **0e.** | Article | We will publish a **technical article/workshop** that explains the purpose of W3b Stitch, the implementation of the delivered pallets (anchoring, credential provenance, reputation), and how developers and partners (media verification platforms, credential issuers) can integrate with it. This will be published on Medium and the Web3 Foundation forum to reach both the developer community and ecosystem stakeholders. |
| # | Deliverable | Specification |
|---|-------------|---------------|
| 1. | Substrate module: **pallet_tdr_anchor** (Trust Delta Anchoring) | We will implement a pallet that anchors content/credential hashes and Verifiable State Bundle (VSB) commitments. **Functionality:** (a) extrinsics: `anchor_hash(origin, hash, cid, tags)`, `anchor_vsb(origin, merkle_root, bundle_size)`, `link_derivation(origin, parent_anchor_id, child_anchor_id)`, `verify_membership(origin, merkle_root, leaf, proof)`; (b) storage for Anchors, VSBs, and Parent↔Child links; (c) events for every anchor/verification; (d) on-chain verification of Merkle proofs; (e) weights/benchmarks and >80% unit/integration test coverage; (f) README + rustdocs + example usage in a node-template runtime. |
| 2. | Substrate module: **pallet_capm_credentials** (Credential Authentication & Provenance) | We will implement a pallet to manage issuers, schemas, and credential provenance. **Functionality:** (a) issuer registry (DID → keys/permissions); (b) schema registry (schema hash/CID); (c) credential anchoring with optional revocation via Merkle accumulator; (d) extrinsics: `register_issuer`, `register_schema`, `anchor_credential(origin, cred_hash, issuer, schema_ref)`, `revoke_credential(origin, cred_id)`, `verify_credential(origin, cred_hash, proof?)`; (e) events + queries; (f) weights/benchmarks, >80% test coverage, README/rustdocs. |
| 3. | Substrate module: **pallet_dirm_reputation** (Decentralized Identity & Reputation / Trust Deltas) | We will implement a pallet to record **Trust Delta Records (TDRs)** and compute deterministic reputation scores. **Functionality:** (a) storage for TDRs keyed by subject DID/resource ID; (b) signal types: `endorse`, `dispute`, `challenge`, `resolve` with configurable weights; (c) extrinsics: `submit_signal(origin, subject, signal_type, ref_anchor)`, `set_weights(origin, weights)` (governed), `recompute_score(origin, subject)`; (d) on_initialize hook for scheduled recomputations; (e) events + query APIs; (f) weights/benchmarks, >80% tests, README/rustdocs. *(Note: offchain worker hooks for IPFS/Filecoin proof lookups will be stubbed in M1 and fully wired in a later milestone.)* |
| 4. | Substrate chain | We will deliver a **custom Substrate chain runtime** that integrates the three pallets (`pallet_tdr_anchor`, `pallet_capm_credentials`, and `pallet_dirm_reputation`). **Functionality:** (a) modules interact so that credential anchors (CAPM) and content anchors (TDR) feed into reputation scoring (DIRM); (b) runtime configuration to link pallets via events/hooks; (c) chain spec + genesis configuration; (d) end-to-end demo scenario (anchor → credential → trust delta → reputation recompute) using test accounts; (e) >80% integration test coverage and benchmarks. |
| 5. | Library: w3bstitch-js | We will deliver a **JavaScript/TypeScript library** (`w3bstitch-js`) that wraps RPC calls to our Substrate node and exposes high-level developer functions. **Functionality:** (a) connect to chain endpoint via Polkadot.js API; (b) functions like `anchorHash()`, `verifyAnchor()`, `registerIssuer()`, `anchorCredential()`, `submitSignal()`, `getReputationScore()`; (c) examples + inline docs; (d) published as an NPM package; (e) developer guide showing usage in dApps and credential issuers’ systems. |
| 6. | Smart contracts: ink! trust adapters | We will deliver a set of **ink! smart contracts** that provide lightweight anchoring and verification adapters for environments where full Substrate pallets are not deployed. **Functionality:** (a) contract for anchoring/verifying hashes on-chain (bridging to pallet_tdr_anchor where available); (b) contract for credential revocation/verification; (c) contract for emitting trust delta events usable by off-chain indexers; (d) full unit tests in ink!; (e) deployment + integration guide. |

### Milestone 2 — 

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

- **Referrer:** N/A
- **Payment Address:** N/A

## Additional Information :heavy_plus_sign: The white paper is  available on www.w3bstitch.com

**How did you hear about the Grants Program?**  Was actively seeking connection for the w3b-stitch project on github. 

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done: Repo for w3bstitch is open and will be  updated soon.
- If there are any other teams who have already contributed (financially) to the project: N/A
- Previous grants you may have applied for: Currently pursuing multitude of various grants, and partnerships though unrelated.

