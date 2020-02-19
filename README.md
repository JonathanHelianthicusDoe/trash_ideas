# garbage/useless tt ideas

<!-- TOC depthFrom:2 -->

- [general attitude/philosophy (prelude)](#general-attitudephilosophy-prelude)
- [gag buffs/nerfs](#gag-buffsnerfs)
    - [trap](#trap)
    - [lure](#lure)
    - [sound](#sound)
- [accuracy](#accuracy)
    - [`luredRatio`](#luredratio)
        - [Pros](#pros)
        - [Cons](#cons)
    - [`atkAcc` clamping](#atkacc-clamping)
        - [Pros](#pros-1)
        - [Cons](#cons-1)
- [appendix (a.k.a. random garbage)](#appendix-aka-random-garbage)
    - [why is lure kind of broken no matter how much you nerf and/or buff it?](#why-is-lure-kind-of-broken-no-matter-how-much-you-nerf-andor-buff-it)

<!-- /TOC -->

## general attitude/philosophy (prelude)

## gag buffs/nerfs

### trap

Does trap need to undergo some kind of balancing of its own? Maybe. If sound is
nerfed (see the section on sound), then that might be enough to incidentally
make trap balanced; the fact remains that without *any* balancing efforts
(read: TTR), trap remains the least popular gag (at least amongst 6-trackers).
Notice that this doesn&rsquo;t *necessarily* imply that trap is underpowered
(and thus unbalanced); perhaps people just routinely underestimate the utility
of a guaranteed stun for lure, and/or fail to imagine sufficiently clever ways
of using trap gags in combination with other gags to kill cogs. Also note that,
besides nerfing sound (and thus making lure more of an option&hellip; putting
aside lure nerfs) making trap more appealing, it also makes sense to consider
accuracy changes: see the section on `atkAcc` clamping that explains how stuns
(and thus trap) would be more useful with a different method of clamping
`atkAcc`.

Nevertheless, it&rsquo;s at least worth exploring a few conservative balancing
options.

|            | Banana Peel | Rake        | Marbles     | Quicksand   | Trapdoor     | TNT           | Railroad      |
| ---------- | ----------- | ----------- | ----------- | ----------- | ------------ | ------------- | ------------- |
| TTR        | 12 (**13**) | 20 (**22**) | 35 (**38**) | 50 (**55**) | 70 (**77**)  | 180 (**198**) | 195 (**214**) |
| &delta;TTR |             | +8          | +15         | +15         | +20          | +110          | +15           |
| A          | 12 (**13**) | 20 (**22**) | 36 (**39**) | 60 (**66**) | 92 (**101**) | 156 (**171**) | 188 (**206**) |
| &delta;A   |             | +8          | +16         | +24         | +32          | +64           | +32           |
| B          | 12 (**13**) | 20 (**22**) | 36 (**39**) | 60 (**66**) | 92 (**101**) | 180 (**198**) | 196 (**215**) |
| &delta;B   |             | +8          | +16         | +24         | +32          | +88           | +16           |
| C          | 12 (**13**) | 20 (**22**) | 35 (**38**) | 56 (**61**) | 82 (**90**)  | 172 (**189**) | 198 (**217**) |
| &delta;C   |             | +8          | +15         | +21         | +26          | +90           | +26           |
| D          | 19 (**20**) | 28 (**30**) | 39 (**42**) | 51 (**56**) | 82 (**90**)  | 172 (**189**) | 183 (**201**) |
| &delta;D   |             | +9          | +11         | +12         | +31          | +90           | +11           |

|     | level 5 cog                    | level 6 cog                     | level 7 cog                                       | level 8 cog                                           | level 9 cog                | level 10 cog                                                                                         | level 11 cog                                                                               | level 12 cog                                                                      |
| --- | ------------------------------ | ------------------------------- | ------------------------------------------------- | ----------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| TTR | 1 Quicksand                    | 1 Trapdoor                      | 1 TNT<br />**1 Trapdoor**                         | 1 TNT                                                 | 1 TNT                      | 1 TNT                                                                                                | 1 TNT                                                                                      | **1 Railroad**                                                                    |
|     | "                              | "                               | 1 Quicksand &amp; 1 Fruit Pie<br />**1 Trapdoor** | 1 Trapdoor &amp; 1 Seltzer                            | 1 Trapdoor &amp; 1 Cream   | **1 Trapdoor** &amp; 1 Safe<br />1 Trapdoor &amp; **1 Safe**                                         | **1 Trapdoor** &amp; 1 Storm<br />1 Trapdoor &amp; **1 Storm**                             | 1 TNT &amp; 1 Seltzer                                                             |
| A   | 1 Quicksand                    | 1 Quicksand                     | 1 Trapdoor                                        | 1 Trapdoor                                            | 1 TNT                      | 1 TNT                                                                                                | 1 TNT                                                                                      | **1 Railroad**                                                                    |
|     | "                              | "                               | "                                                 | "                                                     | 1 Trapdoor &amp; 1 Seltzer | 1 Trapdoor &amp; 1 Cream                                                                             | 1 Trapdoor &amp; 1 Storm<br />**1 Trapdoor** &amp; 1 Safe<br />1 Trapdoor &amp; **1 Safe** | 1 TNT &amp; 1 Big Weight<br />**1 TNT** &amp; 1 Hose<br />1 TNT &amp; **1 Cream** |
| B   | 1 Quicksand                    | 1 Quicksand                     | 1 Trapdoor                                        | 1 Trapdoor                                            | 1 TNT                      | 1 TNT                                                                                                | 1 TNT                                                                                      | **1 Railroad**                                                                    |
|     | "                              | "                               | "                                                 | "                                                     | 1 Trapdoor &amp; 1 Seltzer | 1 Trapdoor &amp; 1 Cream                                                                             | 1 Trapdoor &amp; 1 Storm<br />**1 Trapdoor** &amp; 1 Safe<br />1 Trapdoor &amp; **1 Safe** | 1 TNT &amp; 1 Seltzer                                                             |
| C   | 1 Quicksand                    | 1 Quicksand                     | 1 Trapdoor                                        | 1 TNT<br />**1 Trapdoor**                             | 1 TNT                      | 1 TNT                                                                                                | 1 TNT                                                                                      | **1 Railroad**                                                                    |
|     | "                              | "                               | "                                                 | 1 Trapdoor &amp; 1 Glass Of Water<br />**1 Trapdoor** | 1 Trapdoor &amp; 1 Hose    | 1 Trapdoor &amp; 1 Safe<br />**1 Trapdoor** &amp; 1 Big Weight<br />**1 Trapdoor** &amp; **1 Cream** | 1 Trapdoor &amp; 1 Storm<br />**1 Trapdoor** &amp; **1 Safe**                              | 1 TNT &amp; 1 Hose                                                                |
| D   | 1 Quicksand<br />**1 Marbles** | 1 Trapdoor<br />**1 Quicksand** | 1 Trapdoor                                        | 1 TNT<br />**1 Trapdoor**                             | 1 TNT                      | 1 TNT                                                                                                | 1 TNT                                                                                      | **1 Railroad**                                                                    |
|     | "                              | "                               | "                                                 | 1 Trapdoor &amp; 1 Glass Of Water<br />**1 Trapdoor** | 1 Trapdoor &amp; 1 Hose    | 1 Trapdoor &amp; 1 Safe<br />**1 Trapdoor** &amp; 1 Big Weight<br />**1 Trapdoor** &amp; **1 Cream** | 1 Trapdoor &amp; 1 Storm<br />**1 Trapdoor** &amp; **1 Safe**                              | 1 TNT &amp; 1 Seltzer                                                             |

A is a sort of &ldquo;rationalization&rdquo; of TTR, so that the deltas mostly
go up by 8 each time, and otherwise are powers of 2. This has the effect of
making Marbles, Quicksand, and especially Trapdoor considerably more powerful,
but TNT considerably weaker (although still just enough to one-shot a level 11
v1.0 cog). Compared to TTR this actually seems to lower the use for organic
trap by a bit, although having a 171-damage TNT instead of 156 actually is
quite a bit better than going from 180 to 198 damage. Still, having to use a
Big Weight on a level 12 cog that is being TNT&rsquo;d is not really so bad
considering that the Big Weight has two stuns counting towards its accuracy,
and it&rsquo;s only a level 4 gag.

B is just A but adjusted to have the same TNT damage as TTR. This may look fine
for balancing trap but doesn&rsquo;t look quite so good for balancing organic
trap.

C is similar to A in that it makes Quicksand and Trapdoor considerably
stronger, but nerfs TNT a bit, and also in that it is a sort of
&ldquo;rationalization&rdquo; of TTR: the deltas make use of the sequence
\[(0,&nbsp;)8, 15, 21, 26\], which follows the recurrence relation
*a*<sub>*n*</sub>&nbsp;=&nbsp;2*a*<sub>*n*-1</sub>&nbsp;-&nbsp;*a*<sub>*n*-2</sub>&nbsp;-&nbsp;1.
This is, in some sense, the opposite of the method used in the sound section,
where the deltas have a slope of +1 (rather than -1 as they do here).

D is similar to C but without the &ldquo;rationalization&rdquo;; the only
important changes are to the damage of level &le;4 trap gags. Rather than
choosing nice damage numbers or deltas, the damage figures are increased just
enough to make it so that organic versions of the gags are able to one-shot a
cog that is one higher level. In my opinion, if trap were to be balanced, this
is probably the way to do it. The numbers are not as nice, but the effect is to
make both inorganic and organic trap more useful at all stages of the game. In
any case, the deltas still have the interesting(?) property that they alternate
between being prime and composite, and this pattern is maintained even if you
introduce a fictional &ldquo;level 0&rdquo; trap gag that does 0 damage. The
damage for Railroad is chosen by selecting a delta value that has already been
used (viz. +11).

### lure

Format:

rounds; `propAcc`/**organic `propAcc`**

|     | $1 Bill      | Small Magnet | $5 Bill      | Big Magnet   | $10 Bill     | Hypno        | Presentation   |
| --- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | -------------- |
| TTR | 2; 50/**60** | 2; 50/**60** | 3; 60/**70** | 3; 60/**70** | 4; 70/**80** | 4; 70/**80** | 15; 90/**100** |
| A   | 1; 50/**60** | 1; 50/**60** | 1; 60/**70** | 1; 60/**70** | 1; 70/**80** | 1; 70/**80** | 15; 90/**100** |
| B   | 1; 50/**70** | 1; 50/**70** | 1; 60/**80** | 1; 60/**80** | 1; 70/**90** | 1; 70/**90** | 15; 90/**110** |
| C   | 2; 50/**60** | 1; 50/**60** | 2; 60/**70** | 1; 60/**70** | 2; 70/**80** | 1; 70/**80** | 15; 90/**100** |
| BC  | 2; 50/**70** | 1; 50/**70** | 2; 60/**80** | 1; 60/**80** | 2; 70/**90** | 1; 70/**90** | 15; 90/**110** |
| D   | 2; 40/**70** | 1; 40/**70** | 2; 50/**80** | 1; 50/**80** | 2; 60/**90** | 1; 60/**90** | 15; 90/**120** |

Excluding TTR, BC is the strongest here, and A is the weakest. It&rsquo;s not
immediately clear how B, C, and D stack up in terms of strength because they
make some orthogonal changes.

The purpose of A is clear: the accuracy of lure tends to not really be a
problem, so we might as well be conservative there and instead drop the number
of rounds for all lure gags (except level 7) to 1. This makes A the sort of
&ldquo;minimal change&rdquo; needed to &ldquo;balance&rdquo; lure, because it
means that lure is still quite useful for one round of damage mitigation and
effectively two rounds of extra cog-fighting power (although you can only use
trap gags in the first such round, and the first round only has up to a maximum
of 3 attackers), but not so powerful that you can effectively mitigate *all*
damage (assuming the best case of lure never missing).

One problem with A might be that since it doesn&rsquo;t touch `propAcc` values,
organic lure still kind of sucks. With the accuracy changes mentioned in the
accuracy section it&rsquo;s not so bad (compared to in TTR), but still probably
not worth it. B is a stronger version of A that is only stronger if you have
organic lure; `propAcc` gets increased by 20 instead of the usual 10, making
organic lure effectively worth an entire stun rather than half of a stun.

Another problem with A is that it makes single-target lure look even less
appealing than in TTR. Single-target lures are already not used nearly as often
as their multi-target counterparts in TTR, but with only 1 round of
effectiveness for multi- and single-target lures, you can&rsquo;t e.g.
&ldquo;lure left kill right&rdquo; one-by-one and use single-target lures to
get the left-side cogs, &amp;c. To remedy this, C doubles the number of rounds
of effectiveness for single-target lures only.

BC combines B and C and thus is more powerful than either, and also attempts to
fix both problems with A. In case BC was too powerful and/or the problem of
organic lure wasn&rsquo;t solved enough, D is a weakened version of BC that
makes organic lure effectively worth a stun and a half, but lowers inorganic
lure `propAcc` by 10 at all levels (except 7). This may seem harsh (and indeed,
it is perhaps unfortunate that making organic lure last for more rounds
isn&rsquo;t really viable and so D relies on making inorganic lure *more
fickle*), but all is not lost for inorganic lure users so long as their friends
stun dilligently enough to reach an acceptable(!) rate of success.

### sound

|            | Bikehorn  | Whistle   | Bugle       | Aoogah      | Trunk       | Fog         | Opera       |
| ---------- | --------- | --------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| TTR        | 4 (**5**) | 7 (**8**) | 11 (**12**) | 16 (**17**) | 21 (**23**) | 50 (**55**) | 90 (**99**) |
| &delta;TTR |           | +3        | +4          | +5          | +5          | +29         | +40         |
| A          | 4 (**5**) | 7 (**8**) | 11 (**12**) | 16 (**17**) | 22 (**24**) | 29 (**31**) | 40 (**44**) |
| &delta;A   |           | +3        | +4          | +5          | +6          | +7          | +11         |
| B          | 4 (**5**) | 7 (**8**) | 11 (**12**) | 16 (**17**) | 22 (**24**) | 30 (**33**) | 50 (**55**) |
| &delta;B   |           | +3        | +4          | +5          | +6          | +8          | +20         |

|     | level 8 cog                                                           | level 9 cog                                         | level 10 cog                                     | level 11 cog                                                                                   | level 12 cog                                        |
| --- | --------------------------------------------------------------------- | --------------------------------------------------- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| TTR | 3 Trunk &amp; 1 Aoogah<br />2 Trunk &amp; **1 Aoogah** &amp; 1 Aoogah | 1 Fog &amp; 2 Aoogah &amp; 1 Bugle<br />**4 Trunk** | 1 Fog &amp; 3 Trunk                              | 2 Fog &amp; 2 Aoogah                                                                           | 3 Fog &amp; 1 Aoogah                                |
| A   | 2 Trunk &amp; 2 Aoogah                                                | 1 Fog &amp; 3 Trunk<br />**2 Trunk** &amp; 2 Trunk  | 4 Fog<br />3 Fog &amp; **1 Trunk**               | 2 Opera &amp; 1 Fog &amp; 1 Trunk<br />**1 Opera** &amp; 3 Fog                                 | **2 Opera** &amp; 2 Opera                           |
| B   | "                                                                     | "                                                   | 3 Fog &amp; 1 Trunk<br />**2 Fog** &amp; 2 Trunk | 1 Opera &amp; 2 Fog &amp; 1 Trunk<br />**1 Opera** &amp; 1 Fog &amp; **1 Trunk** &amp; 1 Trunk | 3 Opera &amp; 1 Aoogah<br />2 Opera &amp; **2 Fog** |

Note that the primary difference (assuming 4 toons with max sound) between A
and B is that in cases where no toons have organic sound, you need one fewer
Fog to defeat a row of level 10 cogs with B. Assuming no restocks (and 3 Fogs
per toon), you have enough Fogs to do this 3 times (4 with &ge;1 organic sound)
with A and 4 times (6 with 4 organic sound) with B. Note that this also makes
organic sound actually quite a bit more useful with A, since you only need 1
organic sound to make a difference.

Taking out a row of level 10s is pretty powerful, and *probably* still viable
if you have, say, a row of two &le;10s and two 11s, or three &le;10s and one
level &ge;11&hellip; One of the reasons that it&rsquo;s best to err on the side
of less power is that if sound is nerfed (relative to TTR), having even one
soundless (or simply unmaxed sound) toon dampens the possibilities
considerably, in contrast to TTR, where sound is so powerful that only 3 toons
with sound gets you quite far in terms of sound spam. Removing a bit *more*
power obviously has the potential to make this worse, but mostly just makes it
more clear that sound spam is typically not an option (at least, not in the way
that a TTR player is accustomed). Ideally, all possible 6-track builds should
be *roughly* equally viable (toonupless, trapless, lureless, soundless,
throwless, squirtless, dropless). In this case, we expect that &mdash; again,
roughly &mdash; 1 out of every 7 &ldquo;normal&rdquo; (read: 6-track) toons is
soundless.

## accuracy

### `luredRatio`

Assuming that all toons have their gag tracks maxed, `luredRatio` only makes a
difference in TTR in *one* situation: using throw gag(s) on an unlured level
&ge;10 cog, with no stun, while at least one other cog is lured. This is
unfortunate, because:

* This is a very niche use-case that doesn&rsquo;t need to be serviced,
  especially considering that even a single stun will negate the usefulness of
  `luredRatio`.
* Having a mechanic like `luredRatio` unnecessarily complicates accuracy
  calculation.

The proposal is to get rid of `luredRatio` wholesale, and collapse `bonus` and
`prevHits` so that they are the same by definition.

#### Pros

* Simplifies accuracy calculation.

#### Cons

None.

### `atkAcc` clamping

In TTR, we have:

```python
atkAcc = propAcc + trackExp + tgtDef + bonus
```

Where `propAcc` is fixed for each particular gag, `trackExp` depends on the
level of the highest gag that the gag user has access to within the relevant
track, `tgtDef` depends on the cog&rsquo;s level, and `bonus` is mostly just
stun (and `luredRatio`, but `luredRatio` is to be gotten rid of, and only ever
applied in very niche situations anyways).

Again, also in TTR, `atkAcc` is actually clamped to a maximum of 95 and a
minimum of 0 (implementation-wise there is no minimum, but it&rsquo;s easier to
think of it as having a minimum of 0 so that you can think of `atkAcc` as just
being the percentage chance; there&rsquo;s no material difference either way).

Below are (Python) functions `ttr_clamp_acc` and `clamp_acc`, which correspond
to TTR&rsquo;s method of clamping `atkAcc` after it is calculated as the sum of
the four aforementioned numbers, and the proposed method of doing the same
thing, respectively.

```python
def ttr_clamp_acc(atkAcc):
    return max(min(atkAcc, 95), 0)

def clamp_acc(atkAcc):
    if atkAcc <= 95:
        return max(atkAcc, 0)
    else:
        return min(95 + (atkAcc - 95) / 10, 100)
```

<small>Minor note: Python doesn&rsquo;t have types, but it does have data
types, and the above two functions have different return (data) types, namely
`ttr_clamp_acc: int -> int` and `clamp_acc: int -> (int | float)`. But really,
it doesn&rsquo;t matter&hellip; just be sure not to somehow trip on
that.</small>

The tweakable parameter of `clamp_acc` is the `10` that shows up in its
definition. `10` is a convenient number because it gives what I think is a
reasonable slope while also being very easy to calculate in your head (assuming
you&rsquo;re working in base 10, you just move the decimal point one place to
the left). The magic number here is thus 145, because it is exactly when
`atkAcc >= 145` that the gag is guaranteed to hit.

#### Pros

* Makes accuracy more meaningful in general, because its value changes more
  freely to reflect the strategy being used.
* Particularly, makes stunning more meaningful because it creates a nonzero
  benefit in many more cases.
* Makes the game less reliant on dumb luck by allowing accuracy to be pushed
  beyond the 95% mark (with the right gag picks), even up to 100%.

#### Cons

* Complicates accuracy calculation.
* This change would raise the overall power level of toons, since in some cases
  it improves accuracy, and in all other cases it keeps accuracy the same. This
  could be a con.
* Allowing accuracy to possibly reach 100% could be seen as overly rigid or
  deterministic(&#x203d;)

## appendix (a.k.a. random garbage)

### why is lure kind of broken no matter how much you nerf and/or buff it?

**WARNING: this section contains a larger-than-usual dose of personal opinion.
Caveat lector.**

There is a part of lure gags as a mechanic that will always be a *little bit*
broken regardless of how you tweak the parameters. By parameters I mean the
number of rounds that various lure gags (organic, and inorganic) last,
`propAcc` for various lure gags (organic, and inorganic), and how many cogs
that various lure gags (organic, and inorganic) target (1, up to 2, up to 3, or
just however many cogs are unlured at the time).

Imagine, as a simple example, that you have a party with an even spread of
lureless toons and lure toons: 2 of each. The party is fighting a row of level
&ge;10 cogs, and they decide to lure all the cogs (with Hypno, let&rsquo;s
say). In TTR, they can probably continue fighting just using lure (and some
assortment of trap, throw, squirt, and maybe some drop) even if more cogs join
the battle (like in one of the boss battles). When tweaking the parameters of
lure gags to balance this, there are *broadly* two scenarios that come up:

Scenario 1: you, in some way, nerf the accuracy of lure in an attempt to
balance it. This has the very clear and unfortunate disadvantage that this
makes the game (particularly lure, of course) even more reliant on dumb luck.
Generally, you **(a)** get lucky and have the lures mostly work and arrive back
at what looks like TTR lure-based gameplay, **(b)** put a lot of effort into
stunning in order to make the accuracy hover around 85~95% again and thus
arrive back at what still looks like TTR lure-based gameplay (but with more
stunning, which doesn&rsquo;t matter too much considering how long the lure
gags&rsquo; effects last), or **(c)** you don&rsquo;t stun well enough and/or
don&rsquo;t get particularly lucky and thus (seemingly inexplicably) keep
face-tanking cog hits while performing an unusual number of lureless kills
(viz. unusual for a lure-based context). In addition to the aforementioned
disadvantage of making things more reliant on dumb luck in many cases, none of
these 3 outcomes seem particularly appealing; none of them actually seem to
&ldquo;balance&rdquo; lure.

An additional thing to note is that in outcome **(c)**, the &ldquo;lureless
kills&rdquo; in question are not as desirable as they might sound at first:
because they are effectively &ldquo;accidental&rdquo; in some sense (because
they are the result of dumb luck making lure gags miss), they don&rsquo;t look
like actual lureless play, and generally take one of two forms: **(c0)** some
gag(s) are used on a cog as it is lured, but the lure misses and so the gag(s)
do not kill the cog; the cog is killed at some point, but it takes more rounds
than expected, or **(c1)** the gag strategy chosen is a so-called
&ldquo;insurance strategy&rdquo;, and so the cog dies in one round regardless
or whether or not lure hits (assuming the other gag(s) hit). In particular,
**(c0)** is obviously not what anyone really wants from (quasi-)lureless play,
and **(c1)** is nicer but makes especially clear the problem of lure being
entirely dumb luck; you hope that the lure hits, but don&rsquo;t (read: cannot)
expect it to, and when does hit, it just acts as a way of saving some
resources. But making this lure&rsquo;s niche as a gag track is *probably* a
recipe of making lure unappealing in general and thus unbalanced. Also, the
fact remains that you can never rely on lure for anything *remotely* critical
in either **(c0)** or **(c1)**.

Scenario 2: you, in some way, nerf the duration of lure gags in general in an
attempt to balance the gag track. At first, this seems nicer than Scenario 1,
since it doesn&rsquo;t make lure any more fickle than it has to be. But there
is a sneakier, more subtle reason as to why this scenario is still &ldquo;kind
of broken&rdquo;, regardless of whether or not it is combined with Scenario 1.
The reason that I use the phrase &ldquo;kind of broken&rdquo; is because it
depends on your perspective as to whether this is a real problem, a minor
problem, or a complete non-issue.

To illustrate, imagine a simple example where Hypno is a gag that works
identically to how it does in TTR, with the exception that it lasts for just 1
round (rather than 4). Choosing 1 round in particular is *somewhat* arbitrary
(2 rounds *could* be a possibility as well), but much more than 1 round, and
you aren&rsquo;t really nerfing it, and 1 round is the simplest to work with
anyways. When one toon chooses Hypno, the 3 other toons have the opportunity to
pick other non-lure gags; in many cases this will be somewhere between 0 and 2
toonup gags and the rest being attack gags like trap, throw, and squirt.
Assume, for simplicity, that the lure hits. The attack gag(s) are used, and
some cog(s) still remain both alive and lured. The damage that said cogs would
otherwise do immediately after the toons finished using their attack gag(s) is
prevented because they are lured; this is part of the point of using lure in
the first place. If no new cogs join between the time of the attack gag(s)
being used and the next time that the toons get to make gag choices, *and* all
of the remaining (lured) cogs can be taken out with just the gags that are
chosen in that very next round, then great. The cogs are defeated, and the
toons never had to deal with any pesky cogs becoming unlured. But in the case
that these two conditions are not *both* met, some cog(s) will automatically be
unlured after the toons use their attack gags for the second time (or they do
actually get defeated, and it is not until the stream of incoming cogs starts
to overwhelm the toons&rsquo; resources &amp; luck that this automatic unluring
occurs; either way, it happens).

While this seems fine and dandy &mdash; after all, this is basically the point
of nerfing lure gag durations &mdash; the problem comes from the awkward
ordering in which things occur when a cog is automatically unlured. When the
cog(s) automatically unlure after the toons have used their gags, the
*immediate* next thing that happens is that the automatically unlured cog(s)
attack the toons. In the context of TTR, this makes a great deal of sense:
unluring a cog can make sense for various reasons (including killing it
outright), but allowing a cog&rsquo;s lured-state duration to elapse and thus
*automatically* get unlured is basically *always a mistake*, and thus gets
swiftly punished. When nerfing (and rightly so, I might add) lure via what is
here called Scenario 2 (or any combination of Scenarios 1 and 2), this makes
considerably less sense, for two related reasons: **(a)** swiftly punishing
toons for allowing lure to expire seems to make less sense when the lure is
*designed* to expire quickly, and **(b)** this mechanic (so far as I can tell)
seems to inherently make it more difficult to reconcile lure-based play and
lureless play; despite the fact that the cogs get automatically unlured, there
is little chance for toons to plan ahead and take advantage of their knowledge
of when cogs will automatically unlure, because the cog will take a whiff at
them anyways before the next round comes and they have the chance to re-lure
the cog anyways.

To give a (very) simple example that hopefully makes **(b)** more clear,
imagine a lured level 11 cog that is going to get unlured as soon as the next
round of toon attacks ends. In anticipation of it getting unlured, I might use
a Piano gag on it (Piano, just because it does enough damage to one-shot a
level 11 v1.0 cog). But if I *actually* did that, the Piano would just miss
(since the cog is lured and drop gags have a fixed 0% accuracy on lured cogs),
and then the cog would immediately unlure and attack me. Again, depending on
your perspective, this may or may not seem wonky in a bad way.

There are, of course, some reassurances that can be afforded to both **(a)**
and **(b)**, which I will address here. One could reframe **(a)** as not being
a swift punishment for allowing a cog&rsquo;s lured-state to expire, but rather
an occasional punishment that is inherent to using lure gags at all; that is,
it is just part of lure itself that you have to be wise to only use lure when
you know that you can face-tank the requisite number of cog attacks (or have a
way to dispose of the cogs swiftly enough to avoid said face-tanking). As a
rationale, I think that this is actually fine and good, but I would note that
this attitude *could possibly* have the effect of balancing lure too much into
the realm of &ldquo;only marginal usefulness&rdquo;. For **(b)**, as far as I
can tell, there are two (not mutually exclusive) ways of assuaging its concern:
you can either not care and be fine with this kind of friction between
lure-based play and lureless play, or you can insist that sound gags
&ldquo;solving&rdquo; the problem in certain edge cases is sufficient to make
things work.

When I say that sound gags &ldquo;solve&rdquo; the problem in certain edge
cases, I basically just mean that the use of drop gags can be afforded on
certain cogs that are about to be automatically unlured, with the use of one or
more sound gag(s). Of course, this has two problems: one is that this only
actually makes sense in cases where the cogs not being dropped on have low
enough HP (either from being low level, or from being hit in some previous
round(s)) to all (or at the least, all except one) die to the sound gag(s). If
this condition isn&rsquo;t met, then it is almost certainly better to do
something else (probably just aggressively luring). The other problem is that
what is *really* going on here is a shortening of the lure gag&rsquo;s effect
duration by 1 round via the use of sound gag(s). Yes, this technically allows
you to take shots at the cog(s) before they get their free attack(s) on you
(viz. the attack(s) that they get for being automatically unlured), but part of
the price that you pay is that you effectively shorten by &frac12; the number
of rounds that the lure gag&rsquo;s effects last. The effective shortening is
because sound gags have low damage-per-(lured-)cog, come before all the other
gag tracks that can be used to attempt to damage lured cogs (viz. throw,
squirt, &amp; drop), *and* get no bonus damage (read: orange damage) on lured
cogs. The sound thus effectively acts as a low-damage wakeup. The side-effect
of effectively shortening lure effect durations by &frac12; rounds is somewhat
troubling when we are generally talking about lure gags whose effects last for
around 1 round each. So, again, the coexistence of lure-based play and lureless
play still has the same friction and the problem doesn&rsquo;t really seem to
be solved (excepting perhaps some edge cases).
