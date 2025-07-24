---
title: Applying TOGAF to a Real‑World Company
url: /guides/applying-togaf-realworld
date: '2025-06-24'
weight: 2000
book_section: Togaf
---

<span style="color:red">*Note [WIP]:* Though this article looks like it's focused purely on TOGAF, intention here is to emphasise the need for using Enterprise Architecture of whichever medium to save time for Organisations</span>

1 Company context and typical problems
--------------------------------------

Your company has multiple technology and support departments – *Enterprise Technology* (split into *Software Engineering* and *DevOps*), an *Enterprise Applications* team (Oracle ERP, Salesforce CRM, etc.), a *Data Analytics* group (data warehousing and analytics), *Quality Assurance*, *Project Management Office (PMO)*, *Human Resources* and an *Enterprise Excellence/R&D* department. Each group has its own systems and processes. Without a unifying enterprise architecture framework the following challenges commonly emerge:

*   **Siloed initiatives and poor business buy‑in.** Many EA teams complain that “the rest of the business appears to be uninterested.” Without executive sponsorship or departmental engagement, initiatives stall [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them). People see enterprise architecture as a bureaucratic exercise [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them) outdated or bureaucratic rather than something that supports business outcomes.
    
*   **Fragmented data and tools.** When each department buys its own tools, the organization ends up with a patchwork of siloed data sources. Modern EA teams note that fragmented tools and data make it nearly impossible to obtain a clear, up‑to‑date picture of the enterprise landscape [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    
*   **Difficulty demonstrating ROI.** Because benefits are often indirect (e.g., reduced redundancy or better decisions), EA efforts can lose funding [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    
*   **Lack of strategic alignment.** If architecture work is not linked to business objectives, it risks focusing on technology for technology’s sake and losing sight of outcomes [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    

These issues manifest in everyday pain points: *duplicate employee data across HR and PMO systems*, *manual data movement between the ERP and analytics teams*, *inconsistent definitions of customers and products*, *conflicting technology stacks in different departments and no single view of projects and resource availability*. Such fragmentation increases costs and slows innovation.


Redundant Work Without EA (Enterprise Architecture): Realistic Scenarios
-------------------------------------------------

### 1\. Software Engineering (SE), Enterprise Excellence (EE), and Data Analytics (DA) All Build the Same POC

**Scenario:**

*   The SE team experiments with a new streaming data platform like Apache Kafka for real-time processing.
    
*   Unaware of this, the Enterprise Excellence (EE) team runs a parallel Proof of Concept (POC) with Amazon Kinesis for R&D.
    
*   Simultaneously, the DA team prototypes a third solution using Google Pub/Sub to integrate real-time dashboards.
    

**Problem:**

*   Three teams ran POCs for the same capability — *real-time data streaming* — with *zero coordination*.
    
*   No one knew the others were doing similar work. Each spent time, money, and effort duplicating evaluations, licenses, and engineering hours.
    

**Impact:**

*   💸 Wasted cloud credits and duplicate consulting spend
    
*   🧩 Confusion later during integration — different tech stacks
    
*   🧠 Lost opportunity to share learnings or consolidate findings
    
*   📉 Low credibility with leadership when the redundancy is discovered
    

**What a Centralized EA Function Would Do:**

*   Maintain a *central innovation registry*
    
*   Run coordinated evaluations with cross-functional teams
    
*   Define *standard patterns* and preferred tech
    
*   Ensure one vetted solution becomes the enterprise standard
    

### 2\. DevOps Team Builds CI/CD from Scratch, QA Team Uses a Different Stack

**Scenario:**

*   The DevOps team implements GitHub Actions + Terraform to deploy microservices.
    
*   Meanwhile, the QA team sets up a Jenkins + Ansible stack for test environments, completely disconnected.
    
*   Both automate similar pipelines but use incompatible tools and scripts.
    

**Problem:**

*   Duplicate tooling = duplicated training, duplicated maintenance
    
*   Pipelines cannot be reused across teams
    
*   Security policies and audit trails become fragmented
    

**Impact:**

*   🚧 Slower onboarding for developers and testers
    
*   🔒 Security inconsistencies across environments
    
*   📊 No centralized view of deployment status or audit trails
    

**What EA Would Do:**

*   Define *standard DevOps architecture* for the org
    
*   Facilitate governance around CI/CD patterns
    
*   Consolidate pipelines into reusable modules across departments
    

### 3\. 📈 Multiple Teams Buy Their Own BI or Analytics Tools

**Scenario:**

*   The PMO uses Power BI dashboards for reporting.
    
*   HR builds their own visualizations in Zoho Analytics.
    
*   DA runs Snowflake-based analytics integrated with Tableau.
    
*   Leadership asks for “a unified view of enterprise KPIs” — but it doesn’t exist.
    

**Problem:**

*   No consistent metric definitions
    
*   Data duplicated or inconsistent across platforms
    
*   Costs balloon due to overlapping licenses and support
    

**Impact:**

*   🚫 Executives get conflicting reports
    
*   💵 Budget overruns on tool proliferation
    
*   🔁 More effort needed later to consolidate into a data warehouse
    

**What EA Would Do:**

*   Define an *enterprise-wide analytics roadmap*
    
*   Standardize BI tools and reporting layers
    
*   Drive governance for metric definitions, data lineage, and access control
    

### 4\. POCs Without Strategic Alignment = No Business Impact

**Scenario:**

*   EE runs an AI model POC for predicting customer churn.
    
*   DA has already done something similar, but for operational risk.
    
*   SE also explored an ML feature, but focused on product recommendation.
    

**Problem:**

*   No shared goals, no architectural alignment
    
*   Great ideas — but no production follow-through
    
*   Nobody plans for integration, data security, or scale
    

**Impact:**

*   ⏳ Valuable ideas stuck as isolated prototypes
    
*   ⚖️ Tools picked without legal or compliance review
    
*   ❌ Nothing reusable across teams or repeatable
    

**What EA Would Do:**

*   Tie all POCs to *clear business capabilities and value streams*
    
*   Create enterprise innovation frameworks with *review checkpoints*
    
*   Guide which POCs move to production and under what governance


2 Why adopt TOGAF?
------------------

**TOGAF** (The Open Group Architecture Framework) is a widely used enterprise architecture (EA) framework that helps organisations align their IT landscape with business goals. Recent guidance emphasises that TOGAF is not just a governance model; it provides principles, best practices and an *Architecture Development Method (ADM)* to iteratively develop and maintain an enterprise architecture [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf). 

Key benefits include:

*   **Streamlined IT operations.** By clearly framing processes, roles and assets, TOGAF improves understanding of how things work and helps reduce redundancy in systems [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    
*   **Better strategic alignment.** TOGAF bridges the gap between IT and business by providing a framework for aligning IT strategies and capabilities with business goals [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    
*   **Improved interoperability.** Mapping the enterprise reveals where systems are siloed and allows teams to set interoperability standards [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    
*   **Standardised architectural framing.** Using a common framework makes it easier to work with consultants and reuse established patterns [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    
*   **Integrated governance and risk management.** TOGAF embeds governance practices to help identify and manage risks associated with IT architecture [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    

3 Selected use case – integrated customer and product data
----------------------------------------------------------

To illustrate how TOGAF can solve real business problems, consider a **Unified Customer and Product Data** initiative. Today, customer and product information exists in multiple systems:

1.   *Salesforce CRM* holds customer interactions and pipeline data.
2.  *Oracle ERP* maintains orders, product catalogue and financial data.
3.  *HR and PMO systems* store employee and project information for resource allocation.
4.  *Data Warehouse/Data Lake* stores analytical data used by the Data Analytics team.

Without an enterprise architecture, these systems are integrated via ad‑hoc scripts and spreadsheets. HR might enter employee skills in one tool while PMO enters resource assignments in another, causing conflicting information. The Data Analytics team receives periodic extracts instead of real‑time feeds. Departments duplicate data structures, leading to inconsistent definitions of customers, products or projects.

The goal of the use case is to create a single view of customers and products, enable cross‑departmental reporting (e.g., product profitability, customer lifetime value, resource utilisation), and provide near‑real‑time data feeds for analytics. The following sections show how TOGAF’s domains help achieve this.

4 Applying TOGAF’s architecture domains
---------------------------------------

### 4.1 Business Architecture

The *business architecture* domain focuses on the organization’s motivations, operations and alignment with strategy [(togaf.visual-paradigm.com)](https://togaf.visual-paradigm.com/2025/02/18/comprehensive-guide-to-architecture-domains-in-togaf). For the unified data initiative:

*   **Identify business capabilities and processes.** Map the capabilities of each department (e.g., sales operations, order processing, data analytics, project management, HR hiring/training, quality assurance, innovation/R&D). Create a capability map to understand overlaps and dependencies.
    
*   **Define strategic objectives and performance metrics.** For example, reduce time‑to‑report by 50 %, improve resource utilisation by 20 % and increase customer satisfaction scores. Align these objectives with enterprise goals (growth, cost optimisation, innovation).
    
*   **Stakeholder engagement.** Address the lack of business buy‑in by involving executives from sales, operations, HR and PMO at the start. Translate EA activities into tangible outcomes such as faster on‑boarding of new products and improved decision‑making [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    

### 4.2 Data Architecture

**Data architecture** deals with the structure of data assets, governance and integration [(togaf.visual-paradigm.com)](https://togaf.visual-paradigm.com/2025/02/18/comprehensive-guide-to-architecture-domains-in-togaf). In this use case:

*   **Develop a common data model.** Harmonise customer, product, order and project data across systems. The simplified entity–relationship model below illustrates key entities such as *Customer*, *Product*, *SalesOrder*, *OrderItem*, *Project*, *Employee* and *ResourceAllocation*. It defines primary keys (PK), foreign keys (FK) and relationships to ensure consistency across applications.
    
*   **Define data governance policies.** Establish data quality standards, ownership and stewardship. For example, the sales department owns customer data, while product management owns product definitions. Data stewards enforce naming conventions and manage metadata.
    
*   **Plan for data integration and lineage.** Decide how data moves from operational systems (Salesforce, Oracle ERP, HR) into the data warehouse and analytics platform. Use an integration layer to expose APIs and implement ETL/ELT pipelines. Ensure traceability so analysts understand the origin and transformation of each data element.
    
*   **Ensure regulatory compliance.** By documenting data flows and applying security controls, the organization meets legal obligations and protects sensitive information [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf).
    

### 4.3 Application Architecture

The **applications architecture** describes the behaviour of applications and services that support business processes [(togaf.visual-paradigm.com)](https://togaf.visual-paradigm.com/2025/02/18/comprehensive-guide-to-architecture-domains-in-togaf). For our use case:

*   **Inventory existing applications.** Document the functions provided by Salesforce (CRM), Oracle ERP (order management, product master), HR and PMO systems (employee and project management), QA tools and analytics platforms. Identify overlapping functionality (e.g., duplicate resource scheduling features) and opportunities to rationalise.
    
*   **Design integration patterns.** Introduce an *Integration Layer* using an API Gateway or Enterprise Service Bus (ESB). Each system exposes APIs to the integration layer, which manages authentication, orchestration and protocol translation. This reduces point‑to‑point integrations and ensures loose coupling.
    
*   **Plan application services.** For example, a *Customer Service* retrieves customer details by combining CRM and ERP data, while a *Resource Allocation Service* unifies project assignments across PMO and HR systems. A *Reporting Service* fetches curated data from the analytics platform for dashboards.
    
*   **Define non‑functional requirements.** Consider availability, scalability and performance. Adopt service‑oriented or microservice principles to enable independent deployment and scalability.
    

### 4.4 Technology Architecture

The **technology architecture** domain outlines the infrastructure required to support applications [(togaf.visual-paradigm.com)](https://togaf.visual-paradigm.com/2025/02/18/comprehensive-guide-to-architecture-domains-in-togaf). Key activities include:

*   **Assess current infrastructure.** Catalog servers, databases, networks and cloud services used by each department. Identify obsolete components and areas where cost can be optimised (e.g., decommission redundant servers, consolidate environments).
    
*   **Define target infrastructure.** For this use case, deploy the integration layer on a scalable platform (e.g., containers or managed integration services), adopt a secure API gateway, implement data pipelines (streaming and batch) and provision a data lake/warehouse environment with sufficient compute and storage.
    
*   **Set technology standards.** Specify approved platforms (e.g., PostgreSQL for the data warehouse, AWS/Azure integration services), interoperability protocols (REST, GraphQL, messaging), security standards (encryption, access control) and disaster‑recovery plans.
    
*   **Plan migration.** Use the ADM’s Phase F to create a migration roadmap that sequences transitions from legacy batch extracts to modern API‑driven integration, minimises disruption and allows incremental adoption [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf#).
    

## 5. Executing the Initiative with TOGAF ADM

TOGAF’s Architecture Development Method (ADM) provides an iterative cycle to develop and maintain enterprise architecture ([source](https://www.ardoq.com)).

| **ADM Phase**                       | **Key Activities for the Unified Data Initiative**                                                                                                                                               |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Preliminary**                    | Establish the EA capability, define architecture principles (e.g., “single source of truth for customer data”), adapt TOGAF to the organisation and secure sponsorship.                         |
| **Phase A – Architecture Vision**  | Define the vision (“a unified, real-time customer and product data platform”), identify stakeholders (Sales, Finance, HR, PMO, Data Analytics), outline expected benefits and get approval.     |
| **Phase B – Business Architecture**| Map current and target business processes; create capability maps; identify gaps; model future state processes that leverage unified data.                                                      |
| **Phase C – Information Systems Architecture** | Develop Data and Application architectures. Define the common data model, data governance policies, application services, and integration patterns.                                  |
| **Phase D – Technology Architecture** | Specify the technology platforms, infrastructure, and standards needed. Evaluate options (on-premises vs. cloud, integration technologies) and create a target technology model.         |
| **Phase E – Opportunities & Solutions** | Identify implementation projects (e.g., API gateway deployment, data warehouse modernisation), prioritise quick wins, and estimate costs.                                             |
| **Phase F – Migration Planning**   | Create a roadmap to move from the fragmented “as-is” environment to the target architecture. Sequence projects, define work packages, assign responsibilities, and manage dependencies.        |
| **Phase G – Implementation Governance** | Oversee execution; ensure projects comply with architecture standards and guidelines. Monitor KPIs to track benefits and make adjustments.                                       |
| **Phase H – Architecture Change Management** | Establish procedures to handle changes; periodically review the architecture to adapt to new business requirements or technology innovations.                                |
| **Requirements Management**        | Manage requirements across all phases; ensure that new requirements are captured, analysed, and integrated into the architecture.                                                             |


6 High‑level integrated architecture
------------------------------------

The diagram below visualises the target architecture for the unified customer and product data initiative. Business users from PMO, HR and other departments interact with systems that expose APIs through a central **Integration Layer**. Data flows into a **Data Warehouse** and an **Analytics Platform**, enabling near‑real‑time reporting and insights.

**Key aspects**:

1.  *Central Integration Layer.* Instead of point‑to‑point connections, all systems (Salesforce CRM, Oracle ERP, HR system) expose services to a common integration platform. This reduces duplication and eases governance.
2.  *Data pipelines for analytics.* The integration layer feeds both the data warehouse (for curated, structured data) and the analytics/data‑lake platform (for big‑data and real‑time analysis).
3.  *Feedback loop to business users.* Dashboards and reports deliver insights back to business users, closing the loop and enabling data‑driven decision‑making.

7 Expected outcomes
-------------------

Implementing this initiative using TOGAF will address the problems identified earlier:

*   **Improved business buy‑in.** By focusing on outcomes such as faster reporting and better resource utilisation and involving stakeholders early, the EA team demonstrates tangible business value [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    
*   **Reduced fragmentation.** A unified data model and integration layer eliminate siloed tools and provide a single source of truth for customer and product data, tackling the issue of fragmented data and tools[(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    
*   **Better strategic alignment.** The business architecture links the initiative to strategic goals and ensures that technology decisions support business outcomes, avoiding the trap of technology‑for‑technology’s‑sake [(valueblue.com)](https://www.valueblue.com/blog/7-common-enterprise-architecture-challenges-and-how-to-solve-them).
    
*   **Governance and risk management.** TOGAF’s ADM phases (particularly Phases F–H) provide mechanisms for migration planning, implementation governance and change management [(ardoq.com)](https://www.ardoq.com/knowledge-hub/togaf), ensuring that the initiative stays on track and adapts to new requirements.
    

8 Conclusion
------------

Without a structured enterprise architecture, organisations often struggle with siloed systems, inconsistent data, and misaligned initiatives. TOGAF provides a comprehensive framework to address these issues by aligning business objectives with data, application and technology architectures and by guiding the implementation through an iterative ADM cycle. The unified customer and product data use case illustrates how TOGAF helps an organisation move from fragmented systems to an integrated, data‑driven ecosystem that supports informed decision‑making and continuous improvement.