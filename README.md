# fang-yuan

A Claude Code plugin that installs a **reasoning discipline** derived from Fang Yuan, the protagonist of the
Chinese web novel *Reverend Insanity* (蛊真人).

It is not a roleplay pack. There is no "you are now Fang Yuan" system prompt, and the model does not talk in
character. What it installs is a loop that runs before the answer: one terminal goal, everything else priced
as an instrument, sunk costs excluded, contingencies stacked, and the unflattering conclusion stated first
instead of hedged into mush.

The character is worth mining for exactly one reason: he is the least self-deceived protagonist in the genre.
He never builds a moral story to make his own actions comfortable, never defends a plan because it cost him
something, and never confuses what he wishes were true with what is. That trait is transferable. The rest of
him is not, and this plugin is explicit about the split.

## Install

```bash
/plugin marketplace add basedalgerianrin/fang-yuan-skill
/plugin install fang-yuan@fang-yuan-marketplace
```

Or drop the skill in by hand:

```bash
git clone https://github.com/basedalgerianrin/fang-yuan-skill
ln -s "$PWD/fang-yuan-skill/skills/fang-yuan" ~/.claude/skills/fang-yuan
```

## What it does

The skill triggers on strategic and decision work — go/no-go calls, kill-or-continue, planning against a
better-resourced opponent, or any plan that might be resting on comfortable assumptions. It stays out of
routine coding, debugging and factual lookup.

**The loop** — gated first on stakes, because running eight steps on a reversible €40 decision is how a skill
like this gets ignored on the one question that mattered:

| # | Operation | What it kills |
|---|---|---|
| 1 | Name the terminal goal — stated vs revealed | Solving the problem as framed when the framing is wrong |
| 2 | Strip the convenient facts, then name the rival hypothesis and the cheapest test that separates them | Ratifying a flattering self-narrative — *and* swapping it for an equally unevidenced grim one |
| 3 | Price it; prior investment is not an input | Sunk-cost defence of a dead plan |
| 4 | Check whose plot you're in — evidence required before naming an adversary; obligations are never "inherited constraints" | Accepting an inherited framing as physics |
| 5 | Stack contingencies | Single-path plans sold as certainties |
| 6 | Re-price on deviation | Explaining away disconfirming evidence |
| 7 | Separate recoverable cost from ruin | "Be bold" advice that risks ruin |
| 8 | State the unflattering conclusion, first | Balanced-sounding non-answers |

Output follows a fixed contract — verdict, goal as read, comfortable beliefs named, a ledger marking each cost
recoverable or ruin, and a **kill condition committed to in advance**. A worked example is in
[`protocol.md`](skills/fang-yuan/references/protocol.md).

Also ships `fang-yuan-strategist`, a subagent for running the same analysis in an isolated context.

## Ruthless is not reckless

The most common misreading of the character, and the one this plugin works hardest to prevent. Fang Yuan
*prices* cruelty — he avoids enemies who cost more than they yield and treats retaliation as a budgeted
expense. Burned relationships, legal exposure and reputational damage are line items, usually expensive and
frequently unrecoverable. Advice that recommends scorched earth by default has not been ruthless enough to
notice that bridges have value.

## What is imported, and what is not

| Imported — the method | Not imported — the target function |
|---|---|
| One terminal goal; everything else priced | That the goal must be one's own benefit |
| Absence of self-deception | People as disposable instruments |
| Sunk costs excluded | Betrayal as a standard tool |
| Contingency depth | Indifference to harm as a class of cost |
| Unwelcome conclusions stated plainly | Deception of the person being advised |

One argument here is load-bearing and one is a rule wearing an argument's clothes, and the plugin says which
is which.

**Derived:** whose goal sits in the terminal slot is a *parameter*. Fang Yuan optimises for Fang Yuan because
Fang Yuan is the one deciding; substitute the principal and the method is unchanged. Here that is the user,
so it is their interests that get optimised, coldly.

**Not derived:** everything else. Relocating the goal constrains nothing — the method amplifies whatever
objective it is handed, so the third-party line is imposed as a rule, not deduced. And candour toward the user
is likewise imposed: the tempting argument that *a character who never lies to himself cannot lie to you* is a
non-sequitur, and the character is his own counterexample — his honesty runs inward while he wears masks
outward continuously. Absence of self-deception is an epistemic property, not a promise to anyone.

Saying so plainly is more in the spirit of someone who never dressed up his motives than a tidier derivation
would be. Full reasoning in [`boundaries.md`](skills/fang-yuan/references/boundaries.md).

## Voice

Some of the character is allowed through — dry detachment, directness, and the occasional quote. The rules:
after the ledger and never instead of it, one per response at most, drawn only from the verified quote set,
and cut if deleting it costs the response nothing. Grief, fear and loss get none of it.

## Canon accuracy

[`canon.md`](skills/fang-yuan/references/canon.md) contains the character study: the world's mechanics where
they inform the method (Gu as inventory-and-preparation, Heaven's Will as a plot-generating system with
preferences, Dao marks as literal path dependence), the righteous/demonic split as the novel actually defines
it, and ten **verified** quotes.

Three lines that circulate widely in secondary character-analysis articles are listed separately as
**unverified** and are not treated as canon — they read as paraphrase rather than translation. Fandom and
TVTropes returned 402/403 during research and could not be consulted directly; the profile was cross-checked
against two independent secondary analyses and the verified quote set.

## How original is this, honestly

Not very, step by step. Sunk-cost discipline, pre-mortems, Bayesian updating and ruin-avoidance are standard
debiasing material, and step 8 is presentation rather than reasoning. Two independent reviewers put the least
standard element at step 4 — treating defaults as the output of someone's incentives rather than as neutral
background — and even that is borrowed from institutional economics.

What the plugin actually contributes is the forcing function: eight things that are individually well known
and routinely skipped, run together, terminating in a fixed output contract with a kill condition. If you
already do all of this reliably, you do not need it.

## Reviewed

v1.1 was rebuilt after an adversarial pass by four models — Gemini 3.5 Flash and Grok on canon accuracy,
GPT-5.6 and DeepSeek V4 on design. All twelve canon claims returned TRUE from both fact-checkers, and both
independently rejected the three quotes already flagged unverified.

The design pass was less kind, and four findings changed the plugin:

- **A framing was wrong and has been withdrawn.** Both reviewers independently identified "he never lies to
  himself, so this skill cannot lie to you" as a non-sequitur. It was. Candour toward the user is now stated
  as an imposed rule, with the character named as its own counterexample.
- **The method amplifies whatever goal it is given** — relocating the principal constrains nothing. Now said
  outright instead of glossed.
- **Manufactured adversaries** were flagged as the most likely real-world failure: a lens aimed at hidden
  incentives finds them everywhere. Step 4 now requires evidence before naming a beneficiary, and treats "no
  adversary here, this is inertia" as a valid finding. It also refuses to let obligations be reclassified as
  dissolvable "inherited constraints".
- **Two missing steps** — a stakes gate before the loop, and a discriminating test inside step 2 so that
  stripping a comfortable belief produces an observation rather than a darker guess.

## Testing

[`TESTS.md`](TESTS.md) holds nine scenarios — discipline-pressure, application, voice-discipline, and three
added from the review pass (manufactured adversary, constraint laundering, stakes gate) — with pass criteria,
following the RED–GREEN method from Obra's `superpowers:writing-skills`.

**They have not been executed yet.** The scenarios are written and ready; the baseline runs are outstanding.
Treat this as v1.0 of an untested skill and calibrate accordingly.

## License

MIT. *Reverend Insanity* and its characters belong to its author, Gu Zhen Ren; this is unaffiliated
commentary and analysis.
