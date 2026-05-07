# Paycheck Restoration Act: Proposal and Public Comment

This repository contains a worked-out proposal for replacing the US federal
income tax, payroll tax, and corporate income tax with a single federal
consumption tax. It is published here for **public comment, criticism, and
collaborative refinement.**

The full proposal is in [`REPORT.md`](./REPORT.md) (rendered inline on
GitHub) or in [`federal_consumption_tax_report.docx`](./federal_consumption_tax_report.docx)
(formatted for printing or sharing as a document).

## What this is

A serious attempt to redesign the federal tax system from first principles,
with internally-consistent revenue accounting, distributional analysis at
each income level, and a 30-year behavioral projection. The headline
findings:

- A federal consumption tax of approximately 25 percent (combined with
  retained tariffs, excise taxes, estate tax, and a new 15 percent tax on
  foreign investment returns) collects the same $5.20 trillion that current
  law collects.
- Every household income level above the bottom decile pays substantially
  less in actual annual federal taxes than under current law. The bottom
  decile remains roughly neutral.
- The math reconciles by capturing approximately $1 trillion in revenue from
  economic activity that currently escapes federal tax: the shadow economy
  ($2.5 trillion in unreported income), foreign investment returns, and
  business transactions on a base far larger than corporate profits.
- Every American worker receives an effective 15.3 percent raise from the
  elimination of payroll tax (combining the visible employee deduction and
  the hidden employer contribution that currently reduces take-home wages).
- The full case is roughly $2.45 trillion in annual purchasing power
  restored to the American economy when tax savings, eliminated compliance
  costs, and eliminated predatory financial products are combined.

## What this is NOT

- It is not a finished bill ready for Congress. It is a structural design
  with realistic numbers and an honest accounting of the trade-offs and
  risks.
- It is not a partisan document. The proposal cuts across the usual
  ideological grouping (it lowers tax burden on most households,
  significantly reduces tax burden on the wealthy in absolute and percentage
  terms, captures previously-untaxed shadow economy activity, and requires
  new statutory protections for workers).
- It is not a guarantee. The 30-year projections depend on behavioral
  responses (investment, labor supply) that have wide empirical bands. The
  proposal works under the pessimistic, moderate, and optimistic scenarios,
  but the magnitude of benefit varies meaningfully.

## How to participate

This proposal is published under [The Unlicense](./LICENSE), which dedicates
it to the public domain. Anyone is welcome to copy, modify, redistribute,
quote, or build on this work without attribution or permission.

If you want to engage with the proposal directly:

- **Open an issue** with specific feedback, criticism, factual corrections,
  or suggested improvements. Use clear issue titles like "Section 5:
  payroll tax incidence claim needs sourcing" or "Appendix B: bracket
  numbers don't reconcile" so others can find related discussions.
- **Submit a pull request** if you have a specific edit to propose. This
  could be wording improvements, additional citations, alternative
  scenario assumptions, or new analyses.
- **Fork the repository** and develop your own variation. Send a link if
  you would like the original author to see your version.
- **Cite specific section numbers** when discussing the proposal so others
  can follow along.
- **Use an AI to analyze the proposal rigorously**, with the analysis
  framework provided in [`LLM_CONTEXT.md`](./LLM_CONTEXT.md). This file
  is designed to be loaded into ChatGPT, Claude, Gemini, or any other
  large language model alongside the proposal. It establishes the
  analytical principles, empirical anchors, and consistency rules that
  rigorous tax analysis requires. The framework anticipates common
  reflexive responses from both ideological directions and explains what
  rigor demands of each. See the LLM analysis section below for details.

## Interactive model

### Why this exists

Tax policy proposals usually arrive as finished arguments. The numbers are
either trusted or distrusted based on who produced them. Readers who want
to know whether the math actually holds up have no good way to find out
short of rebuilding the analysis themselves.

The interactive model in this repository takes the opposite approach. It
exposes every assumption that drives the proposal's numbers and lets you
change those assumptions and see what happens. If you doubt the shadow
economy estimate, dial it down and watch the required rate climb. If you
doubt that workers will get the full 15.3 percent payroll tax raise, drop
the pass-through compliance to 50 percent and see the distributional
impact get worse. If you think the supply-side response will be muted,
switch the scenario to Pessimistic and watch the 30-year projection flatten.

The model is not designed to make the proposal look good. It is designed
to make the proposal testable. Several scenarios produce uncomfortable
results. Several others produce results that look too generous to be real.
Both kinds of finding are valuable. The point is to put the math in your
hands rather than asking you to take it on faith.

### Quick start

The model is at [`models/index.html`](./models/index.html) in this
repository. To use it:

1. Download the file (or clone the whole repository)
2. Open it in any modern browser by double-clicking the file
3. Adjust the controls and watch the outputs update in real time

No server, no installation, no account. Everything runs in your browser
using vanilla JavaScript and one charting library loaded from a CDN. The
file is approximately 33 KB.

If you would rather use it without downloading, the repository owner can
publish it as a website with one click using GitHub Pages (see the
"Hosting it live" section below).

### What the model contains

The model has three connected sections that all recalculate together
whenever you change any input.

**Section 1: Required Consumption Tax Rate.** This is the headline
number. Given the revenue target and base assumptions you choose, what
consumption tax rate is required to collect enough to match the target?
The default is **Balanced Budget at $7.20 trillion**, which is the
design's actual goal (it matches federal spending of $7.00T plus a small
surplus for debt paydown). You can switch to **$5.20 trillion** to match
current-law collections (which leaves the same $1.80T deficit current law
runs), or to **Custom** for any value between $4T and $9T.

This section also lets you adjust:

- **Shadow economy size** (currently estimated $2.5T, with academic ranges
  from $1.5T to $3.5T). Higher shadow economy means more previously-untaxed
  activity captured by consumption tax, which lowers the required rate.
- **Consumption substitution rate** (default 10%, range 0% to 25%). This
  models households shifting spending toward exempt categories over 5
  years as they respond to the new tax. Higher substitution shrinks the
  base and raises the required rate.

**Section 2: Distributional Impact.** This section shows how tax burden
falls across nine income deciles, comparing current law to the new design
at the same revenue target. The chart displays both systems on a
logarithmic scale so the full range from working class to ultra-wealthy
is visible. The accompanying table shows annual savings per household at
each income level.

This section also lets you adjust:

- **EITC and Child Tax Credit budget**. Three options: current law
  ($0.25T), expanded ($0.41T as proposed in this document), or doubled
  ($0.50T for maximum bottom-decile protection).
- **Statutory pass-through enforcement** (default 100%, range 50% to
  100%). This models how much of the eliminated employer payroll tax
  actually flows to workers as wage increases versus being retained as
  employer profit. Lower compliance shifts burden onto workers and away
  from capital owners.

**Section 3: 30-Year Economic Projection.** This section projects real
GDP and federal revenue over three decades under your chosen behavioral
response assumptions. It compares the new design's trajectory against the
current-law baseline.

This section lets you adjust:

- **Behavioral response scenario** (Pessimistic, Moderate, Optimistic).
  These correspond to the three scenarios documented in Section 9 of the
  full report. The Pessimistic scenario reflects Stiglitz-style skepticism
  about supply-side effects. The Optimistic reflects Mankiw-style
  emphasis on capital formation. The Moderate sits at the consensus of
  empirical literature.
- **Real GDP baseline growth rate** (1% to 3%, default 2%). This is the
  current-law trajectory the new design is compared against.

### Scenarios worth trying

These specific configurations illustrate key arguments and counterarguments
in the proposal. Each one is meant to take less than 30 seconds to set up.

**The bull case.** Set Revenue Target to $5.20T (current law collections).
Set the behavioral response scenario to Optimistic. This shows the new
design at its most favorable. Notice the rate falls to roughly 25 percent,
every income decile saves substantial amounts, and 30-year GDP runs about
68 percent above baseline. This is the case advocates would lead with.

**The bear case.** Set Revenue Target to Balanced Budget ($7.20T). Set
shadow economy to $1.5T (low end of estimates). Set substitution to 25
percent (high end). Set pass-through compliance to 50 percent. Set
behavioral scenario to Pessimistic. This is the simultaneous-failure
worst case. The rate climbs to over 40 percent, distributional benefits
shrink dramatically, and the 30-year growth dividend nearly disappears.
The proposal still beats current law in this scenario, but only slightly.

**The honest balanced budget case.** Set Revenue Target to Balanced Budget
($7.20T) and leave everything else at defaults. The rate displays at
approximately 37 percent. This is the actual cost of fully funding
current spending through consumption tax alone. It is uncomfortably high
compared to the $5.20T headline number that gets quoted most often.
Reckoning with this rate, rather than hiding from it, is the productive
discussion.

**The shadow economy stress test.** Hold everything at defaults and slide
the shadow economy size from $1.5T to $3.5T. Watch the required rate
move and consider how confident you are in the estimate. The proposal's
claim of $420B in annual shadow capture depends on this assumption.

**The pass-through enforcement stress test.** Hold everything at defaults
and slide the pass-through compliance from 100% down to 50%. Watch the
bottom-decile burden grow as the worker benefit shrinks. This illustrates
why the statutory enforcement provisions in Section 5 of the report
matter operationally.

**The compounding growth case.** In Section 3, switch between Pessimistic,
Moderate, and Optimistic scenarios and watch the year-30 GDP gain change.
At Moderate the gain is around 38 percent. At Optimistic it is around 68
percent. The difference is roughly $20 trillion in real GDP, which
illustrates why the supply-side response assumptions are the highest-impact
uncertainties in the design.

### What the model can and cannot tell you

The model is honest about its limitations. It cannot tell you:

- Whether the constitutional amendment to repeal the 16th Amendment will
  actually pass
- Whether the Federal Reserve will respond appropriately during transition
- Whether enforcement of statutory pass-through will be effective in
  practice
- Whether real labor supply elasticities and investment elasticities will
  match empirical estimates
- Whether political consensus around the design can be built and maintained

It can tell you:

- What rate is required given any combination of assumptions
- How burden distributes across income levels at that rate
- How sensitive the bottom-line economics are to each assumption
- Where the design is robust (insensitive to assumption changes) and
  where it is fragile (highly sensitive to assumption changes)

If a scenario you set produces results you find implausible, that is
useful information. It tells you something about either the model's
implicit assumptions or about which combinations of inputs are realistic.
Open an issue describing what scenario you tried and what result surprised
you.

### Hosting it live

If you want to make the model accessible without requiring people to
download files, GitHub Pages publishes the entire repository as a static
website with no setup work. To enable:

1. Go to the repository's Settings on GitHub
2. Click "Pages" in the left sidebar
3. Under Source, select "Deploy from a branch"
4. Choose branch `main` and folder `/ (root)`
5. Save

The model becomes available within a minute or two at
`https://mhaines4102.github.io/ConsumptionTax/models/`. You can link
people directly to that URL. The model loads instantly, works on phones
and tablets as well as desktops, and requires no further infrastructure.

## Analyzing the proposal with an LLM

### Why this exists

Large language models like ChatGPT, Claude, and Gemini are powerful tools
for analyzing complex policy proposals. They can read the full proposal
in seconds, surface specific arguments, identify weaknesses, and engage
in substantive back-and-forth discussion in ways that no static document
can match.

There is a problem, though: LLMs are trained on internet text, which
overrepresents popular framings of tax policy from both ideological
directions. When asked about consumption tax, the typical LLM response
recycles standard talking points (regressive, anti-poor, will be passed
through to consumers, FAIR Tax already failed) without engaging the
specific design under review. The asymmetric application of economic
principles is particularly common: an LLM might accept that workers bear
all of payroll tax through reduced wages while simultaneously rejecting
that workers benefit from corporate tax elimination through increased
wages. Same incidence logic, applied inconsistently.

The file [`LLM_CONTEXT.md`](./LLM_CONTEXT.md) is designed to head off this
failure mode. It establishes:

- The analytical principles rigorous tax analysis requires
- The empirical anchors (with citations) that quantitative claims should
  be measured against
- The consistency rules that prevent asymmetric application of incidence
  and behavioral elasticities
- The common reflexive responses from both ideological directions, and
  what rigor demands of each

The goal is not to make the LLM agree with the proposal. The goal is to
make the LLM do real analytical work instead of pattern-matching against
familiar framings. Critiques that survive rigorous analysis are valuable.
Critiques that depend on inconsistent standards are not.

### Quick start

To analyze the proposal with any modern LLM:

1. Open a fresh chat session with your LLM of choice (ChatGPT, Claude,
   Gemini, or others)
2. Paste or attach `LLM_CONTEXT.md` first, with a message like "Please
   read this analysis framework. I will then load the proposal documents
   and ask you to analyze them"
3. Paste or attach `REPORT.md` (the full proposal) and optionally the
   contents of `models/index.html` if you want the LLM to understand
   the calculator
4. Ask whatever you want to know

### Productive question patterns

The LLM gives sharper answers to specific questions than to general ones.
Examples of question patterns that produce useful analysis:

- "Identify the strongest analytical critique of [specific claim in
  Section X]."
- "Where does the proposal's math seem most fragile? What assumptions
  are carrying the most weight?"
- "How would the proposal compare to [alternative]? Use the same revenue
  level for both."
- "Walk me through what would happen if [specific assumption fails]."
- "Explain why [popular critique] does or does not apply to this
  specific design."
- "Compare this proposal to FAIR Tax (HR 25). What are the substantive
  design differences?"
- "If you had to find a flaw in the distributional analysis, what would
  it be? Be specific."

### Less productive question patterns

These produce generic responses that don't engage the proposal:

- "Is this proposal good?" (No verdict to render)
- "Is this conservative or liberal?" (The design cuts across this
  grouping)
- "Will this work?" (Depends on what "work" means and many factors
  outside the design)
- "What do economists think?" (Economists disagree; specific empirical
  claims are testable)

### What you can do with the analysis

Once the LLM has produced analysis, you can:

- Open issues on this repository citing specific points from the analysis
- Submit pull requests with corrections to the proposal based on the
  analysis
- Use the analysis as a starting point for your own deeper investigation
- Test the analysis against other LLMs (different models will sometimes
  produce different critiques, which is itself useful information)

The LLM_CONTEXT.md file is itself open to revision. If you find its
framing biased in either direction, or if you find empirical anchors
that should be added or corrected, that is a valuable pull request.

## Document structure

The full proposal (REPORT.md or the DOCX) is organized into nine sections
plus two appendices:

1. **Across-the-Board Individual Savings** opens with the core distributional
   finding and the chart comparing federal tax burden under current law
   versus the new design at matching $5.20 trillion total revenue.
2. **The Uncaptured Shadow Economy** explains the $2.5 trillion of US
   economic activity currently escaping federal tax and how the new design
   captures it at point of consumption.
3. **High Earner Avoidance of Income Tax** documents the historical pattern
   of compensation shifting in response to high marginal rates (the 91
   percent era and beyond) and why consumption tax breaks the avoidance
   pattern.
4. **Corporate Tax Reform** explains the wheat-and-flour distinction
   between production inputs and capital consumption, and shows how
   current law systematically subsidizes worker replacement with equipment.
5. **Payroll Tax: The Hidden Burden** documents how workers actually bear
   100 percent of payroll tax economic incidence (including the employer
   half) and details the statutory controls required to ensure the full
   15.3 percent benefit reaches workers.
6. **EITC Reform and Consumption Exemptions** outlines the quarterly
   delivery mechanism for working-family credits and the targeted
   exemptions (rent, groceries, healthcare, education, insurance) that
   protect lower-income households.
7. **Investment Capital and Investment Controls** covers elimination of
   long-term capital gains tax, retention of short-term capital gains tax
   (preventing speculation), and the parallel 15 percent tax on foreign
   investment returns (preventing capital flight).
8. **Increased Purchasing Power for Every American** quantifies the
   $2.45 trillion in annual buying power restored through direct tax
   savings, eliminated compliance costs ($718 billion currently), and
   eliminated predatory financial products.
9. **Dynamic Effects and Long-Run Projection** identifies seven channels
   of behavioral response, presents three projection scenarios
   (pessimistic, moderate, optimistic), and lays out the major risks the
   model relies on.

**Appendix A** presents current federal tax collections (FY 2024) for
comparison.

**Appendix B** estimates federal collections by income bracket under the
new design, with reconciliation of household-level burden to total revenue.

## Repository contents

```
ConsumptionTax/
├── README.md                                    This file
├── LICENSE                                      Unlicense (public domain)
├── REPORT.md                                    Full proposal (Markdown)
├── federal_consumption_tax_report.docx          Full proposal (Word format)
├── LLM_CONTEXT.md                               Analysis framework for LLMs
├── models/
│   └── index.html                               Interactive model playground
└── images/
    ├── tax_comparison_chart.png                 Section 1 chart
    └── projection_chart.png                     Section 9 chart
```

## Known limitations and open questions

These deserve honest acknowledgment and are good starting points for
discussion:

- **Constitutional dependence.** The design's long-run viability requires
  a constitutional amendment repealing the 16th Amendment to prevent income
  tax from creeping back. Every European country with VAT has both. The
  political path to amendment is uncertain.
- **Statutory pass-through enforcement.** The 15.3 percent worker benefit
  requires enforceable mandates ensuring employers pass through eliminated
  payroll tax savings to wages rather than retaining them as profit. The
  proposal includes specific enforcement provisions but they require active
  Department of Labor support to be effective.
- **State coordination.** Five states (Alaska, Delaware, Montana, New
  Hampshire, Oregon) have no current sales tax infrastructure. The proposal
  has them either build infrastructure or have federal collection imposed.
  Both are politically difficult.
- **Federal Reserve response.** Implementation creates a one-time price
  level increase of approximately 18 to 20 percent. The Fed must
  accommodate this without treating it as inflation requiring monetary
  tightening. If misread, monetary tightening could deepen the
  post-transition contraction.
- **Behavioral response uncertainty.** The 30-year projections depend on
  investment and labor supply elasticities that have wide empirical bands.
  The pessimistic scenario still beats baseline, but the magnitude of
  benefit varies meaningfully across plausible assumption ranges.
- **The deficit problem is not solved.** Both current law and the new
  design at $5.20 trillion total revenue leave the same approximately
  $1.80 trillion structural deficit. The new design improves the long-run
  fiscal trajectory through higher growth, but the underlying spending
  question is left for separate analysis.

## A note about precision

The numbers in this proposal are best estimates from publicly-available
data (BLS Consumer Expenditure Survey, BEA Personal Consumption
Expenditure, IRS Statistics of Income, CBO distributional analysis,
academic literature on tax incidence and elasticity). They are not
official Treasury estimates. They should be treated as analytical
projections suitable for policy discussion, not as guaranteed outcomes.
Specific numbers will move with better data, more granular modeling, and
real-world implementation experience.

The proposal's defensibility does not rest on any single number being
exactly right. It rests on the structural argument that a consumption tax
captures more economic activity at lower rates than current law, and that
this expansion of base translates into household-level tax relief while
maintaining federal revenue.

## Contributing

Feedback, criticism, and improvements are genuinely welcome. The proposal
is published in this format specifically to invite scrutiny. If you find
factual errors, methodological flaws, or analytical gaps, please open an
issue. If you have improvements to wording, structure, or coverage, please
submit a pull request.

The proposal is unlikely to become law in anything resembling its current
form. That is fine. The point of publishing it is to make a serious
structural argument available for public discussion, refinement, and use
by anyone who wants to engage with the design choices that shape American
fiscal policy.
