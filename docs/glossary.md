# Glossary

## Concepts

Aggregate layer
:   Pre-computed summaries of the facts by period, axis, geography and organisation. In LOGIQ these
    are PostgreSQL materialised views, and the only objects the analytics API reads.

Asset (orchestration)
:   A data object, such as a warehouse table, that the pipeline produces and that declares which
    assets it is derived from. The orchestrator builds the lineage graph from these declarations.

Business Intelligence (BI)
:   The processes and tools that turn raw operational data into information and insight that
    support decisions.

Conformed dimension
:   A dimension shared, with one agreed definition, by several fact tables, so that figures
    reconcile across views and business axes.

Data warehouse
:   A central, query-optimised repository that consolidates data from several source systems
    for analysis rather than for day-to-day operations.

Decision Support System (DSS)
:   An information system that helps managers make semi-structured or unstructured decisions.

Dimension
:   A table holding descriptive context (who, what, where, when) used to filter and group facts.

ETL (Extract-Transform-Load)
:   The process that extracts data from sources, transforms it into the target model and loads it
    into the warehouse.

Fact
:   A table of measurable business events (amounts, counts, durations), recorded at a declared
    grain and linked to its dimensions.

Fact constellation (galaxy schema)
:   A dimensional schema in which several fact tables share a common set of conformed dimensions.

Financial perimeter
:   The boundary of costs and revenues that belong to one business axis. LOGIQ never mixes the
    parcel and transport perimeters.

Grain
:   The exact meaning of one row in a fact table, for example "one row per transport request".

Graceful degradation
:   Behaviour in which a system stays usable, with reduced capability, when a component is
    unavailable.

High-water mark
:   The last loaded position (for instance a timestamp) from which the next incremental
    extraction resumes.

Idempotent load
:   A load that gives the same result however many times it runs, so retries never duplicate
    data. LOGIQ achieves this with insert-or-update (upsert).

Junk dimension
:   A dimension that groups several low-cardinality flags into one table to keep facts narrow.

KPI (Key Performance Indicator)
:   A measurable value that shows how well an objective is being met.

Materialised view
:   A database view whose result is stored physically and refreshed on demand, making reads fast.

MoSCoW
:   A prioritisation method that sorts scope into Must have, Should have, Could have and Won't
    have (this time).

OLAP / OLTP
:   *Online Analytical Processing* (read-heavy analysis over history) versus *Online Transaction
    Processing* (day-to-day reads and writes of the running application).

Role-playing dimension
:   One physical dimension used in several roles, such as a date used as creation, completion or
    payment date.

RBAC (Role-Based Access Control)
:   Access control in which permissions are attached to roles, and users receive roles.

SCD Type 2 (Slowly Changing Dimension)
:   A historisation technique: a change closes the current row and opens a new version with its
    own surrogate key and validity window, so facts keep pointing at the version valid at event
    time.

Snowflake schema
:   A dimensional schema in which dimension hierarchies are normalised into one table per level.

Staging layer
:   The landing zone that holds a faithful, untransformed copy of each source extract.

Surrogate key
:   A generated key with no business meaning, used as the primary key of a dimension.

## Abbreviations

| Abbreviation | Meaning |
|---|---|
| API | Application Programming Interface |
| B2B / B2C | Business-to-Business / Business-to-Consumer |
| BI | Business Intelligence |
| COD | Cash on Delivery |
| CSV | Comma-Separated Values |
| DRF | Django REST Framework |
| DSS | Decision Support System |
| DW / DWH | Data Warehouse |
| DZD | Algerian Dinar |
| ELT | Extract-Load-Transform |
| ERD | Entity–Relationship Diagram |
| ERP | Enterprise Resource Planning |
| ESI | École nationale Supérieure d'Informatique |
| ETL | Extract-Transform-Load |
| HD / SD | Home Delivery / Stop Desk |
| HTTPS | Hypertext Transfer Protocol Secure |
| JSON | JavaScript Object Notation |
| KPI | Key Performance Indicator |
| LLM | Large Language Model |
| MoSCoW | Must, Should, Could, Won't have |
| OLAP / OLTP | Online Analytical / Transaction Processing |
| ORM | Object-Relational Mapping |
| QR | Quick Response (code) |
| RBAC | Role-Based Access Control |
| RDBMS | Relational Database Management System |
| REST | Representational State Transfer |
| SCD | Slowly Changing Dimension |
| SIT | Systèmes d'Information et Technologies |
| SQL | Structured Query Language |
| TLS | Transport Layer Security |
| UI | User Interface |
| UTC | Coordinated Universal Time |
| VPS | Virtual Private Server |
| WMS | Warehouse Management System |
