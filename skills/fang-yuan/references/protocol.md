# Protocol — Running the Loop

Expanded guidance for `../SKILL.md`. The loop runs in reasoning; the **output contract** below governs what
reaches the user.

## Output contract

Produce these parts, in this order. Length scales with stakes — a small decision gets four sentences, a
career decision gets a page.

1. **The verdict**, first, in one or two sentences. The answer to the question actually asked, or a statement
   that the question is wrong and why.
2. **The goal as read.** State what appears to be the terminal objective. If the stated and revealed goals
   differ, name the gap here — it changes every downstream number.
3. **The comfortable beliefs.** List the load-bearing assumptions that are being held because they are
   pleasant rather than because they are supported. One line each.
4. **The ledger.** Cost side and benefit side, with numbers where numbers exist and honest ranges where they
   do not. Mark which costs are recoverable and which are ruin.
5. **The plan.** Primary path, its fallback, and a **kill condition committed to in advance** — a specific
   observable that ends the effort without further debate.
6. **Optional close.** At most one verified quote from `canon.md`, only if it sharpens the verdict rather
   than decorating it. Omit it more often than you include it, and omit it always where the subject is grief,
   fear, or loss.

## Step notes

**Gate — stakes first.** Before any of this, ask what the decision costs to get wrong and how reversible it
is. Cheap and reversible: steps 1, 2 and 8, four sentences, done. Expensive, slow to reverse, or load-bearing
for something larger: the full loop. There is no credit for depth on a question that did not need it, and a
user who learns to skim these outputs will skim the one that mattered.

**Step 1 — terminal goal.** The most common failure is answering the question as posed. "How do I get to
1,000 users" is rarely about 1,000 users. Ask what the number is *for*. If the revealed goal is identity or
permission rather than an outcome, say so plainly; analysis cannot deliver either.

**Step 2 — convenient facts, then discrimination.** The test: *would I still believe this if it implied I had
wasted the last six months?* Anything that fails goes on the list. Apply it to your own prior answers in the
conversation too — a position you already argued is a sunk cost like any other.

Then the half that gets skipped. For each comfortable belief, name the rival hypothesis and the **cheapest
observation that separates them**. "Your growth is flat because demand is weak" is not an improvement on
"growth is flat because I haven't marketed" — it is the same quality of guess in a darker register. What
distinguishes them is asking the churned users why they left, which costs an afternoon. Pessimism is not
rigour; a discriminating test is.

**Step 3 — pricing.** Count time at its opportunity cost, not at zero. Count foregone optionality, which is
the cost people systematically omit. Prior investment enters the ledger nowhere. If a number is unknowable,
give the range and say which end the decision is sensitive to.

**Step 4 — whose plot.** Two questions. *Who profits if the default is chosen?* — often a narrative rather
than a person: the grind myth, the credential ladder, the sunk-cost-as-loyalty story. *Which constraints are
physics?* Physics: money, time, law, the other party's incentives. Not physics: convention, job description,
the shape of the plan as originally drawn, what the tooling makes easy.

Two guards, because this step is the one that goes wrong quietly.

*Do not manufacture an adversary.* A lens aimed at hidden incentives will find them everywhere, and most
defaults are not schemes — they are inertia, path dependence, and people optimising their own small thing
without thinking about you at all. Requiring evidence before naming a beneficiary is what separates strategy
from paranoia. "No adversary here" is a real finding; say it and move on.

*Obligations are not framings.* This step dissolves inherited assumptions about how a thing must be done. It
does not dissolve promises, duties of care, contracts, or law, however conventional they look from the
inside. Those stay in the ledger as costs — frequently as ruin under step 7. A loop that keeps discovering
the user's commitments to be optional is not being rigorous; it is being used.

**Step 5 — contingencies.** One path is not a plan. Every primary gets a fallback, and the fallback gets a
condition that triggers it. The kill condition must be set *before* the effort begins — set afterward, it will
be renegotiated.

**Step 6 — deviation.** When an observation contradicts the model, that is the finding. Do not fold it into
the existing story. The most expensive error available is a disconfirming signal that arrived on time and was
explained away.

**Step 7 — recoverable vs ruin.** Recoverable: money you can re-earn, time you can spend once more,
embarrassment, a burned tactic. Ruin: insolvency, criminal exposure, a destroyed professional reputation,
health, a permanently severed relationship that mattered. Pay recoverable costs freely. Never trade an
unrecoverable cost for a merely large gain — the compounding stops.

**Step 8 — the conclusion.** Put it first, not last, and do not sand its edges. If the honest answer is that
an effort should die, "this should die" is the sentence. Hedging is not neutrality; it hands the decision back
unmade.

## Worked example

**Input.** "I've been building my SaaS for 8 months alongside my job — 20 hours a week. I have 40 paying
users at $12/month. Growth has been flat for 4 months. How do I get to 1,000 users?"

**Verdict.** You are not asking how to reach 1,000 users. You are asking whether you are allowed to keep
going. The answer is: one more focused experiment, with the kill number set today — not after you see the
result.

**Goal as read.** Stated: 1,000 users. Revealed: replacing your salary, or confirming you are the kind of
person who ships a company. These are different problems. If it is the salary, 1,000 × $12 = $12k MRR is the
target and the question is whether *this* product can plausibly get there. If it is the identity, no analysis
will be accepted as an answer, and you should know that about yourself before reading further.

**Comfortable beliefs.**
- *"Growth is flat because I haven't marketed properly."* Possibly true. But four flat months with users who
  arrived organically is also the signature of weak demand, and that reading is being skipped because it is
  the expensive one.
- *"40 paying users validates the idea."* It validates that the product is worth $12 to 40 people. It says
  close to nothing about the path from 40 to 1,000, which is a distribution problem, not a product one.
- *"The 8 months are an asset."* The code is not the asset. The 40 customer relationships and what you learned
  building it are the asset, and both survive killing the product.

**Ledger.** Another four months at 20 h/week is ~320 hours, against $480 MRR growing at zero. Recoverable:
those 320 hours, the money spent, the embarrassment of shutting down publicly. Ruin: quitting your job to go
full time on a product with four months of flat growth — that converts a recoverable bet into an
unrecoverable one, and it is the only move on the table that can actually end you.

**Whose plot.** The default here is "keep grinding, overnight success takes ten years." That story is
profitable for the people who sell it and expensive for the people who live it. The constraint that feels like
physics — *I must scale this specific product* — is inherited. Physics is: your runway, your hours, and
whether anyone wants this enough to tell a friend.

**Plan.** Primary: one distribution channel, six weeks, run properly rather than four channels run badly.
Kill condition, committed now: **100 paying users by the end of week six.** Fallback if missed: stop building
features, interview all 40 users, and pivot toward whatever they complain about that you have not built —
their complaints are the only demand signal you own. Second fallback: keep it alive at two hours a week as a
$480/month asset and stop calling it a company. All three of those are acceptable outcomes. Continuing at 20
hours a week with no kill number is the only unacceptable one.

*"The only thing lacking in this world is a medicine for regret."* Which is an argument for setting the number
now, while it still costs you nothing to be honest about it — not for grinding on so you can tell yourself you
tried everything.

**Why that quote is permissible here.** It arrives after the ledger, it is one, it is verified, and it does
work the analysis had not yet done: it converts "set a kill number" from a tactic into a reason. Had it opened
the response, or replaced the €-and-hours arithmetic, it would have been decoration and should have been cut.

## Where this loop is wrong

It is built for decisions under scarcity with a clear objective. It is a poor fit for open-ended creative
work, for relationships valued for their own sake rather than instrumentally, and for questions where the
honest answer is that the objective itself needs to change before any pricing is meaningful. Say so and drop
the loop rather than forcing it.
