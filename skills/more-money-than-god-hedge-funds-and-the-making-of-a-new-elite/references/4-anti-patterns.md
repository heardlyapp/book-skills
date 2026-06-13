# Anti-Patterns: The Three Horsemen of Hedge Fund Destruction

> Source: More Money Than God, Chapters 10–11, 14–16

## Horseman 1: Model Hubris (LTCM)

Long-Term Capital Management was assembled in 1994 by John Meriwether, the former head of Salomon Brothers' legendary arbitrage desk. He recruited Myron Scholes and Robert Merton, Nobel laureates in economics for their options-pricing formula. The fund was staffed by PhDs who believed risk could be calculated, measured, and contained.

**Case: The "ten-sigma" myth.** LTCM's value-at-risk models calculated that the most they could lose in a single day was $116 million (99 out of 100 days). For a 21-day period, the maximum loss was $532 million. The odds of losing everything were, according to their models, 1 in 10^24 — an event that should occur once in the lifetime of the universe.

**What actually happened:** In August 1998, Russia defaulted on its debt. This triggered a chain reaction. LTCM lost $550 million in a single day (August 21), and by Labor Day they had lost $1.9 billion — 44% of their capital. This loss should have been impossible by their models. But the models had fundamental flaws:

1. **Normal distribution assumption.** The models assumed price changes followed a bell curve. But markets have "fat tails" — extreme events happen far more often than a normal distribution predicts. The 1987 crash had already demonstrated this, but LTCM's models ignored the lesson.
2. **Correlation blindness.** LTCM believed its portfolio was diversified because its various strategies (bond arbitrage, equity volatility, swap spreads) appeared uncorrelated in normal conditions. But when panic struck, every position moved in the same direction. As Eric Rosenfeld (LTCM partner) later admitted, the failure to anticipate "trader-driven correlation" was the fund's central error.
3. **History is not a guide.** The models were based on historical price data. But the conditions that produced that history were about to change. When all the arbitrageurs simultaneously needed to unwind positions, the market dynamics inverted — the Slinky effect was suspended.

**Case: The crowded trade.** LTCM's strategy was so successful that imitators copied it. By 1998, every bank's proprietary trading desk and every hedge fund that could buy LTCM-style positions already had. When the reversal came, there was nobody left to sell to — the one-way market was down only. Worse, predators realized LTCM would be forced to liquidate, so they shorted LTCM's known positions with impunity. Goldman Sachs's trading desk in London was quoted: "If you think a gorilla has to sell, then you sure want to sell first."

## Horseman 2: Leverage Traps

Leverage is the amplifier: it magnifies both profits and losses. The question is not whether you're right, but whether you can survive being wrong temporarily.

**Case: The 1994 bond market.** When the Fed raised rates by 0.25%, leveraged hedge funds that had been betting on falling rates were immediately underwater. Margin calls forced them to dump positions. The selling drove prices further against them, triggering more margin calls. This cascade spread from the US to Japan to Europe. Several funds were wiped out in what should have been a minor rate move.

**The asymmetry:** The average hedge fund borrows only 1–2 times capital. Highly leveraged funds borrow up to 10 times. But investment banks like Goldman Sachs and Lehman Brothers were leveraged 30-to-1 before the 2008 crisis. Mallaby's key argument: banks, not hedge funds, were the real source of systemic risk.

## Horseman 3: The Illusion of Diversification

Diversification works in normal markets. In crises, correlations converge to 1. When panic drives every market in the same direction, positions that appeared uncorrelated suddenly move in lockstep.

**Case: LTCM's September 1998 death spiral.** The Royal Dutch/Shell premium leaped from 8% to 17% with no fundamental reason. Hurricane bonds (insurance-linked securities with zero connection to interest rates) plummeted 20% on the day Meriwether's letter leaked, despite hurricanes being utterly unaffected. In Europe, British and German government bond spreads moved in opposite directions for no reason other than that LTCM was betting on the convergence. As LTCM's counsel Jim Rickards told Meriwether: "If you're long, they're short. If you're short, they're long."

**Case: The 2008 quantitative crisis.** In August 2007, a dozen or so quantitative hedge funds tried to cut their positions simultaneously, triggering wild swings in equity markets and billions in losses. The same statistical arbitrage strategies that were profitable in calm conditions became deadly when everyone tried to exit at once. This pattern repeated in 2008 after Lehman's collapse, when hedge funds suffered losses not because their strategies were wrong but because the liquidity that made those strategies possible evaporated.

## The Bank vs. Hedge Fund Double Standard

Mallaby argues that the 2007–2009 crisis was primarily a banking crisis, not a hedge fund crisis. Wall Street behemoths loaded up on risk because they expected taxpayer bailouts. By contrast, hedge funds:

- Received **zero** direct taxpayer assistance during the crisis
- Have **high-water marks** — lost fees must be earned back before performance fees resume
- Mostly have **managers' own capital** at risk in the fund
- Face **no government safety net**, so they are more paranoid about leverage

**The irony:** The banks that politicians wanted to protect from hedge funds were the ones that caused the crisis. The hedge funds that politicians wanted to regulate out of existence sailed through with their own survival instincts intact.
