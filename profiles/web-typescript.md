---
title: Reference web TypeScript profile
owner: Software Architect
status: Proposed
last_updated: 2026-10-15
---

# Reference web TypeScript profile

## Purpose and adoption
This optional profile preserves the existing Axis web-stack preferences. It applies only after a project explicitly adopts it and records its fit, exceptions and owner. Existing repository conventions take precedence over this reference; it authorises no replacement of an existing framework, provider or data model. A Swift/native, framework-free or other-platform project does not inherit this profile by adopting a capability.

## Historical technology preferences
- TypeScript with strict checking; justify `any` escapes.
- Zod for untrusted boundaries in TypeScript projects.
- In an existing React/Next.js project, prefer Server Components/Actions where suitable; use Zustand for shared client state when needed and Tailwind where already adopted. Context remains suitable for dependency injection such as themes.
- Prefer `date-fns` or supported Temporal over introducing `moment.js`.
- Supabase Auth/Storage and pgvector are reference preferences when Supabase is already a justified choice. Provider selection and security posture remain L0; RLS is required on adopted Supabase tables.
- Trigger.dev/Inngest are candidates only when background work is needed. PostHog is a candidate only if analytics is justified and explicitly approved; it is not assumed installed.
- Platform environment configuration is the reference secret mechanism; assess whether the project's threat model requires more.
- Historical avoid-list: AWS, Kubernetes, managed Redis, dedicated vector databases and per-seat SaaS require explicit L0 approval before introduction under this profile. No profile approves spend.

## Historical performance defaults
For applicable web projects: LCP below 2.5 seconds, INP below 200 milliseconds and CLS below 0.1. For applicable standard API reads: p95 below 400 milliseconds. Record workloads and environments before treating these as meaningful budgets; define route payload budgets in the adopting project's performance document.

## Evidence and limits
This profile is guidance, not a dependency manifest, package, security certification or deployment. Record adoption in the project, run its own checks and preserve a reviewed exception when a default does not fit. The source is the pre-refactor constraints and memory at Polaris commit `4881ea912345079efeaee5fbd0d287680fd5a06e`.
