# cheap storage vps: 500GB from $25 a year with GreenCloud, plus the fine print worth reading before you pay

A cheap storage VPS in 2026 means paying roughly **$2–3 a month for around 500GB of disk**, and the current GreenCloud Storage KVM lineup sits right at that level: 500GB of SATA storage, 1 core, 2GB RAM and 3TB of traffic for **$25/year** in the US or Amsterdam. The catch, and it's an honest one, is that these servers are built for capacity, not speed — the vendor will tell you that themselves if you ask about disk performance.

This article covers GreenCloud's full storage lineup with verified pricing, how its per-gigabyte cost stacks up against RamNode and Contabo, and the add-on pricing quirks that most comparison posts skip entirely.

> **Quick pick:** for backups, media libraries, Nextcloud and other write-once-read-rarely workloads, the **Storage-0.5TB at $25/year** is the entry point most people actually need, and the US/EU versions come with triple the bandwidth of the same-priced APAC plan. 👉 [Check GreenCloud's current storage VPS prices and locations](https://greencloudvps.com/billing/aff.php?aff=6679)

## What a cheap storage VPS is actually for

A storage VPS trades disk speed for disk space. Instead of fast NVMe drives, you get large enterprise SATA disks arranged in a hardware RAID array, paired with enough CPU and RAM to run file-serving software. GreenCloud's Storage KVM line runs on KVM virtualization with a 10Gbps port, enterprise SATA drives in hardware RAID-10, and each VPS gets one IPv4 address plus IPv6 by default. Linux only — there's no Windows option on these plans.

The typical workloads are the ones RamNode lists on its own storage product page, and they apply here too: server backups and database dumps, Plex or Jellyfin media libraries, Nextcloud or SFTP file sync, seedboxes for legal content like Linux ISOs, and log aggregation. What they all share is lots of data and light I/O. If your application hits the disk hard and constantly — a busy database, video transcoding at scale — a storage plan is the wrong tool regardless of whose logo is on it.

## GreenCloud Storage KVM: the full lineup

GreenCloud splits storage VPS into two groups. US & EU plans run in Phoenix (AZ), Ogden (UT) and Amsterdam. APAC plans run in Tokyo and Singapore, and here's the detail that matters: **same price, one-third the bandwidth**.

| Plan | Storage | CPU / RAM | Bandwidth | Price | Get it |
| --- | --- | --- | --- | --- | --- |
| Storage-0.5TB | 500GB SATA | 1 core / 2GB | 3TB | $25/year | [Order Storage-0.5TB](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Storage-1 | 1024GB SATA | 2 cores / 3GB | 6TB | $45/year | [Order Storage-1](https://greencloudvps.com/billing/aff.php?aff=6679) |
| Storage-2 | 2048GB SATA | 4 cores / 6GB | 10TB | $80/year | [Order Storage-2](https://greencloudvps.com/billing/aff.php?aff=6679) |
| StorageAPAC-0.5TB | 500GB SATA | 1 core / 2GB | 1TB | $25/year | [Order StorageAPAC-0.5TB](https://greencloudvps.com/billing/aff.php?aff=6679) |
| StorageAPAC-1 | 1024GB SATA | 2 cores / 3GB | 2TB | $45/year | [Order StorageAPAC-1](https://greencloudvps.com/billing/aff.php?aff=6679) |
| StorageAPAC-2 | 2048GB SATA | 4 cores / 6GB | 4TB | $80/year | [Order StorageAPAC-2](https://greencloudvps.com/billing/aff.php?aff=6679) |

All plans include a 10Gbps port, Linux OS only, and 24/7/365 support. The prices above are the annual rates shown on the product page; if monthly billing is available for storage plans, it isn't advertised there, so plan around paying for a year up front.

The APAC bandwidth gap deserves its own sentence. StorageAPAC-0.5TB gives you 1TB of monthly traffic for $25/year while Storage-0.5TB gives you 3TB for the same money. Extra bandwidth in APAC costs **$15/TB/month** versus $3/TB/month in the US and Europe. If your users or your backup source are in Asia, that's still a reasonable trade for the latency. If they're not, there's little reason to pay Tokyo prices for Amsterdam distances.

## The add-on pricing most comparisons never mention

GreenCloud sells storage expansions à la carte: up to 20TB of additional disk at **$5/TB/month**, RAM at $3/GB/month and CPU cores at $3/core/month, subject to node availability and a cap — you can at most double what your plan already has.

Run the math on that storage add-on and something jumps out. Adding 1TB via the add-on costs $5/month, which is $60 over a year. Upgrading from Storage-0.5TB to Storage-1 gets you an extra 512GB for $20 more per year, plus more CPU, RAM and bandwidth. Per gigabyte, the plan upgrade is dramatically cheaper than the add-on. The add-on only makes sense when you're already on the largest plan and need headroom beyond 2TB, or when you genuinely need just one more terabyte and don't want to migrate.

That's the first thing you won't find in most roundup posts, and it changes which plan you should pick: **buy the bigger plan up front if you know you'll grow into it. Upgrading later via add-ons is the expensive route.**

## How the per-gigabyte cost compares

Here's the second thing roundups tend to skip: a proper cost-per-GB comparison across billing models, because "cheap" means different things monthly and annually.

| Provider | Cheapest plan | Storage | Effective cost | Billing |
| --- | --- | --- | --- | --- |
| GreenCloud Storage-0.5TB | $25/year (≈$2.08/mo) | 500GB SATA | ≈ $0.0042/GB | Annual |
| RamNode smallest | $4/mo | 160GB HDD | $0.025/GB | Monthly or hourly |
| RamNode 1TB tier | $17/mo | 1000GB HDD | $0.017/GB | Monthly or hourly |
| Contabo Storage VPS 10 | €5.50/mo for the first 24 months | 300GB SSD | ≈ €0.018/GB | Monthly, promo rate |

GreenCloud's annual pricing is in a different league on raw cost — roughly six times cheaper per gigabyte than RamNode's entry tier. But the comparison isn't one-sided. RamNode's plans are cancel-anytime monthly (or even hourly) rentals with far bigger bandwidth allowances at the top end — its 4TB plan ships with 150TB of monthly traffic. Contabo's storage line uses SSD rather than SATA HDD and bills monthly, though its advertised price is a promo rate valid for the first 24 months. If you might need to walk away from the server in three months, a $25/year plan you can't recover money from is worse than a $4/month one you can drop.

One more honest data point from the other direction: a community-reported GreenCloud storage promo in early 2026 offered 4TB in Singapore for roughly $6/month — pricing that undercuts everything in the table above. GreenCloud runs these promos periodically, so if your need isn't urgent, watching their announcements can pay off.

## The catch, stated plainly

Storage VPS means accepting mediocre disk performance, and GreenCloud's own support channel says so: when users asked about disk slowdowns, a moderator's answer was that "storage plans are not for high IO."

There's a concrete recent example worth knowing about. In April 2026, users on a hosting community reported that GreenCloud migrated Singapore and Los Angeles storage nodes to newer Cascade Lake hardware, and sequential write speeds dropped sharply afterward — one user documented writes falling from around 380 MB/s to the 94–113 MB/s range with high IO wait, and an 8TB Los Angeles customer reported dropping from about 420 MB/s to 200. CPU scores actually improved after the migration, which pointed specifically at the disk stack. Support responses were template replies, and the official line was that storage plans aren't meant for high-IO workloads. These are user-reported numbers, not officially confirmed, but the pattern is consistent with what storage plans are designed for — and it's the same answer you'd get from any provider running cheap bulk SATA.

Three other limitations to know before ordering:

- **Unmanaged, fully.** GreenCloud doesn't help with software, OS configuration or application issues. You get root access and you're on your own, which is standard at this price but surprises people coming from managed hosts.
- **Refunds are reportedly tight.** Reviewer writeups note that GreenCloud's refund policy is strict, particularly on discounted promo plans, and some HostAdvice user reviews complain about refund friction. There's no generous trial window advertised for storage plans, so treat an order as a commitment.
- **Linux only.** If you wanted Windows file services, this line doesn't offer it — GreenCloud's Windows VPS plans are a separate product with different pricing.

Provisioning itself is quick: typically within 15 minutes of payment, occasionally up to two hours.

## Who should skip a storage VPS entirely

Some readers searching for a cheap storage VPS actually need something else, and it's cheaper to realize that now than after paying.

If your problem is "my laptop's disk is full," a 2TB external drive costs less than one year of any plan here and doesn't depend on your home upload speed. If you need object storage for backups — S3-compatible, pay only for what you fill — several providers sell that by the gigabyte and you'd likely spend pennies for the same archive. And if you need fast disk for a database or a busy web app, GreenCloud's own Budget KVM line starts at $6/month with NVMe-backed SSD storage, which is the better purchase at similar money for speed-sensitive work.

The storage VPS earns its keep when you need a *server*, not just space: something that runs Plex, seeds ISOs, pulls scheduled backups from five other machines, or hosts a Nextcloud instance for a small team. Space plus a CPU plus a fat pipe, running 24/7.

## FAQ

**Is the $25/year price really the ongoing price, or a first-term discount?**
The storage plan prices are shown as flat annual rates on the product page, without a first-term/expiry structure like Contabo's 24-month promo pricing. That said, the page doesn't publish renewal terms separately, so if you want certainty about year two, that's a reasonable question to ask support before ordering.

**Can I get monthly billing on a storage plan?**
The product page lists annual prices only for the storage KVM line. GreenCloud's budget SSD and Windows lines offer monthly billing, but for storage plans, assume you're committing to a year unless support tells you otherwise.

**How much does extra bandwidth cost if I run out?**
$3/TB/month in the US and Europe, $15/TB/month in APAC. On the APAC plans this is expensive enough that heavy transfer users should genuinely reconsider the location.

**What virtualization and access do I get?**
KVM with full root access, 10Gbps port, one IPv4 and IPv6 (/112 or /64) included. NVMe boot drives are available in some locations, with the bulk storage remaining SATA.

## Picking a plan and placing the order

The decision is simpler than the six-plan table makes it look. Roughly: under 500GB of data and light traffic → **Storage-0.5TB, $25/year**. Somewhere between 500GB and 1TB, or you want headroom → **Storage-1 at $45/year**, which remains far cheaper per gigabyte than buying add-ons later. Above 1TB or running media serving for multiple users → **Storage-2 at $80/year**. Inside that framework, pick US/EU unless latency to Tokyo or Singapore genuinely matters to you — the bandwidth difference alone usually settles it.

Two things to double-check at checkout, because this is where budget VPS orders go wrong. First, confirm the location on the order form — GreenCloud lists all locations for a plan in one place, and it's easy to end up with Phoenix when you meant Amsterdam, or vice versa. Second, remember the year is prepaid and the service is unmanaged; if the data you're putting on it is hard to move, that's an argument for starting with the smaller plan rather than the larger one.

If that trade sounds right for your use case, 👉 [order the GreenCloud storage plan that fits from the official site](https://greencloudvps.com/billing/aff.php?aff=6679) and have your backup or media stack ready to deploy — you'll have root access long before your coffee gets cold.
