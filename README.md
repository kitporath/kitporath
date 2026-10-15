# Kit Porath

AI infrastructure and agent operations · Michigan · remote · [kitporath.com](https://kitporath.com)

I spent more than twenty years in automotive manufacturing, much of it leading production
teams, before I got serious about computers. I started with cybersecurity, built
infrastructure to practice on, and rebuilt it three times. Today it is a private cloud in my
workshop, and agents running on open-weight models on my own hardware do most of the
building and the day-to-day operations. My part is designing the systems, setting the rules
the agents work under, and deciding what merges. I don't write code by hand.

The cloud is built as defense in depth, because agents do most of the work: an edge firewall
and IDS, a cluster with no route to the internet, default-deny between apps, single sign-on,
Vault with offline unseal keys, digest-pinned images, runtime detection with automatic
quarantine, and encrypted offsite backups. Each layer has been tested, and
[kitporath.com](https://kitporath.com/#defense) lists how.

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
