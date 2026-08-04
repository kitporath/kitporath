# Kit Porath

## I run fleets of AI agents against production infrastructure — and I can prove how they fail.

Most engineering orgs are trying to do this right now. Most are finding out the hard
way that the problem isn't model quality, it's that **agents report work as done that
isn't.** I've been running it in production for a year, on hardware I own, that pages
me when it breaks. Then I published the failure taxonomy — including my own errors.

📄 **[How AI agents fail at infrastructure work](https://github.com/sovereignty-labs/kws/blob/main/docs/agent-failure-analysis.md)** — 13 audited claims, 8 material errors, hand-labelled and grouped

Michigan · Eastern Time · remote · [sovereignty-labs.com](https://sovereignty-labs.com)

---

### The platform this runs on

I designed, built and operate a production private AI cloud on my own hardware. When
it lost power completely, it was back in **1 hour 50 minutes with zero data loss** —
storage, database quorum, hypervisors and Kubernetes cold-started in dependency
order. Then I turned the recovery into a verified runbook and shipped permanent fixes
so the next one is shorter.

`19 monitored hosts` · `6-node RKE2` · `~96 pods` · `8 GitOps applications` ·
`3-node HA Vault with transit auto-unseal` · `digest-verified image mirror for
airgapped operation` · `default-deny egress`

It is **operated by agents running on that same hardware.** From anywhere in the
world, over a private network, I direct them to investigate, change, or respond to a
security event — on loops I built. That is the part most "AI-powered" infrastructure
claims and does not do.

### Four platforms, and the inversion that should worry you

| Platform | How it was built | Where it is now |
|---|---|---|
| **Valhalla** — k3s on mini PCs | by hand | **gone** |
| **Asgard** — Proxmox, Talos, full rack, 10G | AI-collaborated | completed · ran Hirdforge in production |
| **KWS** — bare metal → K8s, GitOps, SSO, Vault, GPU inference | AI-built under my direction | **production** · survived total power loss and a deliberate chaos test |
| **Hirdforge** — multi-agent engineering platform | directed build | **deployed to production K8s** · 712 merge commits · ~67k lines of Go |

**The one I built by hand is the one that no longer exists.** Those same mini PCs now
run the KWS control plane. As I moved from typing code to directing it, the systems
got *more* durable, not less — because the discipline scaled and my hands didn't.

That inversion is the whole argument. The keystrokes were never the value.

### What I'm unusually good at

**Catching AI when it's wrong — fast, and with receipts.** A secrets engine sealed for
27 hours with its auto-unseal chain silently dead and every dashboard green. An agent
reporting an 80% vulnerability reduction that was a unit mismatch. Another retiring 52
container images as "unused" — 15 were running the cluster, including the CNI. A
security scanner reporting *clean* because it had silently stopped reading. Every one
found by querying live state instead of reading a report.

**Building the platform layer, not the model layer.** Gateway, routing, quotas, cost
attribution, observability, disaster recovery, egress control, identity. I self-host
inference too, which is rarer — but the job is the gateway, and I've run it under real
failure.

**Turning a manual process into an automated one, with the people who do it.** Twenty
years leading operations in automotive manufacturing, up to 35 direct reports, plus an
IT systems administration role. I know what happens when the process in the wiki isn't
the process, and I know that the number that renews a budget is minutes-per-task, not
model accuracy. That's not background — it's the half of this work that can't be
crammed for.

I work across Claude Code, Codex, opencode and Grok's tooling, and pick the harness to
fit the task. The value is the direction and the verification, not the tool.

---

### Evidence

| | |
|---|---|
| **[Agent failure analysis](https://github.com/sovereignty-labs/kws/blob/main/docs/agent-failure-analysis.md)** | 13 audited claims, 8 material errors, the taxonomy and the countermeasures |
| **[kws](https://github.com/sovereignty-labs/kws)** | The private AI cloud — architecture, ADRs with rejected alternatives, incident narratives |
| **[hirdforge](https://github.com/sovereignty-labs/hirdforge)** | Multi-agent engineering platform. Run `git shortlog -sn` — agents authored roughly half the non-merge commits, and the history says so |
| **[asgard](https://github.com/sovereignty-labs/asgard)** | The generation before KWS — including the audit that found "healthy, triple-replicated" meant one disk from total, silent loss |

Infrastructure repos are **curated extracts, not mirrors** — architecture, decisions
and incidents are public; live inventories and secrets are not. That distinction is
itself part of the work.

**Open to platform, forward-deployed and AI-reliability roles.**

📧 [kitporath@gmail.com](mailto:kitporath@gmail.com) ·
💼 [linkedin.com/in/kitporath](https://www.linkedin.com/in/kitporath)
