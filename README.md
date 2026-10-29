# Kit Porath

Infrastructure · cybersecurity · local AI inference and agent operations · Michigan · remote · [kitporath.com](https://kitporath.com)

I spent more than twenty years in automotive manufacturing, much of it leading production
teams, before I got serious about computers. I started with cybersecurity, built
infrastructure to practice on, and rebuilt it three times. Today it is a private cloud in my
workshop, and I build and run its physical and platform layers myself: the rack, the 10G and
40G network on Cisco Nexus, Proxmox and OpenNebula/KVM, Kubernetes across three generations
(k3s, Talos, RKE2), LINSTOR/DRBD, MinIO and ZFS storage, and ArgoCD GitOps. Agents running on
open-weight models on my own hardware write the application software and run most of the
routine operations. My part is the architecture, the specs and constraints the agents work
under, and deciding what merges. I don't write or read application source code (Go, Python,
TypeScript).

The cloud is built as nine layers of defense in depth, because agents do most of the work: an
OPNsense edge firewall with Suricata, a cluster with no route to the internet, Cilium
default-deny between apps, Keycloak single sign-on, HA Vault with offline unseal keys, an
internal CA, digest-pinned images, Trivy and gitleaks in CI, Falco with automatic pod
quarantine, host hardening, and encrypted offsite backups. Each layer has been tested, and
[kitporath.com](https://kitporath.com/#defense) lists how.

The inference tier is the third pillar, and it is hand-tuned: five GPUs (an R9700 with 32GB, a
PRO 4000 Blackwell, an RTX 3090, a 5060 Ti and a 3060) running llama.cpp and ExLlamaV3, with
the KV-cache budgets, quantization choices and a 180B model split across CPU and GPU worked
out by me. LiteLLM fronts it, MCP servers give the agents their tools, and together they run
roughly 90% of this estate day to day.

### What's here

| | |
|---|---|
| [kws](https://github.com/kitporath/kws) | The private AI cloud: architecture, decision records with the rejected alternatives, and incident write-ups, including [an error analysis of AI agents doing infrastructure work](https://github.com/kitporath/kws/blob/main/docs/agent-failure-analysis.md) (13 claims audited, 8 wrong, 3 of them mine) |
| [hirdforge](https://github.com/kitporath/hirdforge) | A multi-agent engineering platform on production Kubernetes. The public extract is 67,115 lines of Go, and `git shortlog -sn` shows agents authored 382 of its 808 non-merge commits |
| [asgard](https://github.com/kitporath/asgard) | The infrastructure generation before KWS: Proxmox, Talos, 10G |

The infrastructure repositories are curated extracts, not mirrors. Architecture, decisions
and incidents are public. Inventories and secrets are not.

### Not public yet

**Workbench** is the coding-agent app I use every day: a Go server with its own agent loop, a
web app and a desktop app. Every thread works in its own git worktree, and anything that
reaches outside it waits for my approval. **Groundly** is a self-hosted research notebook
that cites the exact passage behind every claim, or says the sources don't support an answer.
I'm happy to demo either.

Open to remote US roles in AI infrastructure, AI platform, agent operations and
forward-deployed engineering.
[kitporath@gmail.com](mailto:kitporath@gmail.com) · [linkedin.com/in/kitporath](https://www.linkedin.com/in/kitporath) · [résumé](https://kitporath.com/resume.html) · [evidence](https://kitporath.com/evidence)
