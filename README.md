<div align="center">
<h1>DriveNow Database Design</h1>
  <p><strong>Database design for a car-rental and fleet-management system</strong></p>
  <p>
    <a href="https://github.com/Tariq-Zeyad/Tariq-Zeyad-Database-Assignment-1">GitHub Repository</a>
    &nbsp;·&nbsp;
    <a href="https://app.diagrams.net/">Open in diagrams.net</a>
    &nbsp;·&nbsp;
    <a href="https://simulationeg.com/">Simulation Academy</a>
  </p>
</div> <table>
  <tr><th align="left">Student</th><td>Tariq Zeyad Khashan</td><th align="left">Group</th><td>1</td></tr>
  <tr><th align="left">Student ID</th><td colspan="3"><strong>Add before submission</strong></td></tr>
  <tr><th align="left">Source requirements</th><td colspan="3">DN-SRS-2026-01 · Version 1.3</td></tr>
  <tr><th align="left">Deliverable</th><td colspan="3">Editable diagrams.net source and page-by-page PNG exports</td></tr>
</table>

## Project overview

This project translates DriveNow’s approved car-rental and fleet-management requirements into a conceptual data model and a relational schema. The design also documents unresolved questions, stated assumptions, and business rules that cannot be enforced by simple column-level constraints alone.

## Deliverables

| File or folder | Description |
| --- | --- |
| [`DriveNow.drawio`](DriveNow.drawio) | Editable source containing all 62 pages: the contents page, Chen ERD, relational-schema overviews, detailed table pages, assumptions, and business rules. |
| [`exports/`](exports/) | PNG preview of every draw.io page. Each image uses the matching page name. |
| `README.md` | Project summary and navigation guide. |

## Navigate the diagrams

Open `DriveNow.drawio` in [diagrams.net](https://app.diagrams.net/) and start with `0-Contents`.

| Page group | What it contains |
| --- | --- |
| `1-ERD-*` | Seven Chen ERD pages organized by business area, with relationship cardinalities and participation. |
| `2-Schema-Overview-*` | Five overview pages showing related tables and their fields together. |
| `2-Schema-1` to `2-Schema-47` | Detailed relational schema pages with keys, nullability, applicable constraints, and FK reference boxes. |
| `3-Questions-Assumptions` | Open questions, assumptions, and gaps or contradictions identified in the SRS. |
| `4-Business-Rules` | Rules requiring transaction, trigger, or application-level enforcement. |

`RENTAL` spans `2-Schema-23` and `2-Schema-24` so the exported page remains within the assignment’s 4,000-pixel width limit.

## Design scope

The relational design contains **46 tables and 261 columns** covering branches and staff, training, vehicle inventory and movement, pricing, customers, reservations, rentals, maintenance, payments, corporate invoicing, and loyalty.

Key design choices include:

- Effective-dated category and model rates preserve pricing history; the rental records the rate and discounts charged at the time.

- Vehicle status events and branch transfers retain operational history and accountability.

- Separate transaction records preserve training attempts, loyalty movements, repair work, and part usage.

- Corporate invoices and their rental allocations are modeled separately from individual rental payments.

- Cross-row and temporal rules are documented with suggested enforcement approaches rather than being presented as ordinary `CHECK` constraints.

## Validation

The final diagram source contains **62 pages**, with **62 matching PNG exports**. The exports were checked against the source, and no page exceeds the specified 4,000-pixel width limit.



