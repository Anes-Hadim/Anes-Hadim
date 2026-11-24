## Hadim Anes Abdelhak

Fourth-year engineering student at **ESI Algiers** (École Nationale Supérieure
d'Informatique), specialising in **Systèmes Informatiques**. I work on the layer
most people never see — event loops, cache eviction, queue delivery guarantees,
load balancing. Vice-president of **Shellmates**, ESI's cybersecurity club.

**[anes-hadim.vercel.app](https://anes-hadim.vercel.app)**

---

### Systems I built to understand them

Each one started as a question I could not answer by reading about the real
thing. They are small on purpose — one idea each, tested, measured, and honest
in the README about what they do *not* do.

| | | |
|---|---|---|
| **[nanocache](https://github.com/Anes-Hadim/nanocache)** | Redis-protocol cache server in C. O(1) LRU via entries linked into both the hash chain and a recency list, so the eviction victim never needs searching. | `755k SET/sec`, p99 1.4 µs |
| **[hashring](https://github.com/Anes-Hadim/hashring)** | Consistent hashing with virtual nodes and bounded loads, plus xxHash32 from scratch. | `10.9%` of keys move to add a node — vs modulo's `88.9%` |
| **[taskq](https://github.com/Anes-Hadim/taskq)** | Durable job queue on an append-only log. CRC-32 framing, so recovery tells a written record from a torn one. Leases instead of pops. | `34` tests, none of which sleep |
| **[minilb](https://github.com/Anes-Hadim/minilb)** | L7 load balancer. nginx's smooth weighted RR, peak-EWMA with power-of-two-choices, half-open circuit breaker. | `37` tests over real sockets |
| **[saga-shop](https://github.com/Anes-Hadim/saga-shop)** | Three services, three databases, no shared transaction. Orchestrated saga with compensating actions + transactional outbox. | `24` tests |

All five are dependency-free and documented with the reasoning, the measured
numbers, and a **Known limits** section.

### Competitions — now with the code

**[radarml-track2](https://github.com/Anes-Hadim/radarml-track2)** · *1st place,
Synapson Datathon (IEEE)* — radar modulation classification across 13 SNRs on
UCL ARESTOR recordings. I built two pipelines and **submitted the one that
scored worse**: a Fourier template bank hit 0.9962 balanced accuracy but was
perfect at every SNR from −25 dB up, which is physically implausible below the
noise floor. It had 660 templates for the dataset's 660 configurations — it was
re-identifying source recordings, not classifying modulation. The rejected code
is in the repo so the reasoning can be checked.

**[riverload-c2](https://github.com/Anes-Hadim/riverload-c2)** · *2nd place,
Odyssia Datathon* — forecast the Rhine's depth, then load a ship. The forecast
is a constraint generator, not the deliverable, so the loss is asymmetric:
quantile LightGBM on pinball loss, three blended forecasters, forward-only
backtesting, and a MILP for cargo under mass, trim and deadline constraints.

### Elsewhere

- Infrastructure &amp; deployment internship — Ubuntu Server, Nginx reverse
  proxy, MariaDB for a three-tier application
- Cisco CCNA — Switching, Routing and Wireless Essentials

### Stack

`C` `Java` `JavaScript` `SQL` · `Linux` `Nginx` `Docker` `Kubernetes` ·
`Node.js` `Express` `React` `Next.js` · `PostgreSQL` `MySQL` `MariaDB` `MongoDB`

---

<sub>Much of my 2025–26 work lives in private and organisation repositories —
a school-management platform, an event administration platform, club projects
and datathon notebooks — so this profile shows less than the work does.</sub>
