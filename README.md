🟡 What is a Canary Deployment?

Deploying a new version (v2) to a small subset of users/traffic first, while most users get the stable version (v1).
Monitor metrics/traces; if no errors, gradually shift more traffic to v2 until it’s 100%.
If errors spike, INSTANT rollback to v1—no drama, no downtime.

> Why Not Just “kubectl apply”?
That’s a blind update. If v2 is broken, everyone is impacted!
Canary = controlled risk, SRE/DevOps gold standard for rolling out changes.

💡 When to use canary?

Any time you deploy code that you can’t 100% guarantee.
Large user base, 24x7 APIs, or critical B2B stuff.
Want “blast radius” as small as possible.

🚦 How Istio + ArgoCD Supercharges This

Istio: Does the actual traffic split, metrics, tracing.

ArgoCD: All changes are GitOps—self-healing, rollback, audit, reviewable.

Kiali: Visualizes traffic.

Jaeger: Traces request flows—see who hits v1 vs. v2.

Prometheus/Grafana: Live metrics/alerts—see if error rates/latency spike.
