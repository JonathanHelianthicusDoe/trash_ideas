# garbage/useless tt ideas

<!-- TOC depthFrom:2 -->

- [general attitude/philosophy (prelude)](#general-attitudephilosophy-prelude)
    - [what about other (non-TTR) servers, though?](#what-about-other-non-ttr-servers-though)
- [gag buffs/nerfs](#gag-buffsnerfs)
    - [toonup](#toonup)
        - [organic toonup](#organic-toonup)
        - [Bamboo Cane](#bamboo-cane)
        - [balancing](#balancing)
    - [trap](#trap)
    - [lure](#lure)
        - [balancing numerically](#balancing-numerically)
        - [balancing mechanically](#balancing-mechanically)
            - [pros](#pros)
            - [cons](#cons)
    - [sound](#sound)
- [accuracy](#accuracy)
    - [`luredRatio`](#luredratio)
        - [pros](#pros-1)
        - [cons](#cons-1)
    - [`atkAcc` clamping](#atkacc-clamping)
        - [pros](#pros-2)
        - [cons](#cons-2)
- [facilities](#facilities)
    - [barriers to entry](#barriers-to-entry)
        - [factories: the side entrance](#factories-the-side-entrance)
        - [factory-like facilities](#factory-like-facilities)
    - [gag retention](#gag-retention)
- [cogs](#cogs)
- [toontasks](#toontasks)
- [appendix (a.k.a. random garbage)](#appendix-aka-random-garbage)
    - [why is lure kind of broken no matter how much you nerf and/or buff it?](#why-is-lure-kind-of-broken-no-matter-how-much-you-nerf-andor-buff-it)

<!-- /TOC -->

## general attitude/philosophy (prelude)

TTO/TTR (henceforth TTR, because TTO no longer exists) is an excellent game,
but suffers (as so many games do) from some design decisions that unfortunately
were not quite prescient enough to see into the far future. There are issues of
balance: between gag tracks, between cogs and toons, &amp;c. There are issues
of overly restrictive gameplay, and gameplay not adapted to the ways that
players have shaped it. It has historically been generally wise to adapt games
to the ways that players have intentionally adjusted them for the purpose of
fun. This document catalogues some very concrete proposed changes that
typically err on the side of only that which is needed to improve the game,
rather than change the game unnecessarily or add to it. See my open letter,
[&ldquo;On sellbot field offices (SBFOs), especially concerning the problem of
&lsquo;difficulty&rsquo; in
Toontown&rdquo;](https://gist.github.com/JonathanHelianthicusDoe/e5a261941bfa0f29148a6999b6ca7a65)
if you are interested in more abstract considerations of the kind mentioned in
this paragraph.

Some of the changes proposed here are meant to be combined with other such
changes, but some may be designed *without* other changes in mind, for the sake
of independence and flexibility.

While the changes made here are obviously, first and foremost, changes made to
balance the game and make it more fun, there are also some aesthetic
considerations to fill in the gaps. Mostly, this comes in the form of what
numbers are chosen in cases where numeric values are being balanced. The
tendency is to favor numbers that are more &ldquo;round&rdquo; (read:
[regular](https://en.wikipedia.org/wiki/Regular_number), or its synonym,
5-[smooth](https://en.wikipedia.org/wiki/Smooth_number)), and to favor
[sequences](https://en.wikipedia.org/wiki/Sequence) and mathematical
[functions](https://en.wikipedia.org/wiki/Function_(mathematics)) that are more
[&ldquo;beautiful&rdquo;](https://en.wikipedia.org/wiki/Mathematical_beauty).
In this document, heeding these aesthetic concerns is referred to as
&ldquo;rationalization&rdquo; (both in the mathematical sense, from
&ldquo;ratio&rdquo;, and the usual sense of &ldquo;to give a rationale&rdquo;).
Again, these concerns are always strictly secondary to the more important
concerns of game balance and fun.

### what about other (non-TTR) servers, though?

Other servers besides TTR exist, but are often dedicated to &ldquo;adding
to&rdquo; the base game and/or &ldquo;modernizing&rdquo; it. While these are
certainly noble goals, they often amount to addition for the sake of addition
(e.g. entirely new cog types, entirely new gag tracks, &amp;c.) and revisionism
for the same of revisionism (a kind of pathological uniqueness). This document
instead focuses on TTR-as-essentially-TTO, that is, the &ldquo;base game&rdquo;
in more or less the same state gameplay-wise as TTO in 2013. This acts as a
starting point, or even <i>tabula rasa</i> (a <i>tabula rasa</i> that, like a
newborn human mind, is not really a &ldquo;blank&rdquo; slate at all&hellip;).

## gag buffs/nerfs

### toonup

Balancing toonup gags is a bit of a different beast than balancing any of the
other six tracks; rather than balancing the tracks against themselves, toonup
is fundamentally different and can only be balanced from a perspective that
includes not just the HP of cogs, but also the attacking power of cogs and the
cog-elimating powers of the other six gag tracks.

In TTR, toonup is very much overpowered, because lure and sound are powerful
enough to make laff loss a relatively rare event. Whenever toonup is eventually
used, it does the job with just 1 or 2 gags. With nerfs to lure and sound
making cogs *generally* (buffs to trap notwithstanding) more difficult to
defeat, this effect should be counteracted a bit and thus make toonup not so
overpowered.

That being said, there are still two outstanding problems with toonup:

- Organic toonup is still probably underpowered even after nerfing lure and
  sound.
- Bamboo Cane does worryingly little damage compared to the other toonup gags.

#### organic toonup

It&rsquo;s well-known that in TTR, organic toonup is incredibly underpowered.
It is, by far, the least powerful out of the seven possible tracks that can be
made organic. Partly, this is due to toonup just being overpowered; since each
toonup gag already does so much healing, adding just a tad extra is not going
to be useful or even noticable. As a result, nerfing lure and sound, and thus
making toonup less overpowered (relatively), already ameliorates the problem of
organic toonup.

But there is another reason why organic toonup is so underpowered, and it has
to do with the fact that toonup is fundamentally different from the other six
gag tracks. With other gag tracks (particularly trap, sound, throw, squirt, and
drop), very slight differences in a gag&rsquo;s damage can make the difference
between a cog not dying and a cog dying, simply because a cog with 1 HP is
alive and one with 0 HP is not. Strictly speaking, a similar principle does
apply to toonup: very slight differences in healing amounts can make the
difference between a toon being fully healed and a toon not being fully healed,
simply because a toon with 1 laff fewer than their max laff is not fully
healed, and a toon with laff equal to their max laff is. But the difference
between a toon with laff 1 fewer than their maximum and a cog with 1 HP is very
stark. Getting a toon to the point of having 1 laff missing is &ldquo;good
enough&rdquo;; it is not the same, but is nevertheless nearly indistinguishible
from, having full laff. But a cog with 1 HP is *not* &ldquo;good enough&rdquo;;
that cog still occupies a space in battle and can attack the toons at will,
very unlike one with 0 HP.

This fundamental difference is not something to get rid of. It is just an
inherent part of toonup affecting *toons* rather than cogs (unlike the other
six gag tracks). Rather than trying to smooth over this fundamental difference,
the best thing to do is to treat it like it is rather than trying to make
organic toonup *look like* organic versions of other gag tracks. Making organic
toonup gags do (roughly) 10% more healing than their inorganic counterparts is
appealing because of its perceived consistency; but as is explained here, this
consistency is only perceived, not actual.

#### Bamboo Cane

In TTR, the Bamboo Cane gag just intuitively feels a bit underwhelming compared
to the other six toonup gags. But is that feeling justified? Here are a few
quantitative ways of looking at this question.

How much healing does the Bamboo Cane do in proportion to the other
multi-target toonup gags (not including the level 7 gag)? The Bamboo Cane does
45/18&nbsp;=&nbsp;2.5 times more than the Megaphone, but the Juggling Balls do
120/45&nbsp;=&nbsp;2.666&hellip; times more than the Bamboo Cane. From this
perspective, the Bamboo Cane is slightly underpowered.

How much single-target healing does the Bamboo Cane do compared to its
corresponding single-target toonup gag? The Megaphone does 6/10&nbsp;=&nbsp;0.6
times as much healing as the Feather. The Juggling Balls do
40/70&nbsp;=&nbsp;0.571428&hellip; times as much healing as the Pixie Dust. The
Bamboo Cane does 15/30&nbsp;=&nbsp;0.5 times as much healing as the Lipstick.
From this perspective, the Bamboo Cane is underpowered.

How does the Bamboo Cane&rsquo;s healing amount look in the context of
toonup-gag-healing-amount-growth as a function of gag level?

|                   | Feather | Megaphone | Lipstick | Bamboo Cane | Pixie Dust | Juggling Balls | High Dive |
| ----------------- | ------- | --------- | -------- | ----------- | ---------- | -------------- | --------- |
| TTR               | 10      | 18        | 30       | 45          | 70         | 120            | 210       |
| &delta;TTR        |         | +8        | +12      | +15         | +25        | +50            | +90       |
| &delta;&delta;TTR |         |           | +4       | +3          | +10        | +25            | +40       |

As can be seen from the &delta;&delta;TTR row, the Bamboo Cane is the only
toonup gag where the toonup-gag-healing-amount-growth takes a noticable
&ldquo;dip&rdquo; or &ldquo;decline&rdquo; (in particular, note the dip from +4
down to +3). From this perspective, the Bamboo Cane is underpowered.

So it seems that the feeling that the Bamboo Cane gag is a bit underwhelming
*is* actually justified. What, then, should be the healing amount of the Bamboo
Cane? The most obvious choice is 48, since it&rsquo;s the next multiple of 3
after 45. 48 actually has the advantage over 45 that it is also divisible by 2
(that is, it&rsquo;s divisible by 6). Divisibility by 6 is particularly nice
for the healing amounts of multi-target toonup gags because, when using a
toonup gag, you are always healing either 1, 2, or 3 toons (since you cannot
toonup yourself). The integers that are divisible by all three of those numbers
are just those integers that are divisible by 6.

With the Bamboo Cane doing 48 laff of healing, it does
48/18&nbsp;=&nbsp;2.666&hellip; times more than the Megaphone, and the Juggling
Balls do 120/48&nbsp;=&nbsp;2.5 times more than the Bamboo Cane. So they have
been swapped in this respect and are as balanced as before (but now the
Juggling Balls are the ones that look slightly underpowered). The Bamboo Cane
would do 16/30&nbsp;=&nbsp;0.5333&hellip; times as much healing as the
Lipstick. This is still less than both 0.6 and 0.571428&hellip;, but still an
improvement. And the toonup gag healing amount table would look like this:

|                 | Feather | Megaphone | Lipstick | Bamboo Cane | Pixie Dust | Juggling Balls | High Dive |
| --------------- | ------- | --------- | -------- | ----------- | ---------- | -------------- | --------- |
| A               | 10      | 18        | 30       | 48          | 70         | 120            | 210       |
| &delta;A        |         | +8        | +12      | +18         | +22        | +50            | +90       |
| &delta;&delta;A |         |           | +4       | +6          | +4         | +28            | +40       |

There is no longer a &ldquo;dip&rdquo; where the Bamboo Cane is, although it
seems that the dip has just moved up by 1 gag level. While this is possibly
unfortunate, it really shouldn&rsquo;t matter, since the Pixie Dust is a
single-target toonup gag; 70 points of healing is a lot for a single toon.
However, it should be noted that bumping Pixie Dust up from 70 to 75 solves
this problem (if it is a problem), and also makes Juggling Balls do
40/75&nbsp;=&nbsp;0.5333&hellip; times as much single-target healing as the
Pixie Dust, which is exactly on par with Bamboo Cane doing
16/30&nbsp;=&nbsp;0.5333&hellip; times as much single-target healing as
Lipstick.

#### balancing

Format:

healing (**organic healing**); `propAcc` (**organic `propAcc`**)

|     | Feather                            | Megaphone                          | Lipstick                           | Bamboo Cane                        | Pixie Dust                         | Juggling Balls                       | High Dive                            |
| --- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- | ------------------------------------ | ------------------------------------ |
| TTR | 10&nbsp;(**11**); 70&nbsp;(**70**) | 18&nbsp;(**19**); 70&nbsp;(**70**) | 30&nbsp;(**33**); 70&nbsp;(**70**) | 45&nbsp;(**49**); 70&nbsp;(**70**) | 70&nbsp;(**77**); 70&nbsp;(**70**) | 120&nbsp;(**132**); 70&nbsp;(**70**) | 210&nbsp;(**231**); 70&nbsp;(**70**) |
| A   | 10&nbsp;(**12**); 70&nbsp;(**70**) | 18&nbsp;(**22**); 70&nbsp;(**70**) | 30&nbsp;(**36**); 70&nbsp;(**70**) | 48&nbsp;(**58**); 70&nbsp;(**70**) | 70&nbsp;(**84**); 70&nbsp;(**70**) | 120&nbsp;(**144**); 70&nbsp;(**70**) | 210&nbsp;(**252**); 70&nbsp;(**70**) |
| B   | 10&nbsp;(**12**); 70&nbsp;(**70**) | 18&nbsp;(**22**); 70&nbsp;(**70**) | 30&nbsp;(**36**); 70&nbsp;(**70**) | 48&nbsp;(**58**); 70&nbsp;(**70**) | 75&nbsp;(**90**); 70&nbsp;(**70**) | 120&nbsp;(**144**); 70&nbsp;(**70**) | 210&nbsp;(**252**); 70&nbsp;(**70**) |
| C   | 10&nbsp;(**12**); 70&nbsp;(**90**) | 18&nbsp;(**22**); 70&nbsp;(**90**) | 30&nbsp;(**36**); 70&nbsp;(**90**) | 48&nbsp;(**58**); 70&nbsp;(**90**) | 70&nbsp;(**84**); 70&nbsp;(**90**) | 120&nbsp;(**144**); 70&nbsp;(**90**) | 210&nbsp;(**252**); 70&nbsp;(**90**) |
| D   | 10&nbsp;(**12**); 70&nbsp;(**90**) | 18&nbsp;(**22**); 70&nbsp;(**90**) | 30&nbsp;(**36**); 70&nbsp;(**90**) | 48&nbsp;(**58**); 70&nbsp;(**90**) | 75&nbsp;(**90**); 70&nbsp;(**90**) | 120&nbsp;(**144**); 70&nbsp;(**90**) | 210&nbsp;(**252**); 70&nbsp;(**90**) |

First note that all proposals (A, B, C, and D) raise the healing amount of
Bamboo Cane from 45 to 48, as per the section on the Bamboo Cane.

A raises the bonus healing amount for having organic toonup by a factor of 2,
from 10% extra (rounded up to the nearest integer, to a minimum of 1 extra) to
20% (ditto). This is mathematically convenient not just because it doubles the
benefit, but because division by 5 is still fairly easy (although not as easy
as by 10) in decimal, and also because this same mechanic of 20%-rounded-up is
also used for yellow damage (`hpBonus`) against cogs, so players are used to
doing this kind of calculation already. Here we can see what impact this has on
per-target healing from multi-target gags:

| Megaphone (2 targets)               | Megaphone (3 targets)                             | Bamboo Cane (2 targets)               | Bamboo Cane (3 targets)                                 | Juggling Balls (2 targets)            | Juggling Balls (3 targets)                              |
| ----------------------------------- | ------------------------------------------------- | ------------------------------------- | ------------------------------------------------------- | ------------------------------------- | ------------------------------------------------------- |
| \[9,&nbsp;9\] (**\[11,&nbsp;11\]**) | \[6,&nbsp;6,&nbsp;6\] (**\[8,&nbsp;7,&nbsp;7\]**) | \[24,&nbsp;24\] (**\[29,&nbsp;29\]**) | \[16,&nbsp;16,&nbsp;16\] (**\[20,&nbsp;19,&nbsp;19\]**) | \[60,&nbsp;60\] (**\[72,&nbsp;72\]**) | \[40,&nbsp;40,&nbsp;40\] (**\[48,&nbsp;48,&nbsp;48\]**) |

The intent of simply increasing the benefits of organic toonup is to make it
more useful and appealing, rather than hoping that the same thing that works
for other tracks (drop, squirt, throw, sound, and trap) will work for a track
that doesn&rsquo;t do any damage to cogs.

B is identical to A except that the base healing of Pixie Dust is raised from
70 to 75, for the reasons explained at the end of the section on the Bamboo
Cane gag.

C is similar to A except that there is even further incentive for organic
toonup, by raising `propAcc` by 20 across the board when the gags are organic.
The number 20 is chosen in particular for two reasons: one is that it puts
toonup gags at 97.5% accuracy when the track is maxed (97.5% being exactly
halfway between 95% and 100%), and the other reason is that 20 is conveniently
also the number used for a single stun&rsquo;s contribution to gag accuracy.
The 97.5% figure is obtained because `trackExp` for toonup gags is halved
compared to its calculation for all other gag tracks; with maxed toonup, that
is a `trackExp` of 30. So we have an `atkAcc` of
90&nbsp;+&nbsp;30&nbsp;=&nbsp;120 (because `tgtDef` and `bonus` don&rsquo;t
apply to toonup). With the `clamp_acc` function defined in the section on
clamping `atkAcc`, we have:

```python
if atkAcc <= 95:
    return max(atkAcc, 0)
else:
    return min(95 + (atkAcc - 95) / 10, 100)
```

```python
if 120 <= 95:
    return max(120, 0)
else:
    return min(95 + (120 - 95) / 10, 100)
```

```python
return min(95 + (120 - 95) / 10, 100)
```

```python
return min(95 + 25 / 10, 100)
```

```python
return min(95 + 2.5, 100)
```

```python
return 97.5
```

And finally, D is to C as B is to A.

Choosing between these 4 options is a matter of how much organic toonup really
needs to be buffed to be roughly as viable as any of the other 6 possible
organic tracks, as well as a matter of how powerful one is willing to make
toonup. It is clear that out of these 4 options, A is the weakest and D is the
strongest. But hopefully, the case that I have made is convincing, and 75-laff
Pixie Dust really does create better intra-track balance. If this is the case,
then it seems that whether or not 75-laff Pixie Dust is the right choice is a
matter of the sheer power of the toonup gag track overall.

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

|            | Banana Peel      | Rake             | Marbles          | Quicksand        | Trapdoor          | TNT                | Railroad           |
| ---------- | ---------------- | ---------------- | ---------------- | ---------------- | ----------------- | ------------------ | ------------------ |
| TTR        | 12&nbsp;(**13**) | 20&nbsp;(**22**) | 35&nbsp;(**38**) | 50&nbsp;(**55**) | 70&nbsp;(**77**)  | 180&nbsp;(**198**) | 195&nbsp;(**214**) |
| &delta;TTR |                  | +8               | +15              | +15              | +20               | +110               | +15                |
| A          | 12&nbsp;(**13**) | 20&nbsp;(**22**) | 36&nbsp;(**39**) | 60&nbsp;(**66**) | 92&nbsp;(**101**) | 156&nbsp;(**171**) | 188&nbsp;(**206**) |
| &delta;A   |                  | +8               | +16              | +24              | +32               | +64                | +32                |
| B          | 12&nbsp;(**13**) | 20&nbsp;(**22**) | 36&nbsp;(**39**) | 60&nbsp;(**66**) | 92&nbsp;(**101**) | 180&nbsp;(**198**) | 196&nbsp;(**215**) |
| &delta;B   |                  | +8               | +16              | +24              | +32               | +88                | +16                |
| C          | 12&nbsp;(**13**) | 20&nbsp;(**22**) | 35&nbsp;(**38**) | 56&nbsp;(**61**) | 82&nbsp;(**90**)  | 172&nbsp;(**189**) | 198&nbsp;(**217**) |
| &delta;C   |                  | +8               | +15              | +21              | +26               | +90                | +26                |
| D          | 19&nbsp;(**20**) | 28&nbsp;(**30**) | 39&nbsp;(**42**) | 51&nbsp;(**56**) | 82&nbsp;(**90**)  | 172&nbsp;(**189**) | 183&nbsp;(**201**) |
| &delta;D   |                  | +9               | +11              | +12              | +31               | +90                | +11                |

<!-- markdownlint-disable MD033 -->
<!-- Please forgive me for this table... I think this is as good as it gets -->
|     | level 5 cog                                                   | level 6 cog                                                    | level 7 cog                                                                                     | level 8 cog                                                                                                   | level 9 cog                                    | level 10 cog                                                                                                                                                                                  | level 11 cog                                                                                                                                                                   | level 12 cog                                                                                                                                                               |
| --- | ------------------------------------------------------------- | -------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TTR | 1&nbsp;Quicksand                                              | 1&nbsp;Trapdoor                                                | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                        | 1&nbsp;TNT                                                                                                    | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | <ul><li>1&nbsp;Quicksand&nbsp;&amp;&nbsp;1&nbsp;Fruit Pie</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream   | <ul><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul>                                                                     | <ul><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Storm**</li></ul>                                                    | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
| A   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                 | 1&nbsp;Trapdoor                                                                                               | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                               | "                                                                                                             | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream                                                                                                                                                  | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul> | <ul><li>1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;TNT**&nbsp;&amp;&nbsp;1&nbsp;Hose</li><li>1&nbsp;TNT&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> |
| B   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                 | 1&nbsp;Trapdoor                                                                                               | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                               | "                                                                                                             | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream                                                                                                                                                  | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul> | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
| C   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                 | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                                      | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                               | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Glass&nbsp;Of&nbsp;Water</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Hose    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul>                                                     | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Hose                                                                                                                                     |
| D   | <ul><li>1&nbsp;Quicksand</li><li>**1&nbsp;Marbles**</li></ul> | <ul><li>1&nbsp;Trapdoor</li><li>**1&nbsp;Quicksand**</li></ul> | 1&nbsp;Trapdoor                                                                                 | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                                      | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                               | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Glass&nbsp;Of&nbsp;Water</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Hose    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li><ul>                                                      | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
<!-- markdownlint-enable MD033 -->

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
*a*<sub>*n*</sub>&nbsp;=&nbsp;2*a*<sub>*n*&minus;1</sub>&nbsp;&minus;&nbsp;*a*<sub>*n*&minus;2</sub>&nbsp;&minus;&nbsp;1.
This is, in some sense, related to the method used in the sound section, where
the deltas have a slope of +1 (thus creating a [triangular
sequence](https://en.wikipedia.org/wiki/Triangular_number)), rather than the
deltas-of-the-deltas having a slope of &minus;1 (thus creating a [tetrahedral
sequence](https://en.wikipedia.org/wiki/Tetrahedral_number), but negative) as
they do here.

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

#### balancing numerically

Format:

rounds; `propAcc` (**organic `propAcc`**)

|     | $1 Bill             | Small Magnet        | $5 Bill             | Big Magnet          | $10 Bill            | Hypno               | Presentation          |
| --- | ------------------- | ------------------- | ------------------- | ------------------- | ------------------- | ------------------- | --------------------- |
| TTR | 2; 50&nbsp;(**60**) | 2; 50&nbsp;(**60**) | 3; 60&nbsp;(**70**) | 3; 60&nbsp;(**70**) | 4; 70&nbsp;(**80**) | 4; 70&nbsp;(**80**) | 15; 90&nbsp;(**100**) |
| A   | 1; 50&nbsp;(**60**) | 1; 50&nbsp;(**60**) | 1; 60&nbsp;(**70**) | 1; 60&nbsp;(**70**) | 1; 70&nbsp;(**80**) | 1; 70&nbsp;(**80**) | 15; 90&nbsp;(**100**) |
| B   | 1; 50&nbsp;(**70**) | 1; 50&nbsp;(**70**) | 1; 60&nbsp;(**80**) | 1; 60&nbsp;(**80**) | 1; 70&nbsp;(**90**) | 1; 70&nbsp;(**90**) | 15; 90&nbsp;(**110**) |
| C   | 2; 50&nbsp;(**60**) | 1; 50&nbsp;(**60**) | 2; 60&nbsp;(**70**) | 1; 60&nbsp;(**70**) | 2; 70&nbsp;(**80**) | 1; 70&nbsp;(**80**) | 15; 90&nbsp;(**100**) |
| BC  | 2; 50&nbsp;(**70**) | 1; 50&nbsp;(**70**) | 2; 60&nbsp;(**80**) | 1; 60&nbsp;(**80**) | 2; 70&nbsp;(**90**) | 1; 70&nbsp;(**90**) | 15; 90&nbsp;(**110**) |
| D   | 2; 40&nbsp;(**70**) | 1; 40&nbsp;(**70**) | 2; 50&nbsp;(**80**) | 1; 50&nbsp;(**80**) | 2; 60&nbsp;(**90**) | 1; 60&nbsp;(**90**) | 15; 90&nbsp;(**120**) |

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
fix both problems with A.

In case BC was too powerful and/or the problem of organic lure wasn&rsquo;t
solved enough, D is a weakened version of BC that makes organic lure
effectively worth a stun and a half, but lowers inorganic lure `propAcc` by 10
at all levels (except 7). This may seem harsh (and indeed, it is perhaps
unfortunate that making organic lure last for more rounds isn&rsquo;t really
viable and so D relies on making inorganic lure *more fickle*), but all is not
lost for inorganic lure users so long as their friends stun dilligently enough
(one half of an extra stun on average to reach TTR levels of accuracy) to reach
an acceptable rate of success.

In my opinion, as far as balancing &ldquo;numerically&rdquo; goes, either BC or
D is probably the best bet.

#### balancing mechanically

Possibly, in addition to balancing numerically, it may be feasible to alter the
actual mechanics of lure gags somewhat. In particular, the idea is to
permanently mark any cog that is successfully lured, and make it so that cogs
that are so marked cannot be lured. Marked (read:
successfully-lured-at-some-point) cogs cannot be lured in much the same way
that cogs currently in a lured state cannot be lured in TTR.

The intent here is to prevent low lure durations from encouraging a continuous
stream of luring, killing, luring, cogs getting automatically unlured,
*re-luring*, &amp; so on &amp; so forth. Rather than effectively giving players
free (except for taking a hit during the initial unlure) re-lures in many cases
because they would be luring anyways to lure fresh new cogs, this ideally
encourages actual lureless play alongside lure-based play. In addition,
there&rsquo;s the incidental consequence of making single-target lure more
useful since it&rsquo;s generally less likely that there&rsquo;s more than one
cog that can be lured at any given time.

This change could be done in tandem with not just a numeric balance of lure
(like BC), but also possibly a change that causes cogs not to immediately
attack when they are *automatically* unlured. Also, making this mechanical
change could justify using one of the numerical balancing schemes but with an
extra round of duration added to all lure gags.

##### pros

- Actually helps to balance lure-based and lureless play and allow them to
  coexist.
- Allows other changes to make more sense, like: numeric balancing,
  not-quite-as-nerfed lure gag durations, and cogs not immediately attacking
  when automatically unlured.
- Makes single-target lure gags more useful, relatively speaking.

##### cons

- Requires an actual mechanical change, not just a numeric one.
- Not actually useful if you don&rsquo;t care about making lure-based and
  lureless play balanced and coexistent.

### sound

|            | Bikehorn       | Whistle        | Bugle            | Aoogah           | Trunk            | Fog              | Opera            |
| ---------- | -------------- | -------------- | ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
| TTR        | 4&nbsp;(**5**) | 7&nbsp;(**8**) | 11&nbsp;(**12**) | 16&nbsp;(**17**) | 21&nbsp;(**23**) | 50&nbsp;(**55**) | 90&nbsp;(**99**) |
| &delta;TTR |                | +3             | +4               | +5               | +5               | +29              | +40              |
| A          | 4&nbsp;(**5**) | 7&nbsp;(**8**) | 11&nbsp;(**12**) | 16&nbsp;(**17**) | 22&nbsp;(**24**) | 29&nbsp;(**31**) | 40&nbsp;(**44**) |
| &delta;A   |                | +3             | +4               | +5               | +6               | +7               | +11              |
| B          | 4&nbsp;(**5**) | 7&nbsp;(**8**) | 11&nbsp;(**12**) | 16&nbsp;(**17**) | 22&nbsp;(**24**) | 30&nbsp;(**33**) | 50&nbsp;(**55**) |
| &delta;B   |                | +3             | +4               | +5               | +6               | +8               | +20              |

<!-- markdownlint-disable MD033 -->
<!-- Please forgive me for this table... I think this is as good as it gets -->
|     | level 8 cog                                                                                                                                       | level 9 cog                                                                                                      | level 10 cog                                                                                                  | level 11 cog                                                                                                                                                                                             | level 12 cog                                                                                                     |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| TTR | <ul><li>3&nbsp;Trunk&nbsp;&amp;&nbsp;1&nbsp;Aoogah</li><li>2&nbsp;Trunk&nbsp;&amp;&nbsp;**1&nbsp;Aoogah**&nbsp;&amp;&nbsp;1&nbsp;Aoogah</li></ul> | <ul><li>1&nbsp;Fog&nbsp;&amp;&nbsp;2&nbsp;Aoogah&nbsp;&amp;&nbsp;1&nbsp;Bugle</li><li>**4&nbsp;Trunk**</li></ul> | 1&nbsp;Fog&nbsp;&amp;&nbsp;3&nbsp;Trunk                                                                       | 2&nbsp;Fog&nbsp;&amp;&nbsp;2&nbsp;Aoogah                                                                                                                                                                 | 3&nbsp;Fog&nbsp;&amp;&nbsp;1&nbsp;Aoogah                                                                         |
| A   | 2&nbsp;Trunk&nbsp;&amp;&nbsp;2&nbsp;Aoogah                                                                                                        | <ul><li>1&nbsp;Fog&nbsp;&amp;&nbsp;3&nbsp;Trunk</li><li>**2&nbsp;Trunk**&nbsp;&amp;&nbsp;2&nbsp;Trunk</li></ul>  | <ul><li>4&nbsp;Fog</li><li>3&nbsp;Fog&nbsp;&amp;&nbsp;**1&nbsp;Trunk**</li></ul>                              | <ul><li>2&nbsp;Opera&nbsp;&amp;&nbsp;1&nbsp;Fog&nbsp;&amp;&nbsp;1&nbsp;Trunk</li><li>**1&nbsp;Opera**&nbsp;&amp;&nbsp;3&nbsp;Fog</li></ul>                                                               | **2&nbsp;Opera**&nbsp;&amp;&nbsp;2&nbsp;Opera                                                                    |
| B   | "                                                                                                                                                 | "                                                                                                                | <ul><li>3&nbsp;Fog&nbsp;&amp;&nbsp;1&nbsp;Trunk</li><li>**2&nbsp;Fog**&nbsp;&amp;&nbsp;2&nbsp;Trunk</li></ul> | <ul><li>1&nbsp;Opera&nbsp;&amp;&nbsp;2&nbsp;Fog&nbsp;&amp;&nbsp;1&nbsp;Trunk</li><li>**1&nbsp;Opera**&nbsp;&amp;&nbsp;1&nbsp;Fog&nbsp;&amp;&nbsp;**1&nbsp;Trunk**&nbsp;&amp;&nbsp;1&nbsp;Trunk</li></ul> | <ul><li>3&nbsp;Opera&nbsp;&amp;&nbsp;1&nbsp;Aoogah</li><li>2&nbsp;Opera&nbsp;&amp;&nbsp;**2&nbsp;Fog**</li></ul> |
<!-- markdownlint-enable MD033 -->

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

- This is a very niche use-case that doesn&rsquo;t need to be serviced,
  especially considering that even a single stun will negate the usefulness of
  `luredRatio`.
- Having a mechanic like `luredRatio` unnecessarily complicates accuracy
  calculation.

The proposal is to get rid of `luredRatio` wholesale, and collapse `bonus` and
`prevHits` so that they are the same by definition.

#### pros

- Simplifies accuracy calculation.

#### cons

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

#### pros

- Makes accuracy more meaningful in general, because its value changes more
  freely to reflect the strategy being used.
- Particularly, makes stunning more meaningful because it creates a nonzero
  benefit in many more cases.
- Makes the game less reliant on dumb luck by allowing accuracy to be pushed
  beyond the 95% mark (with the right gag picks), even up to 100%.

#### cons

- Complicates accuracy calculation.
- This change would raise the overall power level of toons, since in some cases
  it improves accuracy, and in all other cases it keeps accuracy the same. This
  could be a con.
- Allowing accuracy to possibly reach 100% could be seen as overly rigid or
  deterministic(&#x203d;)

## facilities

This section deals with &ldquo;facilities&rdquo;, which is a term here
construed broadly to refer to factories (and the corresponding factory-like
facilities in the other three cog HQs) and bosses (all four in all four cog
HQs). Note that this does not, however, include cog buildings.

### barriers to entry

In TTR, the barriers to entry for the various facilities are as follows:

| facility       | requirement(s)                                           |
| -------------- | -------------------------------------------------------- |
| factory, front |                                                          |
| factory, side  | 31 laff                                                  |
| coin mint      |                                                          |
| dollar mint    | 66 laff                                                  |
| bullion mint   | 71 laff                                                  |
| DA office A    |                                                          |
| DA office B    | 81 laff                                                  |
| DA office C    | 86 laff                                                  |
| DA office D    | 96 laff                                                  |
| front 3        |                                                          |
| middle 6       | 95 laff                                                  |
| back 9         | 100 laff                                                 |
| VP             | 10 factories completed                                   |
| CFO            | cashbot suit tasks (76 laff and access to 6 gag tracks)  |
| CJ             | lawbot suit tasks (100 laff and access to 6 gag tracks)  |
| CEO            | bossbot suit tasks (100 laff and access to 6 gag tracks) |

It is nice that some facilities that are considered to be designed for toons
that are *at least* middling in terms of power are nevertheless available to
anyone: coin mints, DA offices A, front 3s, and VPs. However, the requirements
for facilities that have them range from &ldquo;unfortunate, at least for
certain styles of play&rdquo; to &ldquo;completely unnecessary&rdquo;. There
are basically three groups of requirements that we want to talk about here, and
so we will tackle them one-by-one in descending order of silliness.

#### factories: the side entrance

Really, no amount of argumentation *should* be required to establish that the
side entrance of the sellbot factory should have no barriers to entry. The
front entrance already has no such barriers, and they are both just different
entrances to the same facility anyways. Presumably, the reasoning for giving
the side entrance a laff limit is that if you go left after completing the
first cog battle, you have to go through *stompers* and then complete another
cog battle; if you keep going, you have to do the *most dangerous walk* across
the catwalk area of the factory before finally getting to the part of the
factory that every factory run has to do anyways. However, there are a few
problems with this reasoning for instituting a laff limit:

- Most front entrance runs are long runs anyways, so they do all of this stuff
  as well (but with extra cog fights and catwalking).
- Just because you enter via the side entrance does not mean that you *have* to
  go left after the first cog fight; you can just go straight.
- Obstacles like stompers and goons can indeed shave off significant amounts of
  laff if you aren&rsquo;t at least somewhat careful, but typically the real
  danger is in the last 4 cog fights (a.k.a. the only part of the factory that
  literally every factory run must complete anyways).

It&rsquo;s clear that the way to go is lowering the laff limit on the factory
side entrance to 1, to match the front entrance.

#### factory-like facilities

<!-- ... -->

### gag retention

<!-- ... -->

## cogs

<!-- ... -->

## toontasks

<!-- ... -->

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

See the section on balancing lure mechanically for a possible solution.
