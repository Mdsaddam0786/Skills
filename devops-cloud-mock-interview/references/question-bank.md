# Question Bank — Calibration Anchors

These are examples, not a script. Use them to calibrate the *shape* and *tone* of generated
questions for each topic — never read one aloud verbatim, and never reuse one across sessions
with the same candidate. Each topic has three anchors spanning difficulty and company tier so
the spread is clear; interpolate for combinations not shown (e.g. Intermediate/Product).

## Cloud platforms (AWS/Azure/GCP)

- **Beginner, Service-based**: "A client asks you to give a new contractor read-only access to
  view EC2 instances and S3 buckets in one AWS account, nothing else. Walk me through how you'd
  set that up."
- **Intermediate, mixed**: "Your team's monthly AWS bill jumped 40% after a new feature shipped,
  and nobody's sure why. How would you figure out what's driving the cost, and what would you
  check first?"
- **Advanced, Product/MANG**: "You're designing multi-region active-active deployment for a
  service that needs 99.99% availability and strong consistency for user account data, but
  eventual consistency is fine for activity feeds. How do you architect this, and what do you
  give up to get it?"

## Containers & orchestration (Docker/Kubernetes)

- **Beginner, Service-based**: "A developer says their Docker container works fine locally but
  crashes immediately when deployed. What's your troubleshooting process?"
- **Intermediate, mixed**: "Pods in a deployment keep getting OOMKilled under moderate load, but
  the resource limits look reasonable on paper. How do you investigate and what are your
  options to fix it?"
- **Advanced, Product/MANG**: "You're rolling out a breaking API change across 40
  microservices owned by different teams, all running on the same Kubernetes cluster with
  shared infra. How do you sequence the rollout to avoid a cascading outage, and how do you
  decide when it's safe to proceed to the next stage?"

## CI/CD & Infrastructure as Code

- **Beginner, Service-based**: "A deployment pipeline is green, but the client reports the
  production site is still showing the old version. Where do you start looking?"
- **Intermediate, mixed**: "You need to roll out a database schema change alongside an app
  change, and the app won't work correctly if they're out of sync even briefly. How do you
  sequence the deploy and the migration?"
- **Advanced, Product/MANG**: "Your org wants to move from a single shared Terraform state file
  per environment to per-team ownership, without downtime or a big-bang cutover, across ~200
  resources already in production. How do you plan this migration?"

## Observability, incident response & Linux/networking

- **Beginner, Service-based**: "A client calls saying their website is 'slow.' You have SSH
  access to the server. What do you check, in what order?"
- **Intermediate, mixed**: "You get paged at 2am: error rate on checkout has spiked to 15%, but
  CPU/memory on all hosts look normal. Walk me through your triage."
- **Advanced, Product/MANG**: "Your service's error budget for the quarter is nearly exhausted
  three weeks early due to a string of small incidents, none individually severe. Engineering
  wants to ship a risky but high-value feature this week. How do you make this call, and who's
  involved in making it?"
