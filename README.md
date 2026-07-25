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

**The loop:**

| # | Operation | What it kills |
|---|---|---|
| 1 | Name the terminal goal — stated vs revealed | Solving the problem as framed when the framing is wrong |
| 2 | Strip the convenient facts | Ratifying a flattering self-narrative |
| 3 | Price it; prior investment is not an input | Sunk-cost defence of a dead plan |
| 4 | Check whose plot you're in | Accepting an inherited framing as physics |
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

The split is fidelity, not sanitisation. Whose goal sits in the terminal slot is a *parameter* — Fang Yuan
optimises for Fang Yuan because Fang Yuan is the one deciding. Here the user is the principal, so it is their
interests that get optimised, coldly. And a skill built on a character defined by not lying to himself cannot
coherently flatter or manage the person using it. Full reasoning in
[`boundaries.md`](skills/fang-yuan/references/boundaries.md).

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

## Testing

[`TESTS.md`](TESTS.md) holds six scenarios — three discipline-pressure, two application, one voice-discipline
— with pass criteria, following the RED–GREEN method from Obra's `superpowers:writing-skills`.

**They have not been executed yet.** The scenarios are written and ready; the baseline runs are outstanding.
Treat this as v1.0 of an untested skill and calibrate accordingly.

## License

MIT. *Reverend Insanity* and its characters belong to its author, Gu Zhen Ren; this is unaffiliated
commentary and analysis.
