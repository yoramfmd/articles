# The Data Product Revolution in Healthcare: Why AI's Future Depends on Getting This Right

### A Perspective from the Intersection of Medicine and Technology

I've spent my career at an unusual intersection. After graduating from medical school, I transitioned into high tech, working first as an integration consultant for Microsoft, then as a Product Manager for SAP and other major technology companies. For most of my professional life, I've been enabling data to move from one place to another, building data platforms and IoT solutions that make sense of complex information flows.

Today, I work as a product manager for SAP Business Data Cloud, a state-of-the-art solution for harmonizing business data and curating semantically rich data products. This is the foundation for business AI. And among all the use cases I work with, healthcare remains the most complex and the one I'm most passionate about.

Here's what I've learned: there is no healthcare AI without data harmonization. And the best way to achieve that harmonization at scale is through data products.

### What Is a Data Product, Really?

A data product is a reusable, self-contained package that combines data with the metadata, semantics, and interfaces needed for others to reliably use it. This might sound like technical jargon, but the concept is straightforward: instead of treating data as raw material that everyone processes differently, you package it as a finished product with clear specifications.

Think of it like the difference between raw pharmaceutical ingredients and a dispensed medication. Raw ingredients require deep expertise, specialized tools, and time to compound safely, and even then results can vary. A dispensed medication combines the right active ingredients, formulated to work together, packaged in a labeled delivery form, such as an inhaler, injection, or pill, and accompanied by clear regulatory documentation covering usage, dosage, contraindications, and side effects.

Data products do the same for information. They package multiple data elements into a trusted, labeled, and discoverable unit, with clear guidance on how it should be used, monitored, and relied upon.

A complete data product includes the data itself, curated and quality-assured. It includes metadata and semantics that explain what the data means, where it came from, and how fresh it is. It provides interfaces for discovery and consumption, whether those are APIs, SQL endpoints, or feature stores. It comes with Service Level Objectives defining expectations for freshness, completeness, and accuracy. And critically, it has governance built in from the start, with access controls, de-identification rules, and auditability as core features rather than afterthoughts. Finally, it has clear ownership and ongoing maintenance, so someone is responsible when things go wrong.

But here's what distinguishes a true data product from just another dataset: data products are live, real products measured by the value they provide and their ability to attract "customers" who find them beneficial. They should be designed by domain experts but from the point of view of potential consumers. Success is measured by the value they bring and the usage they drive, not by how many SQL tables they cover or how technically sophisticated the underlying pipelines are. A data product no one uses is a failed product, regardless of its technical merit.

### Why Healthcare Needs This Now

Healthcare generates more data than almost any other industry, yet struggles more than most to turn that data into value. The practical advantages of data products address real operational problems I've watched healthcare organizations wrestle with for years.

First, data products enable faster reuse and eliminate constant reinvention. In traditional healthcare IT, teams continuously rebuild the same datasets. Five different departments each create their own version of a "patient cohort" or "quality measure" or "utilization metric," all slightly different, all maintained separately. A well-built data product serves multiple use cases simultaneously, ending this wasteful duplication.

Second, data products create clear contracts and trust. When everyone consumes the same "30-day readmission" data product with documented logic, those endless reconciliation meetings about "whose number is right" disappear. Defined meaning, lineage, and expectations reduce arguments and enable teams to focus on insights rather than data archaeology.

Third, data products enable better governance at scale. Instead of bolting on HIPAA compliance after building systems, access controls, de-identification rules, and auditability become part of the product from day one. Governance isn't a separate compliance project; it's designed into the product architecture.

Finally, data products dramatically lower integration costs over time. Traditional healthcare IT creates N-to-N point integrations where every team builds custom pipelines to every source. With data products, you publish a few stable products that many consumers can use. The integration happens once, at the product level, and the cost doesn't multiply with each new consumer.

### What Healthcare Data Products Look Like in Practice

When I talk about data products, I'm not describing abstract concepts. These are ready-to-consume building blocks that multiple applications, analysts, and machine learning models can share.

In the clinical domain, imagine a Patient 360 longitudinal timeline that combines encounters, problems, medications, labs, procedures, and imaging events into a single coherent view. Or cohort builder products that answer questions like "show me Type 2 diabetes patients with A1c above 9, on insulin, with their last visit within 6 months." Quality measure products package HEDIS measures, readmission rates, and sepsis care bundle compliance. Medication and adherence products track fills, gaps, switches, prior authorization events, and discontinuations. Care pathway and referral leakage products show where patients go in their journey and, critically, where they don't go when they should.

In the operational domain, provider directory and network adequacy products maintain who's in-network, where, and with what specialties. Risk stratification products combine clinical features with validated scores and ongoing monitoring. Utilization products track emergency department visits, imaging orders, and specialist referrals over time.

For research and analytics, organizations create what are often called "derived data products" that build on foundational clinical and claims data. These derived products link what happened to patients (from EHR data) with what it cost and what the outcomes were (from claims data). They combine information about which services patients used, how much was spent, whether their health improved, and in some cases, mortality. Disease registries serve as another category of derived research products, curating standardized datasets for specific conditions like cancer, maternal health complications, or rare diseases so researchers don't have to repeatedly clean and normalize the same information. Terminology mapping products solve a more foundational problem: translating the thousands of local codes that different hospitals use into standard vocabularies like LOINC for lab tests, SNOMED for diagnoses and procedures, and RxNorm for medications, making it possible for data from different systems to actually mean the same thing.

### The Organizations Building This Future

Several organizations are effectively productizing healthcare data into reusable assets, and their approaches reveal important patterns.

Truveta provides de-identified, standardized EHR data and is expanding linkage with closed claims, supported by tools including the Truveta Language Model. Epic Cosmos represents a collaborative dataset across participating health systems designed for discovery and point-of-care insights, with data mapped to standard ontologies such as SNOMED-CT, LOINC, RxNorm, and others whenever possible.

On the infrastructure side, Datavant focuses on privacy-preserving linkage through tokenization, enabling datasets to be matched across parties without sharing underlying identifiers. They connect more than 60 million records across payers, providers, and life sciences organizations. HealthVerity offers identity resolution and a data ecosystem aimed at research-quality real-world data with comprehensive de-identification services.

Specialty and disease-specific companies are creating domain-focused products. Flatiron Health productizes oncology real-world data with rigorous curation and compliance, positioning it as regulatory-grade for evidence generation. Tempus offers multimodal clinical and molecular data products including DNA, RNA, and pathology images for life sciences and clinical applications. Komodo Health provides patient-journey data products through their Healthcare Map and analytical tools built on top.

Broader analytics and intelligence platforms are also embracing the data product model. Innovaccer's data platform helps organizations build data products for population health and value-based care. Health Catalyst offers domain-specific products combining clinical, financial, and outcomes analytics. Clarify Health Solutions creates performance analytics products specifically for value-based care contracts.

### How Data Products Transform Healthcare IT Architecture

From my years helping organizations move data, I can tell you that data products fundamentally change what the platform needs to do. Instead of "store everything and let people figure it out," the job becomes "publish trusted, well-defined building blocks."

The integration challenges don't disappear, but they move earlier in the process and become explicit rather than hidden. Semantic interoperability matters more than ever. Cosmos data mapped to standard ontologies such as SNOMED-CT, LOINC, and RxNorm show this pattern clearly, though complete semantic harmonization often requires additional vocabularies including ICD-10 for diagnoses, CPT and HCPCS for procedures, NDC for medications, UCUM for units of measure, CVX for vaccines, and sometimes adoption of common data models like OMOP depending on whether the goal is billing, clinical interoperability, or research analytics. Without this comprehensive semantic alignment, data products from different domains can't be reliably combined, and you've just moved the integration problem rather than solving it.

Identity and linkage remain fundamentally hard. Matching patients across systems is still one of the toughest challenges in healthcare IT. Privacy-preserving linkage technologies like Datavant's tokenization approach become foundational infrastructure rather than a project-by-project problem to solve.

Consent and governance must move upstream. De-identification, permitted use, and auditability need to be part of the product definition from the start, not a separate compliance project tackled after data collection. And unstructured data adds significant complexity. Clinical notes, images, and PDFs drive enormous value but require normalization before they can be packaged as products. Many companies now lean on machine learning to curate and standardize this content.

The net effect is fewer one-off integrations but more investment in shared standards, contracts, and quality. Integration happens once at the product level rather than repeatedly for each consumer.

It's important to emphasize that data products won't cover 100% of any organization's data needs. Specific customer variations must still be supported through extensibility frameworks. Point-to-point integration remains relevant for specific scenarios like ultra-low latency data streaming where the overhead of a data product layer would compromise performance. The goal isn't to eliminate all other integration patterns, but to use data products where they provide the most value: for reusable, governed datasets consumed by multiple teams and systems.

### How Data Products Enable the Full Analytics and AI Stack

One of the most important insights from working across both clinical and technical domains is understanding how data products, analytics, planning, prediction, and AI build on each other in a coherent stack.

Data products form the governed foundation. They provide clean, documented, quality-assured datasets with clear Service Level Objectives. They serve as governed inputs to everything else in the stack. Importantly, they can also be governed outputs when machine learning model predictions are packaged as new products.

Analytics uses these data products for descriptive and diagnostic insight, answering questions about what happened and why. A dashboard consuming a "30-day readmission" product shows trends by unit. Reports using quality measure products track HEDIS performance. Operational analytics pulling from ED utilization products support capacity planning. The critical advantage is that analytics teams stop spending 80% of their time wrangling data and can focus on generating insights instead.

Planning builds on analytics by adding constraints and choosing actions within resource limits. Budget planning consumes financial data products plus historical utilization patterns. Capacity planning uses bed occupancy products and forecasted demand. Staffing plans rely on patient volume products and shift coverage requirements. Care pathway planning leverages referral leakage products to optimize patient flow.

Prediction and forecasting use data products to build models estimating future states. Patient no-show prediction consumes appointment history products. Readmission risk models train on claims plus EHR outcomes products. Demand forecasting uses historical utilization products. Cost prediction combines diagnosis, procedure, and payor products. The critical insight here is that model quality depends entirely on data product quality. The old adage "garbage in, garbage out" still applies, but with data products, you know exactly what's going in and can trust the lineage.

AI represents the broader toolbox, including prediction models, large language model workflows, automation, and decision support. AI depends on high-quality data products for both training and inference. Crucially, AI outputs should often be published back as new data products. A sepsis prediction model consuming vitals and labs products produces a "sepsis risk score" product. A clinical documentation LLM consuming a patient 360 product produces a "visit summary" product. Medication reconciliation AI consuming medication adherence products produces "intervention recommendations" as products.

This creates a virtuous cycle. Clinical data products train machine learning models. Model predictions become new data products. These enable better analytics, which improve planning, which enhance models, which refine the underlying products. Each layer depends on the quality of the layers below. Without solid data products at the foundation, everything above becomes fragile.

### The Strategic Imperative

From my experience working with organizations adopting data product thinking, the advantages manifest in several ways. Development accelerates when teams reuse products instead of rebuilding pipelines from scratch. Quality improves because domain ownership puts the people who understand the data in charge of maintaining it. Scale becomes possible as products enable parallel development without teams waiting for centralized resources. Democratization expands as well-defined products make data accessible to more users, not just specialized data engineers. Compliance becomes manageable because each product enforces governance rules while adhering to federated standards. And cost efficiency improves dramatically as you build integration once at the product level instead of N times for N consumers.

But I need to be honest about where most healthcare organizations stand today. Despite the promise, the reality is challenging. Cultural resistance runs deep because shifting from centralized IT control to domain ownership requires organizational change, not just technology deployment. Skill gaps are real as domain teams need data engineering capabilities they often lack. Integration complexity persists because healthcare's fragmented EHR landscape with Epic, Cerner, Allscripts, and others makes creating clean products genuinely difficult. Governance uncertainty remains as organizations struggle to balance domain autonomy with enterprise standards. Legacy systems don't disappear overnight, making transition strategies messy and complex. And semantic challenges persist because without shared vocabularies and ontologies, truly interoperable products remain elusive.

### The Path Forward: The Abstraction Layer Model

Having worked on data integration challenges across industries, I need to be clear about what healthcare data product transformation actually looks like. The shift will be gradual and driven primarily by the major players who currently hold the data, the EHR vendors, imaging system providers, laboratory information system companies, and claims processors, though providers, payers, and regulators also exert significant influence on how this evolves.

The transformation model centers on adding an abstraction layer on top of these existing operational systems. This layer exposes data as semantically rich data products rather than requiring direct database access or custom integration to each system. Think of it as a semantic data platform that sits between operational systems and consumers.

This is exactly the pattern SAP uses with Business Data Cloud. We curate hundreds of finance, manufacturing, logistics, and human resources data products from ERP solutions. The platform creates an abstraction layer that transforms operational ERP data into governed, reusable business data products. Organizations don't directly query SAP tables; they consume standardized data products with clear semantics, governance, and interfaces.

The same architectural approach applies to healthcare, but with FHIR as the foundational standard rather than proprietary ERP interfaces.

### How the Healthcare Model Works

**Layer 1: Operational Systems (The Source)** EHR systems, imaging platforms (PACS), laboratory information systems, pharmacy systems, claims processors, and billing systems continue operating as they do today. These are the systems of record.

**Layer 2: FHIR as the Standardized Interface** FHIR provides the standardized interface layer, offering a significant improvement over direct database access or proprietary schemas. It's not just about transport -- FHIR resources like Observation, Condition, and MedicationStatement encode clinical meaning and relationships. An LLM benefits from this normalized structure and explicit relationships rather than having to parse arbitrary database tables and figure out arcane join keys.

However, FHIR is a necessary foundation, not a complete solution. It requires profiles, implementation guides, terminology bindings, and often local extensions to work consistently across systems. AI and analytics still face challenges with optionality, inconsistent coding, missing fields, and varying implementations. FHIR provides a better starting point for building the semantic layer, but the data product platform must still handle curation, normalization, and quality assurance. Think of FHIR as necessary but insufficient, the foundation upon which semantic data products are built.

**Layer 3: The Semantic Data Product Platform (The Abstraction Layer)** This is where the transformation happens. A semantic data platform sits on top of FHIR services and operational systems. It curates semantically rich data products by combining FHIR resources with additional semantic metadata, governance policies, and quality controls.

For example, rather than just exposing raw FHIR Observation resources, the platform creates a "Diabetes Management Data Product" that provides a curated, governed, real-time patient narrative. This product combines FHIR Resources (the clinical base: observations, conditions, medications, procedures), Semantic Metadata (the meaning: standardized terminologies, clinical context, relationships), Governance and Policy (the safety: access controls, de-identification rules, consent management, audit trails), and Quality Metrics (the reliability: freshness SLOs, completeness measures, validation rules).

**Layer 4: Derived Data Products** Building on foundation products, organizations and vendors create derived products for specific purposes: readmission risk scores, quality measure calculators, population health cohorts, clinical trial matching, care gap identification.

### Who Builds What

**Major EHR and System Vendors (Epic, Cerner/Oracle, Meditech, etc.):** These vendors could provide foundational data products as part of their platform offerings. They have the operational data and increasingly expose it through FHIR APIs. The natural evolution would be packaging this as governed data products: Patient 360 longitudinal views, medication histories, problem lists, encounter summaries, lab result timelines. However, today most vendors still expose raw FHIR APIs rather than true data products with Service Level Objectives, quality metrics, and built-in governance. This represents an opportunity and a likely direction, though it's not yet the predominant reality.

**Healthcare Data Platform Vendors:** Companies building the abstraction layer itself. These platforms ingest from multiple source systems via FHIR and other standards, apply semantic harmonization, and curate standardized data products that work across different EHR vendors.

**Specialized Data Product Providers:** Companies like Datavant, Truveta, Komodo Health, and Flatiron create specific high-value products: privacy-preserving linkage, real-world evidence datasets, disease registries, market intelligence.

**Healthcare Organizations (Internal Teams):** Health systems create organization-specific based and derived products: custom quality measures, local utilization patterns, specific population cohorts, institutional risk models. These teams become product managers and data engineers, not infrastructure builders. They consume foundation products from vendors and create tailored analytical products on top.

### The Gradual Transition

This isn't a rip-and-replace transformation. Organizations gradually start consuming FHIR APIs from existing systems rather than direct database access, implement a semantic data platform that harmonizes data from multiple sources, catalog and govern the first data products (often Patient 360, quality measures, cohort builders), build derived products for specific analytical and AI use cases, expand consumption as more teams adopt products instead of custom integration, and partner with vendors who provide specialized products rather than building everything internally.

The operational systems stay in place. The transformation happens in the abstraction layer above them, where raw operational data becomes semantically rich, governed, reusable data products.

### Why This Model Enables Healthcare AI

This architecture addresses the fundamental problem that has plagued healthcare AI: fragmented, inconsistent, ungoverned data. When an AI model trains on a well-defined data product with documented semantics, clear lineage, and quality metrics, it has a foundation for reliable performance. When predictions are packaged as new data products with monitoring and governance, clinicians can trust them.

FHIR provides a standardized starting point with semantic structure. The data product platform adds the essential curation, normalization, governance, and quality layer that transforms raw FHIR resources into truly AI-ready data. Together, they create the foundation that healthcare AI requires but has rarely had access to.

The shift from raw FHIR resources to semantically rich, governed data products isn't just about better data management. It's about making healthcare data reliable and trustworthy enough for AI at scale.

### Why This Matters for Healthcare AI

My 20 years work with data has convinced me that data harmonization through data products isn't just a better architectural pattern. It's the only path to healthcare AI that actually works at scale. Every AI initiative I've seen struggle in healthcare traces back to data foundation problems. Models trained on inconsistent data. Predictions that can't be trusted because no one knows the lineage. AI recommendations that clinicians ignore because the underlying data quality is questionable.

Data products solve this by making data quality, lineage, semantics, and governance explicit and verifiable. When an AI model trains on a well-defined data product with documented SLOs, you know what went into that model. When predictions are packaged as new data products with their own quality metrics and monitoring, you can trust them in clinical workflows. This isn't theoretical. It's the difference between AI that gets deployed versus AI that gets abandoned after the pilot phase.

The shift from centralized data warehouses to distributed, domain-owned, AI-ready data products represents a fundamental rethinking of how healthcare manages information. It moves us from data as exhaust to data as product, from central control to distributed ownership, from IT building everything to domains owning their data, from analytics as an afterthought to analytics-ready by design, from N-to-N integrations to publish once and consume many, and from governance bolted on later to governance built in from the start.

The organizations that master data products will have decisive advantages in the AI era: faster insights, better models, more personalized care, and operational efficiency that centralized architectures simply cannot match. The question isn't whether healthcare will move to data products. It's whether your organization will lead this transformation or be left managing monolithic warehouses while competitors race ahead with federated, semantically rich, AI-ready data products.

The future of healthcare data isn't centralized. It's distributed, product-oriented, and governed at scale. And from where I sit, working at the intersection of clinical medicine and enterprise data platforms, I can tell you: that future is already here. The only question is how quickly healthcare will embrace it.
