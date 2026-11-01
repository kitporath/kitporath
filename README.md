# Kit Porath

**I direct AI agents to build and run production infrastructure, and I publish where they fail.**

Infrastructure · cybersecurity · AI inference and agent operations · Michigan · remote · [kitporath.com](https://kitporath.com)

I spent more than twenty years in automotive manufacturing, much of it leading production
teams, before I got serious about computers. I started with cybersecurity, built
infrastructure to practice on, and rebuilt it three times. Today it is KWS, a private cloud in
my workshop: 19 monitored hosts on a Cisco Nexus 10G/40G fabric, a six-node RKE2 Kubernetes
cluster driven by ArgoCD, a three-node HA Vault, nine tested layers of defense in depth, and a
multi-GPU inference tier I serve and tune myself.

I don't write or read application source code (Go, Python, TypeScript). Agents write it under
my direction. Local open-weight models carry the routine work, by my own accounting about 90%
of operations and 80% of coding, and I bring in frontier models for large decisions and deep
root causes. My part is the architecture, the specs, the permission boundaries, and deciding
what merges, checked against CI and the running system.

### The audit

In August I audited 13 claims that three AI systems and I made about this estate. Eight
contained a material error, three of them mine, and seven of the eight were a correct
measurement aimed at the wrong surface. One agent reported critical CVEs down 80%. The rescan
said 28%, and that is the number on record.
[Read the analysis](https://github.com/kitporath/kws/blob/main/docs/agent-failure-analysis.md).

### What's here

| | |
|---|---|
| [kws](https://github.com/kitporath/kws) | The private AI cloud: architecture, decision records with the rejected alternatives, and incident write-ups, including the [error analysis](https://github.com/kitporath/kws/blob/main/docs/agent-failure-analysis.md) above |
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

Open to remote US roles in AI infrastructure, AI platform, agent operations and platform
engineering.
[kitporath@gmail.com](mailto:kitporath@gmail.com) · [linkedin.com/in/kitporath](https://www.linkedin.com/in/kitporath) · [résumé](https://kitporath.com/resume) · [evidence](https://kitporath.com/evidence)
