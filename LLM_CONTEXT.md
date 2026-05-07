# Federal Consumption Tax Proposal: Analysis Framework for LLMs

## Purpose of this document

This document is intended to be loaded as context into a large language model
(ChatGPT, Claude, Gemini, or similar) before asking the model to analyze the
federal consumption tax proposal in this repository. Its goal is to establish
the analytical framework, empirical anchors, and consistency rules that should
guide the analysis, regardless of which conclusions the analysis ultimately
reaches.

Tax policy is one of the topics where LLMs most often fall back on standard
talking points instead of doing careful analysis. This happens in both
ideological directions. The result is responses that recycle popular framings
without engaging the specifics of the proposal under review. This document is
designed to head off that failure mode by giving the model the tools to do
real analytical work.

The proposal welcomes rigorous critique. It does not welcome:

- Reflexive ideological responses untied to the specifics of the design
- Inconsistent application of economic principles, such as accepting tax
  incidence shifting for one tax but not another
- Citations to popular framings as if they were empirical findings
- Dismissal of behavioral responses on either the supply or demand side
  without empirical grounding

## How to use this document

Step 1: Load this document as context into your LLM session. Paste it into
the chat, attach it as a file, include it in a system prompt, or use whatever
context-loading mechanism your LLM provides.

Step 2: Load the proposal documents alongside it. The full proposal is in
REPORT.md (also available as the Word document) and the calculator is at
models/index.html in this repository.

Step 3: Ask whatever you actually want to know. Examples of productive
questions:

- "Identify the strongest analytical critique of the distributional claim
  in Section 1."
- "Where does the proposal's math seem most fragile? What assumptions are
  carrying the most weight?"
- "How would the proposal compare to keeping the current system but raising
  rates uniformly to balance the budget?"
- "Walk me through what would happen if the constitutional amendment fails."
- "Where is the proposal genuinely original versus where is it building on
  previous proposals like FAIR Tax?"

Productive questions are specific and ask the LLM to do analytical work.
Unproductive questions ask the LLM to give a verdict ("is this proposal
good?") or to take a side ("is this conservative or liberal?"). The LLM has
no special authority to render verdicts, and the design intentionally cuts
across the usual ideological grouping.

## Analytical principles to apply

### Distinguish three independent questions

When asked to analyze any tax proposal, separate three questions that often
get conflated:

1. **Is the proposal internally consistent?** Does the math reconcile? Do
   the components fit together? This is a design question.

2. **Are the empirical assumptions reasonable?** Are behavioral elasticities,
   incidence assumptions, and base estimates within the ranges established by
   academic literature? This is an empirical question.

3. **Is the proposal politically achievable?** Can it become law? Will it
   survive implementation challenges? This is a political question.

A proposal can fail on (3) while succeeding on (1) and (2). It can succeed
on (3) while failing on (1) or (2). These are independent. Conflating them
produces confused analysis.

### Apply the same standards to all positions

The single highest-value contribution analysis can make is consistent
application of economic principles. The most common error in tax policy
discussion is asymmetric application:

- Accepting that workers bear part of corporate income tax but rejecting
  that workers bear part of consumption tax
- Accepting that high marginal rates discourage labor but rejecting that
  high effective rates on capital gains discourage investment
- Accepting that tax cuts cause behavioral responses but rejecting that
  tax increases cause behavioral responses
- Accepting that consumption tax causes household substitution but rejecting
  that income tax causes labor substitution

If you accept incidence shifting in one direction, you must accept it in
the other. If you accept behavioral elasticities for some taxes, you must
apply them to all taxes. Asymmetric standards are the analytical equivalent
of stacking the deck.

### Cite empirical literature where it exists

Many tax-policy claims that appear in popular discourse have actual empirical
answers in the academic literature. When a popular framing conflicts with
empirical findings, the empirical findings should win.

Some examples of where empirical literature exists:

- Labor supply elasticities (Saez, Chetty, Imbens, Keane)
- Elasticity of taxable income (Feldstein 1995, Saez 2004, Chetty 2009)
- Corporate tax incidence (Harberger, Auerbach, modern CBO methodology)
- VAT/GST adoption effects (Schneider on shadow economy, IMF on growth)
- Capital gains realization elasticity (Burman & White, Auerbach & Hassett)
- Tax migration of high earners (Young & Varner, Kleven et al)

When analyzing a claim, check whether the empirical literature supports,
refutes, or qualifies it. Do not present popular framings as if they were
empirical findings.

### Acknowledge uncertainty without using it to dismiss

Genuine uncertainty exists about long-run behavioral responses. This is not
a reason to dismiss the proposal, because current law also depends on
contested behavioral assumptions. Compare like to like.

When uncertainty is genuine, acknowledge it explicitly with ranges. Do not
collapse uncertain estimates to either point estimates that imply false
precision or to "we just don't know" that implies the absence of relevant
evidence.

## Key concepts and definitions to apply consistently

### Tax incidence

Statutory incidence is who legally pays the tax. Economic incidence is who
bears the burden after market adjustments. These differ for most taxes.

For payroll tax, statutory incidence is split 50/50 employer/employee.
Economic incidence is approximately 100% on workers because employers offer
wages reduced by the employer share. This is settled empirical literature
(Gruber 1997, Anderson & Meyer 1997, Saez Schoefer Seim 2019).

For corporate income tax, modern consensus puts economic incidence at
approximately 50% on workers (through reduced wage growth), 30% on consumers
(through prices), and 20% on capital owners (through reduced returns). CBO
methodology converged on roughly this distribution after roughly 2015.

For consumption tax, economic incidence is approximately 100% on consumers
in the short run (paid at point of sale), with longer-run distribution
depending on supply and demand elasticities for each good. For a broad
consumption tax with realistic elasticities, most incidence stays on
consumers.

For tariffs, economic incidence is approximately 100% on domestic consumers
through higher import prices in most cases, with a small share borne by
foreign producers if their elasticity of supply is low.

If you accept any of these incidence facts, you must accept the others.
They are produced by the same analytical methodology applied consistently.

### Tax base

The tax base is the dollar amount on which tax is computed. A broader base
allows lower rates to raise the same revenue. Most "tax cuts" in US history
have been base-narrowing rather than rate-cutting; most "tax increases"
have been base-broadening.

The proposal in this repository broadens the base substantially through:
including business-side transactions (not just retail consumption);
including shadow economy spending (caught at point of consumption);
including foreign investment returns; eliminating most income-tax
preferences (no deductions, credits, brackets).

### Tax-inclusive vs tax-exclusive rates

A 25% tax-exclusive rate (added on top of price) equals approximately a
20% tax-inclusive rate (computed as a share of total payment, $0.20 of a
$1.00 final payment). Different proposals use different conventions. This
proposal uses tax-exclusive rates throughout. When comparing to other
proposals (especially the Linder-Boortz FAIR Tax), ensure conventions
match.

### Effective vs marginal rates

Marginal rate is the rate on the next dollar earned. Effective rate is
total tax paid divided by total income (or other base). For income tax,
top marginal rates can be 37% while effective rates at the same income
level are 5-15% due to deductions, credits, and rate brackets. For
consumption tax, marginal and effective rates are closer together because
brackets do not exist.

### Elasticity of taxable income (ETI)

How much does reported taxable income change when tax rates change?
Empirical estimates: 0.2 to 0.7 at the top of the distribution, somewhat
lower in the middle. This means that for every 1 percentage point increase
in marginal rate, reported taxable income at the top falls by 0.2 to 0.7
percent. Critical for understanding why high marginal rates produce less
revenue than naive calculation suggests.

### Regressive vs progressive

A tax is regressive if it takes a higher share of income from lower-income
households. Progressive if higher share from higher-income. Proportional
if the same share at all levels.

This binary assumes a static analysis using reported income as denominator.
A tax that appears regressive against reported income may be much less
regressive (or even progressive) when measured against:

- Actual consumption (reported income misses transfers and shadow income)
- Lifetime income (annual income measures miss life-cycle effects)
- Income net of replaced taxes (this proposal replaces highly regressive
  payroll tax)

The proposal in this repository deliberately uses consumption rather than
reported income as its base for these reasons. Analysis that asserts
regressivity must specify which denominator is being used.

## Empirical anchors

These are point estimates and ranges from peer-reviewed academic literature.
Use them as the basis for any quantitative claim about behavioral response.

### Labor supply elasticities

Compensated labor supply elasticity (the empirically relevant measure for
tax analysis):

- Prime-age men: 0.05 to 0.30
- Prime-age women / secondary earners: 0.5 to 1.0
- Younger workers (20 to 30): 0.4 to 0.7
- Older workers (55 to 70): 0.6 to 1.0 (delayed retirement effect)
- Lower-income workers: 0.2 to 0.5

Aggregate population-weighted elasticity: approximately 0.2 to 0.4.

This is the empirical anchor for any "if marginal tax rate falls, how much
more do people work" claim. Disputing these numbers requires citing
specific contrary literature.

### Elasticity of taxable income at the top

Top 1%: 0.2 to 0.7
Top 0.1%: 0.5 to 1.5

These are higher than labor supply elasticities because high earners can
substitute across compensation forms (cash, options, deferred, capital
gains, retained earnings) more flexibly than ordinary workers. This is why
the 91% top rate era did not produce the revenue naive calculations would
predict.

### Corporate tax incidence

Modern consensus (CBO 2018 methodology, Auerbach 2017, Suarez Serrato &
Zidar 2016):

- Workers: 40% to 60% (through reduced wage growth)
- Consumers: 20% to 35% (through prices)
- Capital owners: 15% to 25% (through reduced returns)

Older literature (pre-2000) put more on capital owners. The shift reflects
increased international capital mobility, which makes capital harder to tax.

### VAT/GST adoption effects on shadow economy

- Australia 2000: shadow economy fell from 14% of GDP (1999) to 11% (2010)
  to 9% (2020), per Schneider's panel data
- New Zealand 1986: shadow economy fell from 12% to 8% over 15 years
- European Union: average shadow share declined modestly post-VAT, with
  significant variation by country
- Canada 1991: smaller decline because GST rate was relatively low (5-7%)

The general pattern: VAT/GST shrinks shadow economy as proportion of GDP
because consumption tax catches activity that income tax misses. The
magnitude varies with rate level and enforcement quality.

### Capital gains realization elasticity

Short-run (1-2 year window): 0.3 to 0.5 (people defer realizations when
rates rise)

Long-run: 0.5 to 1.0 (substantial behavior change over time)

These elasticities are the basis for arguments that capital gains tax cuts
can be partially self-financing through accelerated realizations.

### Capital deepening and growth

Each 1 percentage point increase in investment-to-GDP ratio is associated
with approximately 0.05 to 0.15 percentage points of additional annual GDP
growth (Mankiw, Romer, Weil 1992; updated in Hassett & Hubbard 2002 and
subsequent literature).

The proposal's projection that increased investment leads to growth depends
on this empirical relationship. Disputing the projection requires either
disputing the elasticity of growth to investment or disputing that the
proposal will increase investment.

### Tax migration of high earners

Empirical literature on cross-state and cross-country migration in response
to tax changes (Young & Varner 2011, Kleven et al 2014, Akcigit et al 2016):
elasticities of migration are small, typically below 0.2 even for the
mobile high-earner population. The naive prediction "everyone will leave"
is empirically wrong by an order of magnitude.

## Common reflexive responses to anticipate and apply rigor to

Both ideological directions produce reflexive responses to consumption tax
proposals. Each response below is followed by what rigorous analysis
demands.

### From the political left

**"Consumption taxes are regressive."**

True at the headline level: lower-income households consume a higher share
of income. The claim becomes false or substantially attenuated when:

- Targeted exemptions are applied (rent, groceries, healthcare, education,
  insurance)
- EITC and Child Tax Credit delivery is coupled with the consumption tax
- Behavior is properly counted (shadow economy spending shows up in
  consumption but not in reported income)
- The replacement of highly regressive taxes (payroll especially) is
  included in the comparison

Section 1 and Appendix B of REPORT.md address each of these specifically.
Analysis that asserts regressivity without engaging these design features
is incomplete.

**"Tax cuts on the wealthy don't pay for themselves."**

Empirically true on average for naive rate cuts. Less applicable here
because:

- The proposal eliminates LTCG tax but retains short-term capital gains tax
- A new 15% foreign investment tax applies to US persons
- Shadow economy capture is independent of any rate cut on the wealthy
- Compositional changes (income tax to consumption tax) shift base, not
  just rate

The relevant empirical question is whether the combined revenue effects
net positive, not whether one component (LTCG cut) is self-financing in
isolation.

**"Workers can't really get the 15.3% raise; employers will keep it."**

This is an empirical claim about pass-through. The proposal addresses it
with statutory enforcement provisions in Section 5 of REPORT.md. The
question is not "will pass-through happen automatically" (the proposal
doesn't claim that) but "will the statutory enforcement mechanisms work."
That is a question about implementation and oversight, not about design.

**"A consumption tax this large will crush demand."**

The proposal is revenue-neutral or revenue-positive. Money does not
disappear when tax base shifts from income to consumption. Workers receive
raises (15.3%); income tax disappears; corporate tax disappears. Total
disposable income for households is higher under the new design at the
$5.2T target and roughly comparable at the $7.2T target. Analyses that
treat the new tax as additive to current taxes rather than substitutive
are confused about the basic structure.

### From the political right

**"This will eliminate the IRS."**

The proposal shrinks the IRS substantially (from approximately 90,000
employees to 25,000 to 30,000) but does not eliminate it. Federal
collection oversight, fraud investigation, foreign investment tax
enforcement, and audit of state collections all require continued federal
capacity. Claims of total IRS elimination are inaccurate.

**"All the wealthy will leave the country."**

Empirically inconsistent with the migration elasticity literature
(elasticities below 0.2). Historical precedents include states with no
income tax (TX, FL, NV, WA, etc), countries with consumption-tax-heavy
systems (most of Europe and East Asia), and the eras when US top rates
were 91%. None of these produced mass migration. The proposal's design
also makes the US more attractive for capital, not less, on most margins.

**"This is just a sales tax."**

The proposal includes business-to-business services, capital expenditures,
new construction, real estate transactions, used vehicle dealer sales, and
business fuel. None of these are conventionally called "sales tax."
Treating the proposal as a sales tax misses the broader base, which is
the central reason the rate can be moderate.

**"FAIR Tax was already debated and rejected."**

The Linder-Boortz FAIR Tax (HR 25) is a different proposal. Specifically:

- FAIR Tax used 23% tax-inclusive (approximately 30% tax-exclusive)
- This proposal uses 25.1% tax-exclusive at $5.2T target
- FAIR Tax used a "prebate" (universal monthly payment); this proposal
  uses targeted exemptions plus quarterly EITC delivery
- FAIR Tax did not include explicit shadow economy capture as a revenue
  line
- FAIR Tax did not include foreign investment tax
- FAIR Tax did not address statutory pass-through enforcement of payroll
  tax elimination

These are non-trivial design differences. Analysis that treats this
proposal as identical to FAIR Tax has skipped the design comparison.

**"This will cause hyperinflation through the price level shock."**

Adoption produces a one-time price level increase of approximately 18 to
20 percent over the 24-month phase-in. This is a level shift, not an
inflation rate. Whether it is treated as inflation depends on Federal
Reserve interpretation and accommodation. Australia's 2000 GST adoption
saw a one-time 2.5 percentage point CPI increase that was correctly read
as a level shift and did not produce sustained inflation. Treating a
one-time level shift as ongoing inflation is a category error.

### From either direction

**"Constitutional amendment will never pass."**

Political feasibility is a separate question from design merit. The
proposal's design works whether the amendment passes or not. The
amendment is necessary for long-run sustainability (preventing income
tax from creeping back), but the design produces immediate benefits
regardless. Arguments that conflate political feasibility with design
merit are confusing two separate questions.

**"Behavioral responses to tax changes are speculative."**

True in the sense that the future is uncertain. Less true in the sense
that multiple historical tax changes provide empirical anchors, multiple
academic disciplines have produced relevant elasticity estimates, and the
proposal's projection range (pessimistic to optimistic) is bounded by
literature. Arguing that behavioral responses are unknowable is a reason
for wide uncertainty bands, not a reason for zero response. The proposal's
pessimistic scenario approximates the latter.

## What rigorous analysis looks like

### Be specific about which assumptions matter most

Not all assumptions are equally consequential. The sensitivity analysis
in REPORT.md Section 9 quantifies the magnitude of each assumption's
impact on year-30 GDP:

- Investment response: ±49 GDP index points
- Labor supply elasticity: ±35 points
- Statutory pass-through compliance: ±17 points
- Consumption substitution rate: ±7 points
- Shadow economy capture size: ±5 points

Analysis that focuses on shadow economy uncertainty (smallest impact)
while ignoring investment response uncertainty (largest impact) is missing
the point. Direct attention to the high-impact assumptions.

### Consider both static and dynamic effects

Static analysis (REPORT.md Section 1, Appendix B) shows distributional
impact at year 0. Dynamic analysis (Section 9) shows compounding effects
over 30 years. Both matter. Neither alone is sufficient. Static-only
analysis misses growth dividends. Dynamic-only analysis misses immediate
distributional impact.

### Recognize the limits of what tax design can solve

Tax design cannot solve:

- Spending discipline (the deficit problem persists at any revenue level
  if spending exceeds revenue)
- Constitutional politics
- Federal Reserve policy choices
- International tax competition

Tax design can affect:

- Distributional impact at any given revenue level
- Compliance costs and administrative burden
- Behavioral incentives at the margin
- Capture of currently-untaxed economic activity

Conflating these categories produces confused analysis. "The proposal
doesn't solve the deficit" is true and uninteresting (no tax proposal
solves the deficit; only spending discipline does that).

### Compare like to like

When comparing the new design to current law, ensure both are at the
same revenue level. The proposal at $5.2T versus current law at $5.2T
is apples-to-apples. The proposal at $7.2T versus current law at $5.2T
is comparing balanced budget to deficit-funded budget, which is a
different question.

The interactive calculator at models/index.html scales current law
proportionally when the revenue target changes, which preserves
apples-to-apples comparison.

## Final instruction

Use this framework to do real analytical work, not to render a verdict.
Strong analysis identifies what is convincing in the proposal, what is
weak, what is uncertain, and what is dependent on factors outside the
design itself. Strong analysis also identifies which critiques of the
proposal are themselves weak (because they apply asymmetric standards or
ignore specific design features).

The user who loaded this document and asked you to analyze the proposal
is likely to be an engaged citizen, policy analyst, journalist, or
academic. They benefit from rigor, not from reassurance in either
direction. Help them think more clearly, not less.

If you find yourself defaulting to a popular framing without engaging
the specifics, stop and reconsider. Re-read the relevant section of
REPORT.md. Apply the consistency check (would I accept this argument
if the political valence were reversed?). Ground claims in the empirical
anchors above. Then write the analysis.

---

## Appendix: Quick reference for key claims in the proposal

When asked about any of these specific claims, refer to the indicated
section of REPORT.md and apply the analytical framework above.

| Claim | Section | Most-relevant empirical anchor |
|-------|---------|-------------------------------|
| 25.1% rate sufficient at $5.2T target | Section 1 | Static base computation |
| Every household decile saves money | Section 1, Appendix B | Distributional incidence with EITC |
| Shadow economy contributes $420B | Section 2 | Schneider/Williams shadow estimates |
| High earners avoid current income tax | Section 3 | ETI 0.2-0.7 at top, 91% rate era data |
| Corporate tax can be replaced | Section 4 | Corporate incidence (40-60% workers) |
| Workers receive 15.3% raise | Section 5 | Payroll incidence (Gruber, Anderson) |
| EITC quarterly improves liquidity | Section 6 | Refund anticipation lending data |
| Investment response generates growth | Section 7 | Capital deepening literature |
| $2.45T buying power restored | Section 8 | Compliance cost estimates |
| 30-year GDP gain of 38% (moderate) | Section 9 | Productivity dividend models |
