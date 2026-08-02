# Kit Porath

**AI Platform Engineer.** I build secure, GitOps-native private AI infrastructure, direct
AI to build it, and verify what it tells me against the running system.

Michigan · Eastern Time · remote · [sovereignty-labs.com](https://sovereignty-labs.com)

---

### The platform

I built and operate a production private AI cloud on hardware I own. When it lost power
completely, it was back in **1 hour 50 minutes with zero data loss** — storage, database
quorum, hypervisors and Kubernetes cold-started in dependency order, then the recovery
turned into a verified runbook and permanent fixes so the next one is shorter.

`19 monitored hosts` · `6-node RKE2` · `~96 pods` · `8 GitOps applications` ·
`3-node HA Vault with transit auto-unseal` · `87 digest-verified mirrored images for
airgapped operation`

It is **operated by agents running on that same hardware.** From anywhere in the world,
over a private network, I can reach them and have them investigate, change, or respond to
a security event — on loops I built. That is the "agent-operated" part of the line above,
and it is the part most infrastructure claims and does not do.

### Four platforms, and the inversion that matters

| Platform | How it was built | Where it is now |
|---|---|---|
| **Valhalla** — k3s on mini PCs | by hand | gone |
| **Asgard** — Proxmox, Talos, full rack, 10G | AI-collaborated | completed · runs Hirdforge in production |
| **KWS** — bare metal → K8s, GitOps, SSO, Vault, GPU inference | AI-built under my direction | production · survived full power loss and a deliberate chaos test |
| **Hirdforge** — multi-agent engineering platform | directed build | deployed to production K8s · 435 merged PRs · ~68k lines of Go |

The one I built by hand is the one that no longer exists. Those same mini PCs now run the
KWS control plane. The way I work with AI matured across that arc — by hand, then
collaborating, then directing — while the systems got **more** durable, not less.

The discipline is the deliverable, not the keystrokes.

### How I work

**Verify live, don't trust reports.** A status document, a dashboard, or an AI's "done" is
a claim. Only a query against the running system is a fact. I've caught a secrets engine
sealed for 27 hours with its auto-unseal chain silently dead and every dashboard green, a
storage flag reported off that was on, and a crash-looping control plane reported healthy.

**Coordination is infrastructure, not agency.** Reliability in a multi-agent system comes
from deterministic routing and mechanical verification — tests and CI — never from a model
judging its own work. Changes land as pull requests behind human approval.

I design the systems and make the decisions. AI implements under my direction. I verify
against live state and catch it when it's wrong, and I say so plainly, because it's the
honest description and it's also the skill. I work across Claude Code, Codex, opencode and
Grok's tooling and pick the harness to fit the task — the value is the direction and the
verification, not the tool.

Twenty years of operations leadership before this, in automotive manufacturing, up to 35
direct reports, and an IT systems administration role along the way. Root-cause discipline
and verifying a fix instead of accepting a report is the judgment baseline, not a gap.

---

### Work

| | |
|---|---|
| **[kws](https://github.com/sovereignty-labs/kws)** | Private AI cloud — architecture, decisions, and the incident record including the power-loss recovery |
| **[hirdforge](https://github.com/sovereignty-labs/hirdforge)** | Multi-agent engineering platform — thesis, architecture, rejected alternatives |
| **[anvil](https://github.com/sovereignty-labs/anvil)** | Local inference control plane over llama.cpp. Runs on KWS |
| **[asgard](https://github.com/sovereignty-labs/asgard)** | The enterprise platform generation before KWS — lineage and decisions |

The infrastructure repositories are **curated extracts, not mirrors.** Architecture,
decisions and incidents are public; live inventories, addresses and secrets are not.

📧 [kitporath@gmail.com](mailto:kitporath@gmail.com) ·
💼 [linkedin.com/in/kitporath](https://www.linkedin.com/in/kitporath)
