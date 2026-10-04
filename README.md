# cheap residential proxies: how to compare per-IP and per-GB billing without getting stuck with a bad IP pool

If you have spent an afternoon price-shopping residential proxies, you have probably noticed that every "cheapest providers" list compares the same number: dollars per gigabyte. That number is useful, but it is only half the story. A provider charging $1/GB will beat a provider charging $3/GB on paper, right up until you push 300 GB through a single IP and realize the second provider would have charged you $24 flat.

So before comparing brands, it is worth understanding that "cheap" in this market is mostly a billing-model question. Below is how the two common models actually behave, what 9Proxy charges for each of them right now, and how to work out which one costs less for the traffic you genuinely generate.

## The two billing models, and the trap in each

Per-GB billing charges for data. You buy a block of traffic, it gets consumed as requests pass through rotating residential IPs, and when the block runs dry you buy another. Small projects love this because the entry cost is tiny: $5 for 5 GB, for example.

The trap is that page sizes change without your permission. A site adds tracking scripts, images get heavier, you start rendering JavaScript, and suddenly the same 100,000 requests cost three times what they did last month.

Per-IP billing charges for addresses instead. You buy a fixed number of residential IPs, each with unlimited bandwidth, and the cost stays flat whether those IPs move 5 GB or 500 GB. The trap here is the mirror image: if your task is 2,000 rotating requests totalling 1 GB, buying IPs is wildly expensive. You paid for addresses you barely use.

Neither model is cheaper in the abstract. What makes one cheap is the ratio of traffic to IP count in your workload.

## What 9Proxy charges, and the price change you should know about

9Proxy (9proxy.com) runs both models, plus combined bundles, and it is one of the few budget-tier providers that lets you pick. Its network is advertised at 20 million-plus residential IPs across 90-plus countries, with targeting down to country, city, ZIP code and ISP level, and support for HTTP/HTTPS and SOCKS5.

One thing to flag before the tables: 9Proxy announced its first-ever price adjustment on 18 May 2026, effective 1 June 2026. IP-based packages and bundle packages went up. GB-based packages were left untouched. The prices below are the post-adjustment ones, which is what matters if you are buying today.

### IP-based packages (unlimited bandwidth per IP)

| Package | Price per IP | Total | Get it |
| --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | Order the 100 IP pack |
| 500 IPs | $0.144 | $72 | Order the 500 IP pack |
| 1,000 + 500 bonus IPs | $0.084 | $126 | Order the 1,500 IP pack |
| 2,500 IPs | $0.084 | $210 | Order the 2,500 IP pack |
| 5,000 IPs | $0.072 | $360 | Order the 5,000 IP pack |
| 15,000 IPs | $0.048 | $720 | Order the 15,000 IP pack |
| 25,000 IPs | $0.035 | $863 | Order the 25,000 IP pack |
| 50,000 IPs | $0.029 | $1,438 | Order the 50,000 IP pack |
| 100,000 IPs (business) | $0.023 | $2,300 | Order the 100,000 IP pack |
| 200,000 IPs (business) | $0.021 | $4,140 | Order the 200,000 IP pack |
| 500,000 IPs (business) | $0.018 | $8,625 | Order the 500,000 IP pack |

Two details matter more than the headline numbers. First, IPs bought this way do not expire, so unused balance keeps. Second, each IP in a per-IP plan stays usable for a few hours up to roughly 24 hours — these are real household connections, and the person behind one can unplug their router at any time.

### GB-based packages

| Package | Price per GB | Total | Traffic validity | Get it |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days | Buy the 5 GB pack |
| 50 + 5 bonus GB | $2.10 | $105 | 180 days | Buy the 55 GB pack |
| 100 GB | $1.50 | $150 | 180 days | Buy the 100 GB pack |
| 200 GB | $1.00 | $200 | 180 days | Buy the 200 GB pack |
| 1,000 GB | $0.80 | $800 | 180 days | Buy the 1,000 GB pack |
| 2,000 GB | $0.75 | $1,500 | 180 days | Buy the 2,000 GB pack |
| 3,000 GB (enterprise) | $0.72 | $2,160 | No expiry | Buy the 3,000 GB pack |
| 6,000 GB (enterprise) | $0.70 | $4,200 | No expiry | Buy the 6,000 GB pack |
| 10,000 GB (enterprise) | $0.68 | $6,800 | No expiry | Buy the 10,000 GB pack |

The 180-day window on the regular GB packs is generous compared with monthly subscriptions, but it is still a deadline. The 3,000 GB-and-up enterprise packs remove it entirely, which is the honest reason they cost more per gigabyte than you might expect for the volume.

### Bundle packages (IPs plus traffic)

| Bundle | What is included | Price | Traffic validity | Get it |
| --- | --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | 180 days | Order the Starter Bundle |
| Popular | 1,500 IPs + 50 GB | $180 | 180 days | Order the Popular Bundle |
| Pro | 5,000 IPs + 500 GB | $720 | 180 days | Order the Pro Bundle |

The Pro bundle has a listed price of $860 with a 16.28% discount bringing it to $720, so the saving is $140 if you are comparing against buying the components. Bundles make sense when one project needs both stable sessions and high-volume rotation, which happens more often than the separate plans suggest.

## Which one is actually cheaper for your workload

Three quick scenarios, using the prices above.

**Heavy bandwidth, few IPs.** You keep 80 browser profiles alive and push about 300 GB a month. The 100 IP pack costs $24. That works out to roughly $0.08 per GB, and it does not change if your pages get heavier. A $1/GB provider would bill $300 for the same 300 GB. This is where the per-IP model stops looking expensive and starts looking like the cheapest residential capacity on the market.

**Light traffic, many IPs.** You want to check how a landing page renders across 20,000 different US locations, and the whole job moves 5 GB. The 5 GB pack costs $15. Buying IPs at that scale means the 25,000 IP pack at $863. Per-GB wins by a factor of fifty.

**Steady middle.** 200 GB through 50 sessions that you want to keep alive. The 100 IP pack is $24, so under $0.12 per GB effective. The 200 GB pack is $200. Per-IP again, unless the traffic is spiky enough that you would rather not think about session management.

The pattern is consistent: the more data each individual IP moves, the worse per-GB billing looks. Rotation-heavy, low-payload work is the reverse.

## What you give up by going cheap

Every budget residential network trades something away, and it is worth being specific rather than vague.

Dynamic residential IPs are not permanent. A review on Trustpilot's French-language page for 9Proxy complained that purchased IPs stopped working after about an hour and caused security flags on the user's accounts. 9Proxy's own support reply acknowledged the cause: these are real users' connections, so when the original owner disconnects, the IP goes offline. Their recommendation was to switch to static ISP proxies for workflows that need one fixed identity over a long session. That is a fair answer, and it is also a genuine limit of the whole product category, not just this vendor.

Trustpilot feedback is split by regional page. The Australian page shows a 4.6/5 "Excellent" rating dominated by reviews about speed and the replacement policy, while the French-language page sits far lower with 2/5, concentrated on the instability complaint above. Reading both is more useful than reading either. What they agree on is that support answers, which matters when a batch of IPs dies mid-project.

Third-party benchmark data is middling rather than spectacular. ProxyLook's comparison pages list 9Proxy at 3.9/5 with a 97% success rate and an average response time around 1,300 ms. That is respectable for the price tier and below what you would expect from enterprise providers charging three or four times more per gigabyte.

Support and billing are the areas where the cheaper providers usually cut hardest, and here 9Proxy does not. Payments include credit cards, bank cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), Alipay, Apple Pay and Google Pay. Support runs around the clock through Telegram, email and a ticket system. New users can request a limited trial subject to availability, and you have to say whether you want an IP-based or GB-based trial when you ask — the trial is not a self-serve button.

There is also a referral setup worth knowing about: signing up through an invite link includes a 5% discount for the referred user, and the affiliate programme behind it pays out up to 15% in commission by crypto. If you are buying anyway, there is no reason to pay full price for the privilege.

## How 9Proxy's headline prices compare

| Provider | Cheapest entry | Scaling price | Pool | Billing model |
| --- | --- | --- | --- | --- |
| 9Proxy | $15 for 5 GB ($3/GB); $24 for 100 IPs | $0.68/GB at 10,000 GB; $0.018/IP at 500,000 IPs | 20M+ IPs, 90+ countries | Per-GB, per-IP with unlimited bandwidth, or bundles |
| Webshare | $3.50/GB at 1 GB | $1.40/GB at 3,000 GB | 80M+ IPs | Per-GB, plus static residential from $6/month |
| DataImpulse | $5 for 5 GB ($1/GB) | $0.80/GB at 1 TB | 90M+ IPs, 195 countries | Per-GB, non-expiring traffic |
| Decodo | $2/GB | Volume discounts at 1,000 GB+ | 115M+ IPs, 195+ locations | Per-GB with 3-day, 100 MB trial |
| IPRoyal | ~$7/GB | ~$1.75/GB in bulk | 195+ countries | Per-GB, pay-as-you-go |
| PacketStream | $1/GB | Flat $1/GB | US and Europe focused | Per-GB, P2P network |
| GeoNode | $49/month flat | ~$0.49/GB effective if fully used | 140+ countries | Flat rate with 10 concurrent threads |

Read that table with one thing in mind: the per-GB column tells you nothing about what you will pay for a bandwidth-heavy job. DataImpulse at $1/GB looks cheaper than 9Proxy's $3/GB entry, until the workload involves 300 GB through a small set of stable IPs, where 9Proxy's $24 IP pack produces an effective rate around $0.08/GB. Different question, different winner.

## Getting set up without overbuying

The signup path is straightforward. Create an account, pick a package, then choose how you want to connect: a Windows client that routes traffic at the OS level, Proxy2Web for browser-based use with plain username and password authentication, ProxyHub for mobile device management, or the API if you are wiring proxies into a pipeline. SOCKS5 support means anti-detect browsers and custom scripts connect without protocol conversion — reviewers on AlternativeTo mention Dolphin Anty and AdsPower specifically.

Two features quietly cut the real cost. A "Today List" lets you reuse IPs from the previous 24 hours at no extra charge, which 9Proxy estimates saves 20 to 30 percent on typical workloads. Auto-refresh detects and replaces offline IPs within about 60 seconds, so you are not manually hunting through a list for dead addresses. Combined with the replacement policy for non-working proxies, the practical cost per usable IP is lower than the list price suggests.

If you are not sure which model fits, buy the smallest pack in the model you suspect is right and measure. One week of real traffic tells you more than any comparison table, including this one. 👉 Create a 9Proxy account and check the current rates before the next pricing round.

## Questions people ask before buying cheap residential proxies

**Does a cheap residential pool mean more blocks?** Pool size and IP reputation matter more than price, but they correlate. A 20-million-IP pool with a focus on clean addresses is workable for scraping mainstream sites. For heavily protected targets, success rate data from independent benchmarks is worth checking before you commit to volume.

**Can I test before paying?** 9Proxy runs a limited trial for new users when availability allows, and you need to specify IP-based or GB-based when requesting it. Several competitors offer self-serve trials, including Decodo's 3-day, 100 MB option, so if a guaranteed trial is non-negotiable, that is a real difference.

**Do unused IPs or traffic expire?** IPs purchased on IP-based plans do not expire, and enterprise GB packs from 3,000 GB upward have no expiry either. Regular GB packs and bundle traffic are valid for 180 days.

**What if the IPs stop working mid-project?** That is what the replacement policy covers, and it is why 24/7 support matters at this price tier. For long sessions that need one stable identity, the honest answer is that rotating residential pools are the wrong tool, and you want static ISP proxies instead.
