# Best VPS 2026: Which LightLayer Plan Fits, What Year Two Costs, and What the Refund Policy Actually Covers

LightLayer's cheapest VPS runs **$4/month** for 1 core, 1GB RAM and 50GB of SSD storage, and the same box drops to **$24.99/year** (about $2.08/month) on the Manila and Taiwan annual plans. Over twelve months that is a fraction of what the mainstream picks in the 2026 roundups charge, which is why the name keeps surfacing in budget threads. It is also a self-managed Linux server sold with a refund policy that covers provider-side faults only, so the low price is real but conditional: it only works if you can administer the box yourself and you pick the right size the first time.

Below are the current plans and prices, the sizing rules that decide which tier you need, the year-two cost question nobody puts in a comparison table, and the four hosts most buyers end up choosing between.

> **Quick pick:** Most readers should take the **Startup plan at $4/month**, or the **$24.99/year** annual plan in Manila or Taiwan if they can commit for a year. One WordPress site, a staging environment, a small Docker host or a VPN endpoint all fit. Move up to the 4-core Mid-Tier only when you are running several sites or a database that needs more than 2GB of RAM.
>
> If you need someone else to manage the server, or you want your money back because you changed your mind, LightLayer is the wrong shop.
>
> 👉 [Check the current LightLayer plan prices](https://account.lightlayer.net/?affid=74)

## LightLayer VPS plans and prices

LightLayer sells by location and network route, so identical specs can carry different prices depending on which data center you pick. The figures below are what its plan and order pages list at the time of writing. Confirm the number on the order page before you pay, especially if you are choosing between a standard and a premium route.

| Plan | vCPU / RAM / Storage | Port and bandwidth | Price | Order |
| --- | --- | --- | --- | --- |
| Startup | 1 core / 1GB / 50GB SSD | 100Mbps, unlimited | **$4.00/mo** | [Order Startup](https://account.lightlayer.net/?affid=74) |
| Pay As You Go | 2+ cores / 2GB+ / scalable | 200Mbps+ | **from $5.60/mo** | [Configure Pay As You Go](https://account.lightlayer.net/?affid=74) |
| Mid-Tier | 4 cores / 4GB / 80GB SSD | 200Mbps, unlimited | **~$11–18/mo** (varies by location) | [Order Mid-Tier](https://account.lightlayer.net/?affid=74) |
| Business | 32 cores / 32GB / scalable | 200Mbps, unlimited, premium network | **$53.60/mo** | [Order Business](https://account.lightlayer.net/?affid=74) |

Annual billing changes the entry price far more than the spec sheet does. These are the yearly rates for the 1 core / 1GB / 50GB configuration:

| Location | Annual price | Effective monthly |
| --- | --- | --- |
| Manila | $24.99/yr | ~$2.08 |
| Taiwan | $24.99/yr | ~$2.08 |
| Los Angeles (Global route) | $29.99/yr | ~$2.50 |
| Los Angeles (Standard route) | $39.99/yr | ~$3.33 |
| Los Angeles (Premium route) | $49.99/yr | ~$4.17 |

A few things worth knowing before you open the cart. The virtualization is KVM, the hardware is AMD EPYC, and every plan includes full root access, so you install whatever you want. Locations span Hong Kong, Taiwan, Japan, Thailand, Singapore, the Philippines, the United States, the United Kingdom and Germany. Payment goes through PayPal, credit card or Alipay, which matters if you are buying from Southeast Asia and do not want a card on file. LightLayer is a young brand, dated to 2024 by third-party host directories, with a wide spread of new locations. Long-term operational track record is the thinnest part of the offer.

## How much server do you actually need?

Match the plan to your workload rather than to the price. The sizing bands most hosting reviewers use are consistent: a 1–2GB, single-core VPS handles roughly 5–10 lightweight sites or 10,000–50,000 monthly visits; a 4–8GB, 2–4 core machine covers 20–50 sites or 100,000–500,000 visits; 8GB and up with multiple cores supports 50+ sites and a million-plus visits, assuming the stack is tuned.

Applied to LightLayer's lineup:

**Startup (1GB).** One WordPress site with a caching plugin, a static site, a WireGuard endpoint, or a development box you SSH into. 1GB is tight for a full LAMP stack plus a control panel, so budget for a swap file or run the site without a panel. If you are installing cPanel, skip straight past this tier.

**Pay As You Go (2GB+).** Three or four Docker containers, a small Postgres or MySQL instance alongside the app, or two or three low-traffic client sites. This is the tier to pick if you are unsure, because 2GB is where a modern stack stops swapping.

**Mid-Tier (4 cores / 4GB).** A portfolio of client sites, a WooCommerce store with real order volume, or a Node.js app with a background worker. The jump from one core to four matters more than the RAM here; PHP and Node both queue badly on a single core.

**Business (32 cores / 32GB).** Reseller setups, CI runners, or anything doing heavy build or encoding work. Very few readers of a "$4 VPS" article need this, and if you do, compare it against dedicated hardware before committing, because LightLayer also sells dedicated servers and at this spend the math changes.

One rule that saves money: buy the monthly plan first. A $4 month tells you more about whether 1GB is enough than any spec table.

## What you pay in year two

Monthly versus annual is the first half of the cost question. At $4/month, Startup costs $48 over a year. The Manila or Taiwan annual plan costs $24.99 for the same twelve months. You are paying roughly half for the same hardware, which is a straightforward trade for anyone who has already decided to stay.

The second half is the renewal price, and this is where budget VPS shopping usually goes wrong. In 2026 the promotional-to-renewal gap at mainstream hosts is large and well documented: InMotion's self-managed plans renew at 1.9 times the promotional rate on the 4 vCPU plan and 2.7 times on the 16 vCPU plan; Hosting.com's 8GB plan goes from $9.99 to $29 at renewal; HostGator's plans renew at about 2.2 times the promo price. A host that quotes $4 in the headline can be quoting $9 by year two without any change to the spec sheet.

LightLayer's plan pages do not spell out a renewal multiplier the way InMotion does. Ask support, in writing, what the renewal rate on your specific plan and location will be before you prepay for a year, and keep the reply. If the answer is "same as the promotional rate," that is a genuine advantage over most of this list and worth the annual prepay. If the answer is vague, buy monthly.

👉 [See LightLayer's current monthly and annual pricing](https://account.lightlayer.net/?affid=74)

## The refund policy is the part to read twice

LightLayer's refund policy covers provider-side faults only. Third-party refund trackers that log host terms, last verified in November 2026, record it as "provider fault only", with no refund for reasons not attributable to LightLayer, including both regular-priced and promotional products. In practice that means a dead node or a failed provisioning gets you your money back; deciding after nine days that you prefer a different host does not.

That is outside the norm for this price bracket. IONOS, Hostinger, Bluehost and HostGator all list 30-day money-back windows in HostAdvice's provider comparison, and DreamHost advertises 30 days as standard. If a no-questions refund is part of how you buy hosting, LightLayer is not the cheap option, it is the option with no safety net.

The workaround is simple and costs $4: start on the monthly Startup plan, spend two weeks actually using it, and only then convert to annual. You give up about $20 of annual discount in exchange for testing the thing before you commit a year of prepaid time to a policy that will not return it.

👉 [Start on the monthly plan and test it first](https://account.lightlayer.net/?affid=74)

## Managed or self-managed

LightLayer's listed plans are self-managed with root access, and no managed tier appears in its plan lineup. That is fine if "the site is down" means "check the error log" to you. It is not fine if it means "call someone."

The price of the alternative is measurable. InMotion sells two VPS lines on identical hardware in identical data centers: its 8 vCPU / 16GB / unlimited bandwidth plan costs **$21.99/month self-managed** and **$51.49/month managed**. The premium is about 2.3 times for the same box, and what it buys is 24/7 coverage of the operating system, security patching and troubleshooting, rather than just the hardware, network and data center. Whether that is worth roughly $30 a month depends entirely on what an hour of your time costs and how often the server breaks. But it is the number to hold in your head when you compare a $4 plan against a $22 one.

## How LightLayer compares with the 2026 shortlist

| Host | Entry price | Entry spec | Where it wins | Watch out for |
| --- | --- | --- | --- | --- |
| Hostinger | $6.49/mo | 1 vCPU / 4GB RAM | Most polished tooling: AMD EPYC, NVMe, weekly backups, 99.9% uptime, free domain for a year | More RAM per dollar at entry; KVM 2 (2 vCPU / 8GB / 100GB) is $8.99/mo and renews at $14.99 |
| IONOS | ~£2/mo | 1–12 vCPU, 1–24GB RAM | Cheapest entry anywhere, unlimited traffic, easy plan switching | Plesk costs extra, no hand-holding, assumes server knowledge |
| InMotion | $13.99/mo | 4 vCPU / 8GB / 160GB | Managed option on the same hardware, 99.99% uptime, snapshots, free onboarding and migration | Renews at 1.9x on self-managed plans |
| DreamHost | $9.49/mo | 2 vCPU / 8GB / 150GB | Unlimited sites, daily backups, 30-day refund, strong support record | Managed VPS is Ubuntu only; no Windows, no root on the managed line |

Read that table as a set of trade-offs rather than a ranking. LightLayer wins on raw price per gigabyte of RAM at the entry level and on location spread across Asia, which is the reason to pick it if your users are in Manila, Bangkok or Singapore and you want the server nearby. Hostinger wins on tooling and gives you 4GB of RAM for $6.49 where LightLayer gives you 1GB for $4. IONOS wins if the entry price is the only number that matters. InMotion wins when you want to stop being the sysadmin. DreamHost wins if you want a WordPress-optimised managed box with a refund window, and loses immediately if you need Windows, since its managed VPS is Ubuntu only.

On Windows specifically: Hostwinds offers a choice of Linux or Windows and scales to 96GB of RAM, which is the practical pick if your application is .NET and you cannot move it.

## FAQ

**Is a VPS the same as cloud hosting?**
No. A VPS runs on a single physical server partitioned into virtual machines. Performance is stable but capped by that machine, upgrades are manual, pricing is fixed, and a hardware failure on the host can take you down. Cloud hosting spreads across multiple servers, scales automatically, bills by usage and fails over. LightLayer's plans are KVM VPS, so expect the first model: fixed resources, fixed price, manual resize.

**How much cheaper is Linux than Windows?**
PCMag puts the gap at $10–20 per month, with Linux consistently the cheaper licence. LightLayer's plan listings are Linux-oriented; if you need a Windows licence, confirm availability and the added cost with support before ordering rather than assuming it is a checkbox at checkout.

**Does 99.9% versus 99.99% uptime really matter?**
It is the difference between about 43 minutes of downtime a month and about 4 minutes. For a brochure site, 99.9% is fine. For anything taking payments, the extra nine matters, and what matters more is whether the figure is contractual. InMotion promises 99.99%, Liquid Web guarantees 100% on power and network, and LightLayer's plan details do not quote an uptime figure at all. Treat the absence as a reason to keep your own backups rather than a dealbreaker at this price.

**Can I add cPanel later?**
You have root access, so you can install any panel you license. cPanel itself is licensed separately from the server in most setups, and InMotion is a useful reference point here: it lets you add cPanel or CWP at any time on a self-managed plan, billed on top of the server. Ask LightLayer support what panel licensing it can resell and at what price before you assume a $4 server plus a control panel stays a $4 server.

## Which one to buy

One WordPress site, a dev box or a VPN endpoint, and you are comfortable on the command line: **Startup at $4/month**, or the **$24.99/year** Manila or Taiwan plan once you have tested it for a month.

Docker, a database, or two or three small sites: **Pay As You Go from $5.60/month** with 2GB or more. Do not try to squeeze a container stack into 1GB to save two dollars.

Client sites or a store with real traffic: **Mid-Tier, 4 cores and 4GB**, priced by location.

You want a managed server, a Windows licence, or a 30-day refund if you change your mind: buy somewhere else on the list above.

Two things to settle before you pay LightLayer anything: the renewal rate on your exact plan and location, in writing, and whether you are comfortable with a provider-fault-only refund policy. Get both answers and the annual plans are genuinely good value. Skip both questions and you are gambling a year of prepaid time on a number you never checked.

👉 [Compare LightLayer's plans and start with the $4/month tier](https://account.lightlayer.net/?affid=74)
