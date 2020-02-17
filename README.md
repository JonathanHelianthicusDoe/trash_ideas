# garbage/useless tt ideas

## gag buffs/nerfs

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

#### why is lure kind of broken no matter how much you nerf and/or buff it?



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
