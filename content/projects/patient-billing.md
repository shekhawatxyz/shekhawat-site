+++
date = '2026-07-20T01:52:33+05:30'
title = 'Patient Billing System'

+++

A Zango/Django app for managing insurance-claim billing: intake and tracking claims through a full lifecycle (draft → submitted → under review → approved/denied → appealed → closed), with role-based permissions for billing staff and managers at each step. A set of AI agents (claim validator, denial analyzer, appeal drafter) runs as independent Celery tasks to help process claims and draft appeals on denials. Background jobs run through Celery/Redis and data is stored in Postgres.

I deployed it live to AWS Lightsail behind Caddy with real Let's Encrypt TLS, and found (and fixed) a handful of real production issues along the way, including a debug-mode info leak and a CSRF config bug. [GitHub repo](https://github.com/shekhawatxyz/patientbilling) · [Design docs](https://app.notion.com/p/parakram/Patient-Billing-System-39ecbcdf8f20819a8a63f40ff20af215?source=copy_link).
