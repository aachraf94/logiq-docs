<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/logiq-logo-on-dark.svg">
    <img src="docs/assets/logiq-logo-on-light.svg" alt="LOGIQ" width="320">
  </picture>
</p>

<p align="center">
  <b>Turning scattered logistics data into reliable, proactive decisions.</b><br>
  <a href="https://aachraf94.github.io/logiq-docs/"><b>📖 Read the documentation →</b></a>
</p>

---

**LOGIQ** (*Logistics + IQ*) is a Business Intelligence decision-support system built for an
Algerian express-delivery operator. It brings data scattered across several operational
applications into a single **data warehouse**. An **automated ETL pipeline** keeps the warehouse
current. On top of it, LOGIQ adds **interactive dashboards**, **proactive alerts** and an
**AI assistant**.

It covers two business axes — **on-demand dedicated transport** and **parcel delivery** — each read
through three views: *Operations*, *Cost & Profitability* and *Performance*.

## Highlights

- **Data warehouse:** fact constellation with 7 facts and 55 dimensions, plus SCD Type 2 history.
- **ETL pipeline:** asset-oriented Dagster pipeline — incremental, idempotent, refreshed daily.
- **Dashboards:** 30 KPIs across both axes, with role-based access and Arabic / French / English support.
- **Alerting:** threshold rules delivered in-app and by e-mail.
- **Validation:** tested end to end on a production-scale synthetic dataset of ~13 M parcels and ~30.5 M status events.

<p align="center">
  <img src="docs/assets/dash-overview.png" alt="LOGIQ overview dashboard" width="800"><br>
  <sub>Consolidated overview (synthetic test data).</sub>
</p>

## About this repository

This repository contains **only the public documentation site**, built with
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). It holds no project source
code, credentials or real client data. All figures shown come from synthetic test data.

Run it locally:

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open <http://127.0.0.1:8000/logiq-docs/>. Every push to `main` is deployed to GitHub Pages
automatically by `.github/workflows/deploy.yml`.

## Credits

Final-year project (State Engineer diploma, option SIT, 2025/2026) at the
**École nationale Supérieure d'Informatique (ESI)**, Algiers, by **Achraf Abdelkebir**.

- **Host organisation:** Ourquilane
- **Client:** Yalidine El Djazair Services (Yalidine Express)
- **Supervisors:** Mr. Mohamed Amir Abbas (ESI) and Mrs. Yasmine Rihane (Ourquilane)
