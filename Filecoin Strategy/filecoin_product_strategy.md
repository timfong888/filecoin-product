### Document Information

| Author | Product Strategy Team |
| :---- | :---- |
| Last Update | June 10, 2025 |
| State | Draft - Under Review |

### 

### Mission

"To create a decentralized, efficient, and robust foundation for humanity's information."

### Protocol Vision

*Empower developers to build and scale decentralized applications by providing simple, integrated access to Filecoin's verifiable storage, compute, payments, and programmability.*

### Problem Statements

**Current PoRep Implementation**: The protocol currently operates as archive storage, limiting real-time access patterns and creating friction for applications requiring frequent data retrieval.

**On-ramp Misalignment**: Existing on-ramps to the Filecoin network are not aligned with protocol incentives, creating barriers to adoption and suboptimal user experiences.

**Storage Usability Gap**: Customer expectations for storage (simple put/get operations with reliable retrieval) are not met by current protocol implementation, hindering mainstream adoption.

**IPFS Positioning Ambiguity**: Unclear relationship and value differentiation between Filecoin and IPFS creates market confusion despite IPFS having established product-market fit.

### Superpowers

What are the differentiated attributes of the Filecoin Network that **are in demand?**

Each property or set of properties should deliver value to paying customers that is not available from other providers **and** is something that they **actually** need and **want to pay for.** 

Getting the taxonomy precise will be important.  For example, "Verifiable" has been often used (not just in Filecoin, but in the web3 industry, in general); but what exactly is verified (by whom, by what criteria, for what purpose)?

### Typical Must Haves

Systems often compete to meet broad user non-functional requirements such as:

1. Reliability  
2. Latency  
3. Cost  
4. Security  
5. Ease-of-use

Centralized solutions not only meet most user expectations, they have an advantage over distributed systems. Keeping this in mind in terms of target markets.

Here are some hypotheses (with footnotes for coloring) of differentiated properties for Filecoin:

- Cheaper (data at rest and transit)[^1]  
- Cryptographically proven durability[^2]  
- Immutability (via CID)  
- Provenance of storage[^3]  
- Crypto-economically Incentivized resourcing (e.g. geography)[^4]

### Feature Forward Potential Customers

Starting from the features and going forward to users, here are potential customers derived from hypothesized jobs to be done (JTBD).  

The capabilities here assume that there is **not** a significant trade-off for the typical must-haves discussed above.

#### Web2 Markets

Web2 markets present limited immediate opportunities but several longer-term possibilities worth exploring through targeted partnerships and marketplace approaches.[^5]

**Cost-sensitive segments** like archive service providers and storage VARs serving AWS/Azure marketplaces could benefit from Filecoin's cost advantages, though the margin must be significant enough to justify switching costs.

**Research and compliance sectors** represent more compelling opportunities. Open data research in climate, genomics, and epidemiology requires both immutability and cryptographic durability for reproducible science. Similarly, regulated industries in healthcare, finance, and government need long-term retention with data locality controls and provenance guarantees that Filecoin's decentralized architecture can uniquely provide.[^6]

**Edge and regional applications** may emerge where existing cloud services have geographic limitations, particularly for gaming and AI applications requiring local data production and zero-cost egress.

While these represent small bets requiring careful market development, they establish foundation use cases that could scale with protocol improvements.

#### AI/ML Ops Markets

AI/ML operations represent the most compelling long-term opportunity, requiring a discovery-driven approach focused on open source community partnerships, particularly with projects like Ray.

The AI/ML lifecycle presents multiple integration points where Filecoin's unique properties address real pain points. **Data integrity and reproducibility** are critical challenges as teams struggle with dataset versioning, model artifact management, and audit trails for regulatory compliance. Filecoin's cryptographic proofs and immutable CIDs provide verifiable guarantees that datasets and models haven't been corrupted or lost.

**Partnership opportunities** exist across the ecosystem: Hugging Face and Kaggle for dataset storage, Ray and Dask for distributed processing, MLflow for experiment tracking, and Weights & Biases for model monitoring. These integrations could position Filecoin as infrastructure for reproducible AI research and production deployments.

The market size and growth trajectory make this too significant to ignore, but success requires deep technical integration rather than surface-level storage solutions. (See Appendix A for detailed lifecycle analysis.)

#### Web3 Markets

Web3 represents our most strategically aligned opportunity despite being smaller than Web2 markets. The shared decentralization ethos provides natural affinity, but ideological alignment alone is insufficient—we must deliver concrete utility that meets performance and usability requirements.

**Cross-ecosystem opportunities** exist where Filecoin can solve real infrastructure problems. Wallets need decentralized backup and cross-chain data portability. Layer 1 and Layer 2 chains require cost-effective data availability and immutable state snapshots for compliance. DeFi protocols struggle with verifiable off-chain data feeds and immutable audit trails for regulatory requirements.

**Developer infrastructure** presents immediate opportunities through decentralized CI/CD artifacts, verifiable code repositories, and immutable deployment records that Web3 development platforms desperately need.

The strategic imperative is finding use cases that span the entire Web3 ecosystem rather than targeting individual segments. Our name recognition and existing relationships provide significant advantages, but execution must focus on solving genuine technical problems rather than relying on philosophical alignment. (See Appendix B for detailed segment analysis.)

### Market Prioritization

Our analysis reveals three distinct opportunity tiers requiring different strategic approaches and timelines.

**Web3 emerges as the highest-priority segment** despite its smaller total addressable market. The segment is highly underserved by existing solutions, shows strong market fit with our capabilities, and offers manageable go-to-market complexity through existing relationships. While ability to pay is moderate, the strategic value of establishing Web3 dominance justifies prioritization.

**AI/ML Ops represents the largest long-term opportunity** with high ability to pay and medium market fit, but requires significant discovery and technical integration work. The segment is moderately underserved, suggesting competitive solutions exist, making differentiation critical.

**Web2 Regulated markets rank lowest** despite high ability to pay and large market size. These segments are minimally underserved by existing enterprise solutions, indicating strong incumbent positions and high switching costs that make market entry challenging.

This prioritization suggests a phased approach: establish Web3 market leadership while building AI/ML partnerships, with Web2 regulated markets as longer-term expansion opportunities. (See Appendix C for detailed market analysis.)

### Strategic Roadmap

Our roadmap reflects a hypothesis-driven approach that will evolve as we gather market signals and validate assumptions across three parallel tracks.

**Immediate focus (Now)** centers on Web3 infrastructure and marketplaces, leveraging existing IPFS provider relationships and active Layer 2 integrations. Simultaneously, we'll initiate AI/ML open source partnerships while exploring Web2 cloud marketplace opportunities.

**Medium-term expansion** builds on early wins with cross-chain integrations and DeFi data storage solutions in Web3, while developing Filecoin inference capabilities for AI/ML workloads. Web2 efforts will focus on storage VAR partnerships and compliance-focused solutions.

**Future opportunities** include Layer 2 blockchain analytics and decentralized identity for Web3, AI model versioning and decentralized compute for AI/ML, and enterprise data governance solutions for regulated Web2 markets.

This phased approach allows us to validate market assumptions while building capabilities that compound across segments. Success in Web3 infrastructure provides credibility for AI/ML partnerships, which in turn enables enterprise Web2 conversations. (See Appendix D for detailed roadmap timeline.)

[^1]:  Are these apple to apple comparisons, and are these with the subsidy or without?  Is cheaper only against hyperscaler clouds versus a client standing up their own data center (this would not be an apples-to-apple because it is CapEx vs OpEx, but still, we should be precise on the comparison set.  Based on [this report](https://docs.google.com/spreadsheets/d/1BFGVuYUxayafC98wp_styMQdlKgCsaJNhF0aaHhihGQ/edit?gid=1995087444#gid=1995087444), I do not believe that the cost advantage is significant enough as the basis for PMF, but there could be very specific niches.

[^2]:  This provides a guarantee that the data has, in fact, been stored; retrievability is still trusted, but at least there's proof the data exists and has not been lost.

[^3]:  I specified provenance of storage because the more broadly used term of provenance has other implications regarding identification of who the SP is, since in regulatory environments, provenance extends to jurisdictions as well as certifications.  So we need clarity on what precisely is meant.

[^4]:  The decentralization implies that there can be geographic incentivization; however, similar to provenance, the characteristics that have been incentivized need to be specified and verified -- and that doesn't appear to be the case, either.  But it could be possible, and is generally a property of decentralized systems.

[^5]:  This is not exhaustive (I'm writing it in a few hours); but I think it does a pretty good job of identifying the potential space.

[^6]:  While it seems a decentralized network could incentivize geo-targeted and enable geo-fencing on storage, it can't do this now; and while there had been some requirements on this (from experience at Cloudflare and my own start-up) on data locality restrictions, we need to see if this is a real market or real legislation (the way GDPR/SOC2 etc created start-ups).

[^7]:  **Degree Underserved:** this definition is both broad yet precise; the ideal segments aren't being served by incumbents for one of several common reasons, including: price, missing core requirement that can't easily be built by incumbents; the best scenario would be a case where there's a common trade-off that is broken due to innovation (and I'm not aware of one);
