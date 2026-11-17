# Linux VPS hosting: What does RackNerd charge per year, does the price hold at renewal, and which of the five KVM specials do you actually need? (Full plan table)

RackNerd's Linux VPS range is five unmanaged KVM plans, each with full root access, a 1 Gbps port and one dedicated IPv4 address, billed by the year rather than the month. The 1 GB special is **$21.99/year** and the 2 GB is **$35.99/year**, which is the tier most people should buy. Two facts should shape your decision before anything else: these specials come with no money-back window, and the larger plans cost enough per term that picking the wrong one is a real loss rather than an inconvenience.

What follows is the full lineup, what each tier can actually run, the add-on costs that competing price pages leave out, and the cases where paying a managed host is the smarter buy.

## Quick pick

> Most readers should take the **2 GB KVM special at $35.99/year**. It meets the 2 GB minimum RackNerd lists for n8n and Coolify, holds a Docker stack with a few containers, and doubles the entry plan's disk (40 GB against 24 GB). 👉 [Check the 2 GB special's current term price](https://bit.ly/RacKnerd)

## The five KVM specials, side by side

| Plan | vCPU / RAM | SSD storage | Bandwidth | Price (annual term) | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB | 1 vCore / 1 GB | 24 GB | 2 TB @ 1 Gbps | $21.99/yr | [ Order](https://bit.ly/RacKnerd) |
| 2 GB | 1 vCore / 2 GB | 40 GB | 3.5 TB @ 1 Gbps | $35.99/yr | [ Order](https://bit.ly/RacKnerd) |
| 3.5 GB | 2 vCore / 3.5 GB | 65 GB | 7 TB @ 1 Gbps | quoted per term | [ Order](https://bit.ly/RacKnerd) |
| 4 GB | 3 vCore / 4 GB | 105 GB | 9 TB @ 1 Gbps | quoted per term | [ Order](https://bit.ly/RacKnerd) |
| 6 GB | 4 vCore / 6 GB | 140 GB | 12 TB @ 1 Gbps | quoted per term | [ Order](https://bit.ly/RacKnerd) |

RackNerd quotes the three larger tiers per annual term at checkout and rotates the lineup as promotions change, so treat those cells as "confirm on the order page" rather than fixed. All five run on RAID-10 SSD, include one dedicated IPv4, and deploy automatically within minutes of payment.

**What every plan includes, beyond the table:**

- **ctrl**, RackNerd's own control panel: reboot, OS reinstall, an out-of-band HTML5 VNC console, one-click app installs, inbound firewall rules, root password reset and plan upgrades.
- **OS templates:** CentOS, Rocky Linux, AlmaLinux, Fedora, Debian and Ubuntu. Custom ISO installs go through a support ticket.
- **One-click apps:** Docker with Portainer, WordPress stacks (AdminBolt, CyberPanel, CloudPanel), plus AI tooling (Ollama, AnythingLLM, LibreChat, Hermes Agent, OpenClaw) and n8n or Coolify.
- **IPv6:** up to 100 free addresses on request in Los Angeles and France. Other locations don't support it yet.
- **Upgrades:** you can move up one plan at a time, with roughly a minute of downtime for the reboot.
- **Support:** unmanaged service with 24/7 support access for platform issues.

## The price is a year, not a month

The 1 GB special works out to about $1.83/month, which is why RackNerd's headline figures look impossible next to hosts advertising $6 to $13 monthly. You are prepaying twelve months to get that rate. RackNerd also sells a monthly-billed KVM line, and it costs more per month than the annual specials do.

That prepayment is the actual risk. RackNerd's terms carry **no money-back period** on these plans. Cancelling immediately starts a 24-hour termination countdown rather than a refund, prepaid account credit isn't refundable, and a chargeback filed against a service already suspended for abuse carries an administrative fee of $125 to $250. If you are unsure about the provider or the datacenter, spend a few weeks on a monthly plan first, then move to the annual special.

Compare that with how the mainstream hosts structure the same purchase. Hostinger's KVM 1 advertises $6.49/mo but renews at **$11.99/mo**, and it bills the whole term up front: $155.76 for 24 months. KVM 4 goes from $12.99/mo to **$28.99/mo** at renewal, with $311.76 due on day one. The renewal multiple there runs from 1.85x to 2.23x. A $21.99 RackNerd year costs less than two months of Hostinger's renewal rate, and it includes weekly backups and a free domain on the Hostinger side, which is the trade.

Ask RackNerd support to confirm the renewal rate for the exact term you're buying before you pay. That single question settles the cost of year two. 👉 [See the current annual term prices](https://bit.ly/RacKnerd)

## Add-on costs the plan table hides

Cheap VPS comparison pages rarely price the extras, and the extras are where a $3 plan turns into an $8 plan. Atlantic.Net publishes its rate card (dated March 2023): each additional IPv4 costs **$3.65/month**, inbound traffic is unlimited, and outbound traffic beyond the free allowance is **$0.02/GB**. Buy two extra IPs for separate sites and you have added more than the RackNerd 2 GB plan's entire monthly-equivalent cost.

RackNerd's structure is simpler here. One dedicated IPv4 is included on every special, bandwidth allowances run from 2 TB to 12 TB depending on tier, and the port is 1 Gbps across the board. For most multi-site setups, the free IPv6 block in Los Angeles and France removes the reason to buy extra IPv4 addresses at all.

The cost that isn't on any price page is buying the wrong tier. You can upgrade to the next plan up, but you can't get a refund and start over, so size the disk first. 24 GB on the entry plan fills quickly with Docker images, logs and a couple of database dumps.

## Root access, and where the managed line sits

Every RackNerd special gives you full root over SSH. You patch the OS, you own the mistakes, and RackNerd supports the platform rather than your stack.

Managed hosts split on this point in ways that surprise people. hosting.com sells managed cPanel servers with CloudLinux, Monarx, LiteSpeed and daily backups at 99.99% uptime, and it deliberately **does not give root**: patching and security stay in their hands, and the company points customers who want root to its unmanaged range. Liquid Web goes the other way. Its Linux VPS is fully managed, carries a 100% uptime guarantee, includes root access anyway, and starts at **$11/mo** for 1 vCPU, 2 GB RAM, 60 GB storage and 2 TB of bandwidth, billed hourly with unused resources prorated back. Root access alone doesn't tell you whether a plan is managed; what changes is who patches the kernel at 2 a.m.

## Which tier fits which job

**1 GB / 24 GB.** A single low-traffic site, a WireGuard node, an uptime monitor, a secondary DNS server. Disk is the binding constraint here, not RAM. Keep images and logs pruned.

**2 GB / 40 GB.** The default for a reason. RackNerd's own app notes put n8n and Coolify at a comfortable 2 GB, and Docker with Portainer plus two or three small WordPress sites fits without swapping.

**3.5 GB / 65 GB.** A middle tier that is awkward for AI workloads: Ollama, AnythingLLM, LibreChat and Hermes Agent all want **at least 4 GB** according to RackNerd's app requirements. The 3.5 GB plan sits just below that line, so it's a general-purpose upgrade rather than an AI box.

**4 GB / 105 GB.** The first tier that meets the stated minimum for local LLM tooling. Three vCPUs and 105 GB of disk also make it the sensible pick for a busy multi-site server or a CI runner.

**6 GB / 140 GB.** The top special. Note the gap: OpenClaw's listed minimum is **8 GB of RAM**, so none of these five plans clears it. If OpenClaw is your reason for buying, this lineup tops out short of the requirement and you should run a smaller model under Ollama on the 4 GB tier instead.

## Datacenter choice moves latency more than the plan does

RackNerd runs around 20 locations across North America and Europe, including Los Angeles, San Jose, Seattle, Dallas, Chicago, Atlanta, Ashburn, Tampa, New York, Toronto, Amsterdam, London, Dublin and Strasbourg. Each location publishes test files and a looking glass, so you can measure throughput and the actual network path from your own connection before ordering.

For audiences in Asia, Los Angeles is the usual recommendation, and it's one of the two locations that will hand you up to 100 IPv6 addresses on request. Budget nodes on ordinary transit can slow during Asian evening and weekend peaks, which is exactly what the test files are for. Pick the location nearest your users, not the one nearest the top of the list. 👉 [Choose a datacenter and deploy a KVM special](https://bit.ly/RacKnerd)

## When RackNerd is the wrong buy

- **You want someone else to patch the server.** Liquid Web at $11/mo is fully managed with a 100% uptime guarantee. hosting.com's managed cPanel plans run at 99.99% and include migrations, at the cost of root access.
- **You need a refund window or a trial.** RackNerd has neither on the specials. Buy monthly first, or choose a host with a cancellation period.
- **You need maximum RAM per euro.** Contabo's Cloud VPS 4 lists 4 vCPU, 8 GB RAM, 100 GB SSD and unlimited traffic on a 200 Mbit/s port, shown at €5.50 with €4.40/month for the first 24 months. Different hardware class, different network reputation, far more memory for the money.
- **You need a phone call at 3 a.m.** RackNerd's support is ticket and chat based. Atlantic.Net advertises 24/7 phone support in the US, on a rate card that hasn't been refreshed since 2023.

## FAQ

**Which distribution should I pick?** Ubuntu or Debian for most self-hosted stacks, Rocky or AlmaLinux if you're mirroring an enterprise environment. All six templates are available at order time, and ctrl can reinstall later without a ticket.

**Can I run Windows?** The stock templates are Linux only. Custom ISO installs are handled through a support ticket, and licensing is your responsibility.

**How fast is setup?** Automatic. The VPS is provisioned within minutes of payment, with no queue.

**Does it include backups?** No managed backup service is part of the specials. Keep automated off-server backups from day one; on a plan with no refund window, that habit matters more than on a host that will hand your money back.

**Can I upgrade later?** Yes, one tier at a time, with about a minute of downtime for the reboot. Data stays in place.

**How do I get IPv6?** Open a ticket after ordering. Los Angeles and France support up to 100 free addresses; other locations are still being rolled out.

## Deciding in one minute

A single small site or a VPN endpoint: the **1 GB at $21.99/year**. Docker, a few sites, n8n or Coolify: the **2 GB at $35.99/year**. Local AI tooling or a busy multi-site server: the **4 GB**. OpenClaw: none of these, since it wants 8 GB.

Two things to confirm before you pay: the renewal rate for the exact term you're buying, and the datacenter closest to your users, tested against the location's own speed files. Everything else on this page is already decided by the specs. 👉 [Compare the five KVM specials and order](https://bit.ly/RacKnerd)
