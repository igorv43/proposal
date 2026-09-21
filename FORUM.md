<!-- Forum version: identical text to README.md, with the Mermaid diagrams replaced by PNG images. Regenerate after editing README.md. -->

# Terra Classic Liquidity Fabric

## A proposal to the community, validators and investors

| | |
|---|---|
| **Version** | 1.1 — September 2026 |
| **Technical basis** | Specification v0.8.1, with recorded decisions (D-01 to D-22) and public verifications (G-01 to G-11) |
| **Discussion** | https://github.com/igorv43/proposal/issues |
| **Author** | Igor Veras — https://github.com/igorv43 · https://x.com/igorsoares62 |
| **Portuguese version** | https://github.com/igorv43/proposal/blob/main/PROPOSTA-PT.md |

> **How to read this document.** Sections 1–3 explain *what* and *why* in plain
> language. Section 4 explains *how it works*. Sections 5–7 cover the business
> model and where the money goes. Sections 8–11 cover the roadmap, governance,
> risks and what is being asked. Section 13 answers the questions readers ask
> first. A glossary is at the end. Source and discussion:
> https://github.com/igorv43/proposal

---

## Summary in five lines

We propose turning Terra Classic into **multichain financial infrastructure**:
native liquid staking, perpetual markets executed by single-price auction, and
access from any wallet on any chain with one signature — all under a rule no
competitor can copy: **backing and solvency are proven in consensus, every
block, instead of promised in documentation.** The user interfaces belong to the
DEXes and wallets that integrate, charging their own fee; the chain keeps the
protocol fee, whose surplus feeds **50 % the Oracle Pool, 20 % the Community
Pool and 30 % LUNC burn**. This request covers only the foundation and liquid
staking; the perpetuals layer returns to the floor with its own gates met.

### The whole idea in one picture

![The whole idea in one picture: the productive circuit of the stake](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/01-circuit.png)

*Everything runs on the asset's own chain, under solvency rules enforced by
consensus. No competitor can assemble this circuit: none of them is the home of
LUNC.*

---

## 1. The identity of the project

**The chain provides the infrastructure. The interfaces belong to whoever integrates.**

The Liquidity Fabric is not an app, not a DEX, not another website. It is the
layer of assets, accounts, execution, collateral and proof that applications on
every chain use — and pay for. The ones who find the customer and do the
marketing are the platforms that already have users: Terra Classic's own DEXes,
and the wallets and DEXes of Solana, BNB Chain and Ethereum.

And the thesis that runs through everything: **backing that is proven, not
promised.** Terra Classic is the chain whose collapse taught the whole industry
the cost of backing that could not be verified. This project is the exact
inversion of that — and no competitor can tell this story with credibility,
because none of them lived it.

---

## 2. The four pains of today

| Pain | Who feels it |
|---|---|
| **Staked capital is dead capital.** 21 days of unbonding; stakers cannot use their own money for anything | Every LUNC delegator |
| **No native derivatives.** Hedging and leverage on LUNC only on CEXes or other chains — the volume leaves with the user | Traders and the chain itself |
| **Getting in is hard.** A user on Solana, BNB Chain or Ethereum needs a bridge, a new wallet and new gas before the first transaction | Every outside user |
| **LUNC is fragmented out there.** Different representations on each network, with no public accounting proving the backing of each | Everyone holding LUNC off-chain |

Scale context: the chain's combined DeFi TVL is around **US$ 850 thousand**, with
daily DEX volume of a few thousand dollars (DefiLlama, Sep 2026). This project
does not compete for that slice — it creates a layer that is approximately zero
today: derivatives and multichain access.

![Today vs. with the Fabric](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/02-pains-vs-fabric.png)

---

## 3. What will be built

Six layers, one product:

| Layer | What it delivers |
|---|---|
| **Multichain assets** | Canonical LUNC, with an auditable representation on each network |
| **Multichain accounts** | Any wallet operates with one signature, no manual bridging |
| **Trust** | Backing verified in consensus every block, with automatic pause |
| **Execution** | Single-price auction and perpetuals with protections written on-chain |
| **Native capital** | stLUNC as neutral collateral that never votes for anyone |
| **Distribution** | DEXes and wallets integrate, charge their own fee and bring the customer |

![The six layers](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/03-six-layers.png)

---

## 4. How it works, without jargon

### 4.1 Backing that is proven

The rule is an equation the chain checks every block:

> **LUNC locked here = LUNC represented out there + LUNC in transit.**
> If the numbers do not match, the route pauses by itself.

![Proof of backing: locked = represented + in transit, or the route pauses](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/04-proof-of-backing.png)

The solvency page is public: anyone can check, per network, how much is
represented, how much is locked, the headroom against the cap and the history of
pauses — **including the false alarms**, because a record that only shows
successes is not a record. The observer software is open source: "anyone can
verify" only holds if anyone actually can.

### 4.2 One price for everyone

![Single-price auction in three steps](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/05-single-price-auction.png)

The position of an order inside the block stops being worth money: no bot wins
by arriving first — not even the one producing the block. The same engine
executes the perpetuals and any spot market governance may enable later, with no
new code.

### 4.3 The account comes to the user

![Multichain access: one signature from the user's own wallet](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/06-multichain-access.png)

The user does not know there is a bridge — and does not need to. Every
integrated wallet on another network becomes an entry channel into Terra Classic.

### 4.4 Protection lives on the chain, not in the browser

- **Stop and target written on-chain:** they trigger by themselves, even with
  the investor offline, without internet, with the app closed.
- **Withdrawals with a locked destination:** funds only leave to the owner's own
  wallet. Not even a forged bridge message can steal — a bridge compromise
  becomes an inconvenience, not a loss.
- **Delay never becomes loss:** a slow message stays pending until it arrives,
  and anyone can deliver it, including the user, through the redelivery button.
- **Cap by real liquidity:** no market can grow beyond the depth measured by the
  oracle — the rule that prevents the class of attack that constrained the
  sector leader. And LUNC-PERP will be the **last** market, with the most
  restrictive parameters, not the first.
- **Orders never cross the bridge:** bridge congestion does not delay a single
  trade.
- And the mandatory honesty: **market risk is not reversible** — no venue in the
  world reverses a price move, and this proposal will not say otherwise. What we
  guarantee is that delay never becomes loss of principal and that defending a
  position does not depend on human reflexes.

![Protection on-chain: stop and target executed by the chain](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/07-onchain-protection.png)

---

## 5. The business model: they sell, the chain earns

![Integrator model: they charge on top, the chain earns the protocol fee](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/08-integrators.png)

The industry precedent validates the model: the leading on-chain perpetuals venue
outsourced distribution to more than a hundred integrators; Solana's Phantom
wallet routed tens of billions of dollars and earned more than US$ 20 million in
about a year charging 0.05 % on top — without building an exchange (sources:
public reports on the builder-codes program — CoinGecko Research, Blockworks,
2026).

And the rule that guarantees we will never compete with those who distribute us,
written in code: **the protocol's own interface does only custody, proof of
solvency and exit** — close position, cancel, withdraw. Opening a position does
not exist in it. Without opening, it never competes for a single trade; with
guaranteed exit, no user is ever stuck depending on a third-party interface to
escape a position.

Launching perpetuals requires **at least two integrators in production** —
without interfaces there is no product, and the gate makes that literal. The
integration kit (template, widget, SDK and sandbox) is open and cuts integration
cost to days.

---

## 6. Those already building here come out ahead

| Project | Today | With the Fabric |
|---|---|---|
| **Terraport** | DEX, staking, launchpad | Perpetuals front end with their own fee on top, without building an exchange |
| **GarudaDefi** | AMM and farms | Same new revenue line, plus better pairs with the canonical assets |
| **Terraswap** | The chain's original AMM | New arbitrage volume coming from the internal auction |
| **Eris and other LSTs** | Liquid staking in contracts | Multichain routes for their tokens; declared coexistence, nothing is disabled |
| **Validators** | Rewards shrinking with a low Oracle Pool | 50 % of the protocol surplus refills the Oracle Pool, and stLUNC keeps the stake delegated |

On native liquid staking: it exists because the liquidation path of the
perpetuals requires an asset from the chain's own bank module, with no
third-party contract in between — and because **the system's collateral must be
neutral: the module never votes**, with a per-validator cap and a global cap.
Everyone's collateral cannot be anyone's voting machine — including this
project's. Existing LSTs keep operating and gain multichain routes if they want.
**Process commitment:** direct conversation with the chain's teams before any
vote.

---

## 7. Where the revenue goes: the waterfall

![Revenue waterfall](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/09-revenue-waterfall.png)

![Surplus split: 50 % Oracle Pool, 20 % Community Pool, 30 % burn](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/10-surplus-split.png)

Three rules accompany the waterfall, and all three are code:

1. **Burn is paid by profit, never by security.** Nothing is burned or passed on
   while the insurance fund is below target. This is non-governable.
2. **No target, no number, no promise.** The burn figure is whatever the surplus
   pays, and the on-chain history is the only advertising.
3. **Burn is never a price argument.** Communicating the waterfall is allowed;
   promising an effect is not.

And there is burn even before the perpetuals: **20 % of the liquid-staking fee
burns LUNC directly, with no conversion, from the stLUNC stage** — small at
first, real from day one, growing with TVL. Beyond the waterfall, all the new
volume the Fabric generates pays gas and goes through the current on-chain tax,
feeding the burn and the Community Pool that **already exist**.

---

## 8. Roadmap by gates, not by dates

![Roadmap by gates](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/11-roadmap-gates.png)

| Stage | Deliverable | Advances only if |
|---|---|---|
| **Foundation** | Native Hyperlane, canonical LUNC, migration of the old representations, public proof of backing | Audit completed; the equation closes block by block |
| **Liquid staking** | stLUNC with its own revenue and direct burn active | Dedicated audit; 30 days of clean invariants |
| **Demand gate** | Letters from 3 independent market makers + legal opinion | Without signed commitments, perpetuals do not start |
| **Incentivized testnet** | Auction engine + perpetuals + extended oracle | 60 days of metrics met; zero invariant violations |
| **BTC-PERP on mainnet** | First market, low cap | **At least 2 integrators in production** |
| **Expansion** | ETH-PERP, stLUNC as collateral, LUNC-PERP last | Continuity criteria measured at 6 months |

Estimated effort: foundation **4.5–7.5 engineer-months**; complete financial
layer **27–41**, plus audits with their own budget. Every stage has an honourable
stopping point: a project that delivers the foundation and liquid staking, and
stops there, has delivered real value.

The chain runs Cosmos SDK v0.53, which allows integrating the official Hyperlane
modules by composition, without rewriting — the most important technical premise
is already confirmed.

---

## 9. Who decides what: governance and organization

![Governance and organization](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/12-governance.png)

- **Governance** approves scope and budget per milestone and can change
  governable parameters; it cannot change the non-governable limits.
- **The core team** delivers by gates; a minimum team is a gate condition, not a
  recommendation.
- **Integrators, market makers and legal counsel** are external and independent;
  their commitments are gates, not assumptions.
- **Anyone** can verify the state of the system: the observer software is open
  and the solvency page is public.

---

## 10. The risks, said up front

| Risk | How the design answers |
|---|---|
| Demand does not show up | Gates: nothing advances without signed commitments; the foundation already delivers value on its own |
| Dependence on integrators | Launch requires 2 in production; the ready kit cuts integration to days; the console guarantees exit always |
| Bridge failure or delay | Orders do not cross the bridge; value in transit is never lost; 5 independent signers, tolerates 2 down |
| Market manipulation | Position caps limited by real depth, verified in code; LUNC-PERP last and restricted |
| Regulatory | Legal opinion is a mandatory gate before any market; distributed interfaces, neutral protocol |
| The investor's market risk | **Not reversible, and this proposal will not say otherwise.** What we guarantee: delay never becomes loss of principal, and protection does not depend on human reflexes |
| Execution and concentration | Minimum team is a gate condition, not a recommendation; the public specification allows continuity by third parties |

---

## 11. What this proposal asks

1. **Approval of the scope of the Foundation and liquid staking** (stages 0 to
   6), with a budget of **[BUDGET]** and a team of **[TEAM]**, released by
   auditable milestones — not a cheque, a sequence of verifiable deliveries.
2. **Recognition of the allocation waterfall** — fund up to target, operations
   with a cap, and the surplus 50 % Oracle Pool / 20 % Community Pool / 30 %
   burn — as a commitment in code, queryable by anyone, epoch by epoch.
3. **A mandate for the integration conversations** with the chain's own teams
   (Terraport, Garuda, Terraswap, Eris) and with outside wallets and DEXes, and
   for the pilots with market makers — all before any line of the perpetuals
   layer.

The perpetuals layer **returns to the floor** with its own gates met: signed
commitments, legal opinion and a measured testnet. Nobody is asking for approval
of promises.

---

## 12. Permanent transparency

- The complete technical specification (v0.8.1) is public: every decision has a
  record, discarded alternatives and a review trigger; every external dependency
  has a verification procedure and a consequence.
- All accounting — backing per network, revenue waterfall, accumulated burn — is
  queryable on-chain and shown on the public solvency page.
- Critical limits are **non-governable**: absolute maximum leverage, insurance
  fund not withdrawable to treasury, withdrawal locked to the owner, burn only
  from surplus.

---

## 13. Frequently asked questions

These are the questions that come up first when the proposal is read. Each one
has a short answer, the detail, and the part that must be said honestly.

### 13.1 Why is liquid staking tied to the perpetuals?

**Short answer:** they do not depend on each other to work, but each makes the
other much stronger. They are two products that stand alone and form a circuit
when connected.

![FAQ: stLUNC and the perpetuals stand alone and form a circuit](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/13-faq-stlunc-perpetuals.png)

**What it is NOT:** a dependency. Liquid staking launches at stage 6, before any
perpetual, with its own revenue (the 5 % fee on staking rewards) and the direct
burn active. If the perpetuals never left the drawing board, stLUNC would keep
delivering value on its own. The reverse also holds: BTC-PERP launches at stage
9 accepting only USDC as collateral; stLUNC as collateral enters only at stage
10, after a real liquidation cycle has been observed. The roadmap was designed
this way on purpose.

**Why they are connected — the circuit creates value in both directions:**

- *The perpetual gives stLUNC utility.* A liquid-staking token is only worth
  something if there is somewhere to use it. Serving as collateral is the
  strongest use there is: the stake keeps earning staking rewards while it works
  as margin. No CEX offers that for LUNC — there, to trade you redeem and stop
  earning.
- *stLUNC gives the perpetual capital.* The chain's largest stock of native
  capital is delegated LUNC. Without stLUNC, the only collateral is outside
  USDC, which has to be attracted. With stLUNC, capital that already exists on
  the chain can fund the venue without leaving staking.
- *The security detail that ties it together:* because the collateral is liquid
  stake (not loose LUNC), using the venue never requires undoing a delegation.
  The perpetual does not drain consensus security — it reinforces it, by adding
  one more reason to delegate.

**Why the link is restricted — the honest part.** stLUNC as collateral carries a
classic risk, *wrong-way risk*: if LUNC falls, the value of the collateral falls
at exactly the moment the position may be losing. Hence the hard rules of
decision D-16:

| Rule (D-16) | Value |
|---|---|
| Markets stLUNC may collateralize | BTC and ETH only — **never LUNC-PERP** (collateral and asset falling together would be the perfect trap) |
| Haircut on stLUNC value | 35 % |
| Cap per account | 50 % of the account's collateral |
| Insurance fund | separate tranche for stLUNC-backed positions |

**The technical link that explains a decision.** The reason liquid staking is a
native module (and not the contract LSTs that already exist) comes precisely from
the perpetual: the liquidation path must seize and price the collateral with no
third-party contract or admin key in between. The perpetual did not create the
need for liquid staking; it defined how liquid staking must be built so the two
can connect safely later.

*An analogy:* stLUNC is a term deposit that keeps paying interest; the perpetual
is the bank that accepts that deposit as margin without you cashing it out. The
bank works without accepting deposits, and the deposit pays without any bank —
but together, the money works twice.

### 13.2 Who funds the liquidity for withdrawals? Does the community need to put money in?

**Short answer:** nobody needs to fund it, and the community puts in nothing —
because none of the three kinds of withdrawal in the system depends on a
liquidity pool. The budget this proposal asks for is for engineering and audits,
not for liquidity.

![FAQ: the three withdrawal paths need no liquidity pool](https://raw.githubusercontent.com/igorv43/proposal/main/diagrams/14-faq-withdrawals.png)

**1. Redeeming stLUNC for LUNC (the liquid-staking case).** The redemption is
not a swap — it is the chain's normal staking unbonding. Each stLUNC corresponds,
by construction, to LUNC actually delegated plus accumulated rewards; the module
does not lend, rent or rehypothecate anything. When you redeem, the module
enters the staking module's own unbonding queue and, after about 24 days (the
processing epoch plus the chain's 21-day unbonding), your own LUNC, which was
delegated the whole time, comes back to you. There is no liquidity to fund
because the money never left — the waiting time is precisely the proof. A
redemption that was instant and unlimited is what should be frightening: it would
mean the backing is not really staked.

Three honest complements: (a) a buffer of about 2 % of deposits stays
undelegated to serve small redemptions immediately — formed by the deposits
themselves, not by any contribution; (b) whoever does not want to wait 24 days
sells stLUNC on the secondary market (pools on the chain's DEXes — more revenue
for them), where the liquidity comes from voluntary LPs with an economic
incentive: if stLUNC trades below redemption value, arbitrageurs buy at a
discount and redeem through the slow path, and their profit is what pulls the
price back; (c) in a market panic the secondary discount can widen — an
immediate exit may be expensive, but full redemption through the slow path
remains guaranteed by the backing, always.

**2. Bridge withdrawals.** Lock-and-mint model: every LUNC represented outside
has LUNC locked here (the invariant the chain checks every block). Withdrawing
is burning the representation and releasing what was already locked. No pool,
no contribution — backing.

**3. USDC withdrawals from the perpetuals.** The collateral belongs to the user,
segregated in their account; withdrawing is returning what is theirs through the
route back. What needs protection is not the withdrawal but the solvency of the
whole (one trader's gain is paid by another's loss), and that is the role of the
insurance fund, fed by the protocol fee (the first step of the waterfall, before
Oracle Pool, Community Pool and burn), not by contributions. Launch starts with
low position caps precisely so the fund requirement is small at first and grows
with revenue. If the fund were exhausted in an extreme event, the final backstop
is ADL (auto-deleveraging) — a pre-published, deterministic rule — and never a
capital call to the community.

**The political question, answered directly.** Market liquidity (LPs in the
stLUNC secondary market, market makers in the perpetuals) comes from
participants with their own profit motive — which is why the gate of three
market-maker letters exists before any perpetual: the project does not launch
counting on liquidity that has not committed in writing. If one day the
community wants to accelerate with LP incentives, that would be a separate,
optional proposal — the design works without it.

**And if everyone withdraws at the same time?** stLUNC: everyone enters the
unbonding queue and everyone receives their own LUNC after the waiting period;
the secondary price may fall meanwhile, the backing does not. Bridge: every
wrapper burns against LUNC already locked, one for one. Perpetuals: each
account withdraws its own segregated collateral; open positions are governed by
the published risk rules.

### 13.3 Perpetuals — are we talking about leverage or not?

**Short answer:** yes. Leverage is the heart of the product, and this proposal
says so plainly. What it also says: leverage here is a dial, limited in code to
conservative levels, with the stop written on-chain and liquidation by a
published rule.

**What a perpetual is.** A contract in which you take a position on the price of
an asset (BTC, ETH) without ever owning it, with no expiry date, depositing only
a margin — and that is where leverage comes in: the position can be larger than
the margin. With 100 USDC of margin at 2×, you control a 200 USDC position. If
BTC rises 5 %, you gain 10 USDC — 10 % on your capital; if it falls 5 %, you lose
the same 10. Leverage multiplies both sides. The "perpetual" in the name comes
from never expiring: instead of a dated futures contract there is *funding* — a
periodic payment between longs and shorts that keeps the contract price glued to
the spot price. And if the market moves against you beyond what the margin can
absorb, *liquidation* closes the position by force before the loss exceeds the
deposit — that is what the insurance fund, ADL and the whole risk apparatus of
the specification exist to manage.

**Leverage is a dial, not an obligation.** Trading at 1× — position equal to
margin — is possible and is simply price exposure with no multiplier. The design
is deliberately conservative on the dial:

| Market | Leverage at launch | Absolute cap (in code, non-governable) |
|---|---|---|
| BTC-PERP, ETH-PERP | 3× | 10× |
| LUNC-PERP (last market) | 2× | 10× |
| Industry reference | 50×, 100× or more | — |

This is an identity decision: on a chain whose biography is a collapse, a 100×
casino would be narrative suicide. The selling point was never "leverage more";
it is "trade where solvency is proven".

**Why have leverage at all, and not just spot?** Three reasons:

1. **Hedging** — the most defensible use: whoever holds LUNC or BTC and fears a
   fall can protect themselves short without selling the asset (and here,
   without even undoing the staking). That only exists with a derivative.
2. **Capital efficiency** — a market maker providing liquidity on margin can
   quote far more with the same capital; without it there is no competitive
   liquidity.
3. **The cold fact of the market** — perpetuals are where real on-chain volume
   is; it is the product that brings integrators and traders, and volume is what
   feeds the waterfall (Oracle Pool, Community Pool, burn).

**Spot in the same engine.** A spot market is the same auction with no leverage:
you deposit the full amount and exchange the full asset. That is why spot became
an "optional market type" — it is the special case of the engine with the dial at
zero. The perpetual is the general case, with margin.

**The honest sentence for the floor:** yes, it is leverage — limited in code to
conservative levels, with the stop written on-chain, liquidation by a published
rule and never above what the real depth of the market supports. Leverage
without those limits is what breaks protocols; leverage with those limits is
what pays the burn.

---

## Closing

> **The chain that fell because of backing no one could see will become the
> reference for backing that is proven.**

The community does not need to trust this text. It can read the code, query the
chain and verify every number — and that is exactly the proposal.

**Discussion and contact:** https://github.com/igorv43/proposal/issues · [Igor Veras on X](https://x.com/igorsoares62)

---

## Glossary

| Term | Meaning |
|---|---|
| **LUNC** | Luna Classic, the native coin of the Terra Classic blockchain |
| **stLUNC** | Liquid-staking token: represents staked LUNC, keeps earning, can be used as collateral, and the module behind it never votes |
| **Perpetuals (perps)** | Derivative contracts with no expiry, used for hedging or leverage |
| **Single-price auction** | Orders are collected in a batch and all fill at one clearing price; being first in the block gives no advantage |
| **Collateral / haircut** | Assets pledged to back a position; the haircut is the discount applied to their value for safety |
| **Insurance fund** | Reserve that absorbs losses before anyone else; filled before any surplus is distributed |
| **Oracle Pool** | The pool that pays Terra Classic validators for oracle work; a share of the surplus refills it |
| **Community Pool** | Terra Classic's on-chain treasury, controlled by governance |
| **Hyperlane** | The interoperability protocol used for messages and asset transfers between Terra Classic and other chains |
| **Canonical LUNC** | The single official representation of LUNC on each external network, with backing proven on-chain |
| **Invariant** | A rule the system must never break (e.g. locked = represented + in transit); a violation pauses the route |
| **Gate** | A verifiable condition that must be met before the next stage starts |
| **TVL** | Total value locked in a protocol or chain |
| **LST** | Liquid-staking token (e.g. Eris's) |
| **Market maker** | A firm that continuously quotes buy and sell prices, providing liquidity |
| **Leverage** | Holding a position larger than the margin deposited; multiplies gains and losses alike |
| **Margin** | The collateral deposited to open and keep a leveraged position |
| **Funding** | Periodic payment between longs and shorts that keeps a perpetual's price aligned with spot |
| **Liquidation** | Forced closing of a position when losses approach the deposited margin |
| **ADL (auto-deleveraging)** | Last-resort, pre-published rule that reduces winning positions if the insurance fund is exhausted; never a capital call |
| **Wrong-way risk** | When the collateral loses value at the same time the position it backs is losing (e.g. LUNC collateral on a LUNC market) |
| **Unbonding** | The 21-day waiting period to withdraw staked LUNC on Terra Classic |
| **Lock-and-mint** | Bridge model where every token issued on another chain has the same amount locked on the origin chain |

## Diagrams

The diagrams above are images hosted in the proposal repository
(https://github.com/igorv43/proposal/tree/main/diagrams). The GitHub README
contains the same diagrams as editable Mermaid source.
