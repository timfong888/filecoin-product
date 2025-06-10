# Filecoin Product Strategy - Appendix

## Appendix A: AI/ML Ops Lifecycle Analysis

|  | Data Collection & Ingestion | Data Preparation & Preprocessing | Model Training | Evaluation & Validation | Model Deployment | Monitoring & Retraining |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Core Job** | Massive raw datasets that need long-term, potentially cost-effective storage before processing. | Cleaning, transforming, normalizing, and augmenting data. | Models are trained iterating over large data volumes. Model artifacts. | Assessing the trained model's performance against validation datasets. | Serve predictions in a production environment | Detecting drift, logging predictions and inputs, and triggering retraining. |
| **Filecoin Thesis** | Decentralized sources and need for data integrity at ingestion | Cryptographic proofs guarantee the dataset exists and hasn't been lost -- reproducibility and auditing. | Referencing the exact model version or checkpoint used in an experiment. | Guaranteeing the integrity and verifiable existence of the exact dataset used for evaluation via CIDs and proofs | The CID acts as a globally unique, immutable identifier for that specific production model. | Immutable model performance logs and retraining triggers |
| **Open Source** | Hugging Face datasets<br>Kaggle | Ray<br>Dask | Ray<br>MLflow | Weights & Biases<br>MLflow | Ray Serve<br>Seldon | Ray<br>MLflow |

## Appendix B: Web3 Market Segment Analysis

| Segment | JTBD | Unique FIL Opportunities |
| :---- | :---- | :---- |
| Wallets | Onboard more users; deliver value (e.g. easy swaps); differentiate in a sea of options | Decentralized backup/recovery; Cross-chain data portability; Verifiable transaction history |
| Chains | Onboard more developers; launch dApps with high on-chain activity; Data archival for compliance | Immutable state snapshots; Verifiable data availability; Cost-effective long-term storage |
| Protocols / DeFi | Increase users and liquidity. | Verifiable off-chain data feeds; Immutable audit trails; Decentralized oracle data storage |
| CEX/DEX | Onboard more traders and increasing trading activity per trader. | Verifiable trade history; Compliance data storage; Decentralized order book backups |
| Web3 Dev Platforms | Attract, activate and retain more developers | Decentralized CI/CD artifacts; Verifiable code repositories; Immutable deployment records |

## Appendix C: Market Prioritization Analysis

| Segment | Degree Underserved[^7] | Ability to Pay | Ease of GTM (Access + Time) | TAM | Market Fit |
| :---- | :---- | :---- | :---- | :---- | :---- |
| AI/ML Ops | Medium | High | S | L | Medium |
| Web3 | High | Medium | L | S | High |
| Web2 Regulated | Low | High | M | L | Low |

**Legend:**
- S = Short-term (< 12 months)
- M = Medium-term (12-24 months)  
- L = Long-term (24+ months)

## Appendix D: Strategic Roadmap Timeline

|  | Now | Medium | Future |
| :---- | :---- | :---- | :---- |
| Web3  | Infra / Marketplaces<br>IPFS providers<br>Active FIL L2 | Cross-chain integrations<br>DeFi data storage | L2 - Blockchain Analytics<br>Decentralized identity |
| Web2 - Regulated | Cloud Marketplaces | Storage VAR<br>Compliance solutions | Enterprise data governance<br>Regulatory reporting |
| AI/ML | Open Source Projects | Filecoin Inference (stand alone or support existing services) | AI model versioning<br>Decentralized compute |

## Appendix E: Web2 Market Analysis

| JTBD | Features / Attributes | Potential Segment |
| :---- | :---- | :---- |
| I face competitive margins and must reduce storage costs without sacrificing elasticity | Cheaper | Archive Service providers serving AWS/Azure Marketplace; Storage VAR/MSPs |
| I need guarantees of both the data's durability and immutability because I and others run series of experiments or jobs over the data | Immutability<br>Cryptographically durable | Open data research (no privacy requirements) - climate, genomics, astrology, physics, epidemiology, etc<br>IoT data that's public, open |
| I need to comply with regulations (health, finance, security logs) that have legal requirements around data retention, retrieval, **data locality** | Immutability<br>Cryptographically durable<br>Geographic controls[^6]<br>Provenance of storage | Healthcare, finance, government around long-term retention documents or log files. May be particular to a geographic regime. |
| I need to spin up storage close to users or devices and existing edge services are limited (e.g. not close enough, not in the region I care about). Ideally local where data is produced; or zero-cost egress. | Geographic controls | Region-specific businesses (but likely still need one or more of the above features). E.g. games, AI |

---

[^6]: While it seems a decentralized network could incentivize geo-targeted and enable geo-fencing on storage, it can't do this now; and while there had been some requirements on this (from experience at Cloudflare and my own start-up) on data locality restrictions, we need to see if this is a real market or real legislation (the way GDPR/SOC2 etc created start-ups).

[^7]: **Degree Underserved:** this definition is both broad yet precise; the ideal segments aren't being served by incumbents for one of several common reasons, including: price, missing core requirement that can't easily be built by incumbents; the best scenario would be a case where there's a common trade-off that is broken due to innovation (and I'm not aware of one);
