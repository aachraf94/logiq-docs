# Future work

LOGIQ delivers on its four technical pillars: a centralised data warehouse, a reliable automated
ETL, interactive dashboards and a proactive alerting mechanism. Both prioritised axes are delivered
in full, each on its own financial perimeter. This page sets out the boundaries of that result and
where the platform goes next.

## Contributions

| Area | Contribution |
|---|---|
| Warehouse design | Layered dimensional warehouse (staging → dimensions → facts → aggregates) on a constellation schema with conformed, snowflaked dimensions |
| Modelling techniques | SCD Type 2 history, junk and role-playing dimensions, controlled and justified denormalisation |
| Data integration | Asset-oriented ETL — incremental, idempotent, observable — that depends only on the source *contract* |
| Operational / analytical split | Two stores, so heavy analytics never disturb the application |
| Decision experience | Multi-axis dashboards, role-filtered navigation and **auditable KPIs** traceable to their records |
| Security | RBAC over stateless authentication, aligned with the client's ISO 27001 context, on a read-only layer |
| Proactive monitoring | Scheduled, threshold-based alerting with in-app and e-mail delivery and per-user preferences |
| Validation apparatus | Faithful, production-scale source simulation behind a data-quality gate and a post-load integrity audit |

## Limitations

- **Simulated, not live, sources.** The production systems could not be connected within the
  project's scope. The simulation's fidelity to the source contract makes it a sound substitute,
  but the platform has not yet run against the real feeds.
- **No live user-acceptance round.** The platform was validated technically, but not yet
  evaluated formally with decision-makers in day-to-day use.
- **Deliberately bounded scope.** Route analysis was kept out of this version because the data it
  needs was not available within the project's scope.

## Roadmap

| Capability | Status | Condition / next step |
|---|---|---|
| **Route analysis** | Designed, deferred | Awaits routing and optimisation-reference data; the warehouse already accommodates it |
| **Live production integration** | Ready by design | Repoint the ETL from the simulation to the real source contracts |
| **Formal performance benchmarking** | Envisaged | Measure response times and refresh duration under production load |
| **User-acceptance testing** | Envisaged | Evaluate the platform in day-to-day use with the decision-makers |
| **Predictive analytics** | Envisaged | Extend the existing facts with forecasts of volumes, costs and performance |

!!! quote "Closing word"
    The project began with fragmented data and a business that could not read its own activity
    with confidence. It ends with a working, validated decision-support system that consolidates
    that data, keeps it current, makes it visible along the dimensions that matter, and turns
    trustworthy figures into the basis for proactive decisions.
