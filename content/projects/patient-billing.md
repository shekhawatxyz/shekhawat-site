+++
date = '2026-07-20T01:52:33+05:30'
title = 'Patient Billing System'

+++

A Zango/Django app for managing insurance-claim billing, with a React frontend, Celery/Redis for background jobs, and Postgres for storage. I deployed it live to AWS Lightsail behind Caddy with real Let's Encrypt TLS, and found (and fixed) a handful of real production issues along the way, including a debug-mode info leak and a CSRF config bug. [GitHub repo](https://github.com/shekhawatxyz/patientbilling).
