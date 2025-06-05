🟡 What is a Canary Deployment?

Deploying a new version (v2) to a small subset of users/traffic first, while most users get the stable version (v1).
Monitor metrics/traces; if no errors, gradually shift more traffic to v2 until it’s 100%.
If errors spike, INSTANT rollback to v1—no drama, no downtime.

> Why Not Just “kubectl apply”?
That’s a blind update. If v2 is broken, everyone is impacted!

Canary = controlled risk, SRE/DevOps gold standard for rolling out changes.
