# garbage/useless tt ideas

<!-- TOC depthFrom:2 -->

- [general attitude/philosophy (prelude)](#general-attitudephilosophy-prelude)
    - [what about other (non-TTR) servers, though?](#what-about-other-non-ttr-servers-though)
    - [contributing](#contributing)
    - [legal](#legal)
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
        - [bosses (excluding VP)](#bosses-excluding-vp)
- [cogs and laff](#cogs-and-laff)
    - [limiting laff](#limiting-laff)
        - [laff capping](#laff-capping)
            - [pros](#pros-3)
            - [cons](#cons-3)
        - [nerfing toontasks (and company)](#nerfing-toontasks-and-company)
            - [pros (of lowering max-laff awards for non-task activities)](#pros-of-lowering-max-laff-awards-for-non-task-activities)
            - [cons (of lowering max-laff awards for non-task activities)](#cons-of-lowering-max-laff-awards-for-non-task-activities)
            - [pros (of capping max-laff gain attainable from non-task activities)](#pros-of-capping-max-laff-gain-attainable-from-non-task-activities)
            - [cons (of capping max-laff gain attainable from non-task activities)](#cons-of-capping-max-laff-gain-attainable-from-non-task-activities)
    - [tweaking cog attacks](#tweaking-cog-attacks)
        - [single-target vs. multi-target attacks](#single-target-vs-multi-target-attacks)
            - [nerfing multi-target attacks directly](#nerfing-multi-target-attacks-directly)
                - [pros](#pros-4)
                - [cons](#cons-4)
            - [buffing single-target attacks directly](#buffing-single-target-attacks-directly)
                - [pros](#pros-5)
                - [cons](#cons-5)
            - [attack limiting](#attack-limiting)
                - [pros](#pros-6)
                - [cons](#cons-6)
            - [varying target numbers](#varying-target-numbers)
                - [pros](#pros-7)
                - [cons](#cons-7)
- [toontasks](#toontasks)
- [gag tracks](#gag-tracks)
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
rather than change the game unnecessarily or add to it. This document seeks not
to imagine a new game, but rather to scratch the surface of an already-existing
game (viz. Toontown) and reveal the superior game that was within it all
along.<sup>\[1\]</sup>

Some of the changes proposed here are meant to be combined with other such
changes, but some may be designed *without* other changes in mind, for the sake
of independence and flexibility. This means &mdash; among other things &mdash;
that this document is *not* a blueprint for a particular, single, version of
Toontown with some choice combination of all of the proposed changes discussed
within this document. Rather, when concretely forming an actual version of
Toontown, careful judgement and deliberation should be applied to the concerns,
reasoning, and proposals contained within this document.

While the changes made here are obviously, first and foremost, changes made to
balance the game and make it more fun, there are also some aesthetic
considerations to fill in the gaps. Mostly, this comes in the form of what
numbers are chosen in cases where numeric values are being balanced. The
tendency is to favor numbers that are more &ldquo;round&rdquo; (read:
[regular](https://en.wikipedia.org/wiki/Regular_number), or its synonym,
5-[smooth](https://en.wikipedia.org/wiki/Smooth_number)), and to favor
[sequences](https://en.wikipedia.org/wiki/Sequence) and mathematical
[functions][function] that are more
[&ldquo;beautiful&rdquo;](https://en.wikipedia.org/wiki/Mathematical_beauty).
In this document, heeding these aesthetic concerns is referred to as
&ldquo;rationalization&rdquo; (both in the mathematical sense, from
&ldquo;ratio&rdquo;, and the usual sense of &ldquo;to give a rationale&rdquo;).
Again, these concerns are always strictly secondary to the more important
concerns of game balance &amp; fun.

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

### contributing

Suggestions/corrections/additions/typo-fixes/&amp;c. are *encouraged*. You can
file an issue and/or submit a pull request and/or [contact me
directly](https://zz.nfshost.com/contact.html).

By contributing, you agree to license your contributions under the same license
as this work (see the &ldquo;legal&rdquo; section).

### legal

This work is licensed to you (or to anyone else) under the terms of the
[Creative Commons Attribution-ShareAlike 4.0
International](https://creativecommons.org/licenses/by-sa/4.0/) license (or any
later version of the same license, at your option).

[![CC BY-SA 4.0+](https://i.creativecommons.org/l/by-sa/4.0/88x31.png
"CC BY-SA 4.0+")](https://creativecommons.org/licenses/by-sa/4.0/)

---

<details>
<summary>
footnotes for &ldquo;general attitude/philosophy (prelude)&rdquo;
</summary>

1. See my open letter, [&ldquo;On sellbot field offices (SBFOs), especially
   concerning the problem of &lsquo;difficulty&rsquo; in
   Toontown&rdquo;][on-sbfos] if you are interested in more abstract
   considerations of the kind mentioned in this paragraph.

</details>

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
simply because a toon with 1 laff fewer than their max-laff is not fully
healed, and a toon with laff equal to their max-laff is. But the difference
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
|     | level 5 cog                                                   | level 6 cog                                                    | level 7 cog                                                                                          | level 8 cog                                                                                                   | level 9 cog                                    | level 10 cog                                                                                                                                                                                  | level 11 cog                                                                                                                                                                   | level 12 cog                                                                                                                                                               |
| --- | ------------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TTR | 1&nbsp;Quicksand                                              | 1&nbsp;Trapdoor                                                | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                             | 1&nbsp;TNT                                                                                                    | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | <ul><li>1&nbsp;Quicksand&nbsp;&amp;&nbsp;1&nbsp;Fruit&nbsp;Pie</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream   | <ul><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul>                                                                     | <ul><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Storm**</li></ul>                                                    | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
| A   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                      | 1&nbsp;Trapdoor                                                                                               | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                                    | "                                                                                                             | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream                                                                                                                                                  | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul> | <ul><li>1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;TNT**&nbsp;&amp;&nbsp;1&nbsp;Hose</li><li>1&nbsp;TNT&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> |
| B   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                      | 1&nbsp;Trapdoor                                                                                               | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                                    | "                                                                                                             | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Seltzer | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Cream                                                                                                                                                  | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul> | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
| C   | 1&nbsp;Quicksand                                              | 1&nbsp;Quicksand                                               | 1&nbsp;Trapdoor                                                                                      | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                                      | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                                    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Glass&nbsp;Of&nbsp;Water</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Hose    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li></ul>                                                     | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Hose                                                                                                                                     |
| D   | <ul><li>1&nbsp;Quicksand</li><li>**1&nbsp;Marbles**</li></ul> | <ul><li>1&nbsp;Trapdoor</li><li>**1&nbsp;Quicksand**</li></ul> | 1&nbsp;Trapdoor                                                                                      | <ul><li>1&nbsp;TNT</li><li>**1&nbsp;Trapdoor**</li></ul>                                                      | 1&nbsp;TNT                                     | 1&nbsp;TNT                                                                                                                                                                                    | 1&nbsp;TNT                                                                                                                                                                     | **1&nbsp;Railroad**                                                                                                                                                        |
|     | "                                                             | "                                                              | "                                                                                                    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Glass&nbsp;Of&nbsp;Water</li><li>**1&nbsp;Trapdoor**</li></ul> | 1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Hose    | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Safe</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;1&nbsp;Big&nbsp;Weight</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Cream**</li></ul> | <ul><li>1&nbsp;Trapdoor&nbsp;&amp;&nbsp;1&nbsp;Storm</li><li>**1&nbsp;Trapdoor**&nbsp;&amp;&nbsp;**1&nbsp;Safe**</li><ul>                                                      | 1&nbsp;TNT&nbsp;&amp;&nbsp;1&nbsp;Seltzer                                                                                                                                  |
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

Below are (Python) functions `ttr_clamp_acc` and `clamp_acc`<sup>\[1\]</sup>,
which correspond to TTR&rsquo;s method of clamping `atkAcc` after it is
calculated as the sum of the four aforementioned numbers, and the proposed
method of doing the same thing, respectively.

```python
def ttr_clamp_acc(atkAcc):
    return max(min(atkAcc, 95), 0)

def clamp_acc(atkAcc):
    if atkAcc <= 95:
        return max(atkAcc, 0)
    else:
        return min(95 + (atkAcc - 95) / 10, 100)
```

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

---

<details>
<!-- markdownlint-disable MD033 -->
<summary>footnotes for &ldquo;<code>atkAcc</code> clamping&rdquo;</summary>
<!-- markdownlint-enable MD033 -->

1. Python doesn&rsquo;t have types, but it does have data types, and these two
   functions have different return (data) types, namely
   `ttr_clamp_acc: int -> int` and `clamp_acc: int -> (int | float)`. But
   really, it doesn&rsquo;t matter&hellip; just be sure not to somehow trip on
   that.

</details>

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

Some other factory-like facilities besides factories themselves have laff
requirements (viz. dollar &amp; bullion mints, DA offices B, C, &amp; D, middle
6s, and back 9s). Is this warranted? At first it seems like it might indeed be
warranted, considering that all of these factory-like facilities are
significantly more difficult than factories. In addition, it seems unlikely
that a toon that doesn&rsquo;t meet the laff requirements for one of these
facilities will actually have a reason to do the facility. For the most part,
these facilities are frequented for the purpose of getting ready for cog suit
promotions; but anyone who is doing this must have the corresponding suit and
thus enough laff to do the corresponding facilities.

However, I want to argue that these laff limitations should be removed entirely
(or weakened, at the very least), for a number of reasons:

- Shortened versions of all of these factory-like facilities are available to
  anyone, with no limitations. Coin mints, DA offices A, and front 3s all lack
  requirements, but they present identical challenges to their laff-gated
  counterparts! Therefore, for the sake of consistency, the requirements should
  be lifted (or at least, can reasonably be lifted). It could be argued that
  said laff-gated facilities do in fact present more challenge (enough to
  warrant locking them off to those with insufficient laff) because of their
  length. This is a kind of difficulty by attrition, where the danger is that
  you run out of (sufficiently powerful) gags too quickly to complete the whole
  facility. While this is indeed more of a problem for lower-laff toons
  (because they generally have fewer gag tracks and smaller gag pouches), in
  general this is not a good enough excuse. Imposing laff requirements means
  disallowing a party that has just *one* member who does not meet the
  requirement, so even a party with (to give the most extreme example) 3 maxed
  toons and 1 toon who just barely does not meet the requirement is barred,
  despite easily being able to handle the attrition. In addition, the
  facilities themselves provide ways of restocking gags, and players can even
  restock their own gags (and laff) through the use of SOS cards and unites.
- It is common for toontasks to require things that can be easily (sometimes,
  *most* easily) be found within these factory-like facilities. Of course, a
  toon who doesn&rsquo;t meet the requirements can instead do the corresponding
  facilities that don&rsquo;t have such requirements; however, because these
  facilities are meant for teamwork (generally being done in parties of 4
  toons), being more flexible in which ones you can do is a big help. Being
  *able* to do a DA office D is a blessing when you need a DA office, and there
  are already 3 people waiting for a 4<sup>th</sup> toon to join them so that
  they can do a DA office D.
- Completely preventing players from being able to do something just because
  you have a vague idea that they probably aren&rsquo;t capable of it is
  often poor design. It is needlessly frustrating for players who intentionally
  play in an unexpected way, or intentionally seek extra challenge, or just
  feel a bit more &ldquo;railroaded&rdquo; due to the game deciding for them
  that they &ldquo;aren&rsquo;t ready yet&rdquo;. The possible punishment in
  Toontown is never very great (going sad is not exactly the end of the world),
  so allowing players to decide for themselves should be unproblematic.
- Removing these laff requirements is even more important when you consider
  implementing changes to the max-laff mechanic in general. Particularly, laff
  caps that allow players to limit how high their toon&rsquo;s laff will ever
  be able to reach, and changes to max-laff acquisition (viz. toontasks &amp;
  minigames that award max-laff), are both the kinds of changes that demand at
  least the reconsideration of laff requirements. In many of these cases,
  max-laff levels are being lowered overall, and so laff requirements must be
  removed (or at least lowered) in tandem.
- If changes to requirements for doing bosses (see the next section) are
  considered, then removing these laff requirements for factory-like facilities
  may be necessary anyways.

#### bosses (excluding VP)

After considering the requirements for entry into the side entrance of
factories, and for entry into other factory-like facilities, we are now brought
to the same issue w.r.t. boss fights (excluding VP, because it *effectively*
has no requirements due to only requiring 10 factories). It may seem
particularly obvious that there are no significant changes to be made to the
requirements for entry into non-VP bosses, considering that all three require
(and only require) some part of the main taskline to be completed. However,
there are, <i>per se</i>, ways of loosening these requirements without making
changes to the main taskline &mdash; and there are reasons to do so, as well.

What would be the motivation for loosening the requirements for entry into
non-VP bosses? There are basically two motivations: first &amp; foremost is the
desire to open up non-VP bosses to challenge runs. Basically, we are talking
about uber toons here. In TTR, ubers are limited to maxing out their sellbot
suit by defeating the VP many times (and doing many factories). Allowing them
other activities (viz. 3 other possible bosses to run) to do would be a huge
gameplay improvement for uber/challenge-run styles of play. The second (lesser)
motivation is that as TTR&rsquo;s &ldquo;Crash Sellbot HQ&rdquo; and
&ldquo;Crash Cashbot HQ&rdquo; events have shown, opening up bosses to more
toons is a good bit of fun. Of course, this is *not* to actually propose what
these two events do in particular, which involves nerfing said bosses to make
them more accessible to toons of all power levels.

There are two (*not* mutually exclusive) ways that the loosening of non-VP boss
entry requirements can be achieved without any changes to the main taskline:

1. Allow a similar mechanic to &ldquo;Crash Sellbot/Cashbot HQ&rdquo;, with
   so-called &ldquo;rental suits&rdquo; that allow entry into bosses without
   having the proper suit. This would be limited to just CFO, CJ, and CEO.
   Rental suits are permanently level 1; that is, they cannot level up and are
   always &ldquo;ready for promotion&rdquo;. The use of rental suits should
   probably have requirements; requiring the completion of some factory-like
   facilities (e.g. mirroring Sellbot HQ by requiring the completion of at
   least 10 factory-like facilities within the corresponding cog HQ) and/or
   requiring at least 1 maxed gag track should suffice (I would favor having
   both requirements).
2. Make the tasklines that grant cog HQ suits available to any toon that meets
   one or both of the following requirements: **(2a)** the toon has completed
   the normal pre-requisite tasks (as in TTR), **(2b)** the toon has a level 50
   Mr. Hollywood suit.

While these two options are not mutually exclusive, it probably suffices to
just pick one. The second option seems more appealing, because it offers more
of a sense of progression. The sense of progression is both because you have to
progress all the way through Sellbot HQ before getting to the other HQs, and
because it allows leveling up the suits that you get for the other HQs, unlike
rental suits. However, this is a higher barrier to entry than the first option
(which may be a bad thing), and means more laff for ubers due to the other 3
cog HQ suits also granting 5 laff each (this is not so much a problem with laff
capping). The second option also probably means that factory-like facilities
will be more popular (even if defeating some of them is required to get a
rental suit) because bossing on low-laff toons will still mean having to earn
promotions.

## cogs and laff

This section discusses cog behavior (read: attacks) and maximum laff for toons.
These topics are inherently related for the obvious reason that higher maximum
laff is primarily useful for being able to handle more punishment from cogs
before going sad. However, make no mistake: these topics are also intimately
tied to the ability of toons to defeat &amp; otherwise control cogs, that is,
gag balance. These topics are difficult because they are so entangled in the
overall power level of toons in the game, including toons doing challenge runs
like e.g. uber toons and/or semi toons.

That being said, even if these topics are difficult to treat due to being
entangled in&hellip; well, everything else, there is one thing that we can
clearly state: toons have an excess of laff points in vanilla TTO/TTR. In many
ways this is just saying that the balance between toons and cogs is skewed
heavily in favor of toons, hence the existence of challenge run styles of play.
In addition, it is also clear that multi-target attacks that cogs can perform
are disproportionately powerful when compared to their single-target
counterparts. This makes cogs that have no multi-target attacks (e.g. any
bossbots of higher rank than Yesman) disproportionately weak, and also makes
cogs that do have multi-target attacks fickle in terms of damage output because
it is a matter of chance whether or not they choose their attacks to be
multi-target ones.

The concern about multi-target cog attacks is not necessarily a sign of an
actual problem; it might be perfectly okay for some cogs to be limited to
single-target attacks, and for it to be a rather significant matter of chance
whether or not certain cogs choose to use their multi-target attack(s). But it
does give something to consider when trying to balance cogs&rsquo; attacks.

### limiting laff

There are three main ways of limiting laff that we want to consider here: laff
capping, nerfing toontasks (and other max-laff-awarding activities), and
lowering starting laff.

#### laff capping

Laff capping means allowing players to choose a laff limit for their toon at
the point of toon creation. A laff-capped toon starts with the same max-laff as
a normal toon (15, unless modifications are made), but any max-laff increases
that they receive can raise their max-laff to, *at most*, their laff cap. This
is a pretty mechanically straightforward change and has already been
implemented at least once before. Laff capping is an appealing proposition, but
its usefulness is essentially limited to the creation of uber toons; it does
only a little to help balance the game generally, because it is entirely
voluntary.

##### pros

- It&rsquo;s voluntary, which has the benefit of encouraging a wider range of
  playstyles and allowing players to choose for themselves.
- It&rsquo;s flexible enough to limit max-laff to any arbitrary degree.

##### cons

- It&rsquo;s voluntary, which has the drawback of doing only a little to help
  balance the game generally, and
- Being voluntary also tends to cause greater power disparities between toons
  that are trying to cooperate.

#### nerfing toontasks (and company)

It is possible to limit maximum laff in general (and thus take a step towards
balancing the game more generally) by nerfing the max-laff rewards given by
toontasks and other relevant activites. The following list chronicles the
progression of the mainline toontasks that award max-laff, including the
max-laff that a toon has *after* completing each particular
neighborhood/playground (assuming all max-laff boosts are from toontasks, and
not other sources like e.g. fishing):

<details>
<summary>max-laff-awarding toontasks</summary>

- Toontown Central (25 laff)
    - +1 laff (Professor Pete)
    - +2 laff (Honey Haha)
    - +2 laff (Professor Wiggle)
    - +3 laff (Sticky Lou)
    - +1 laff (generic)
    - +1 laff (generic)
- Donald&rsquo;s Dock (34 laff)
    - +2 laff (Billy Budd)
    - +1 laff (generic)
    - +1 laff (generic)
    - +2 laff (generic)
    - +3 laff (generic)
- Daisy Gardens (43 laff)
    - +1 laff (Sofie Squirt/Artie/Inkeeper Janet/Barber Bjorn)
    - +1 laff (Sofie Squirt/Artie/Inkeeper Janet/Barber Bjorn)
    - +2 laff (Postman Felipe)
    - +2 laff (sprocket recovery/generic)
    - +3 laff (Uncle Mud/Uncle Spud/Aunt Hill)
- Minnie&rsquo;s Melodyland (52 laff)
    - +1 laff (generic)
    - +1 laff (generic)
    - +2 laff (generic)
    - +2 laff (generic)
    - +3 laff (generic)
- The Brrrgh (61 laff)
    - +1 laff (Chicken Boy/Wynne Chill/Eddie the Yeti)
    - +1 laff (Chicken Boy/Wynne Chill/Eddie the Yeti)
    - +2 laff (Sweaty Pete)
    - +3 laff (Lounge Lassard)
    - +2 laff (generic)
- Donald&rsquo;s Dreamland I (71 laff)
    - +1 laff (Powers Erge)
    - +2 laff (Lawful Linda)
    - +3 laff (Rocco)
    - +4 laff (Zari)
- Donald&rsquo;s Dreamland II (81 laff)
    - +1 laff (generic)
    - +2 laff (generic)
    - +3 laff (generic)
    - +4 laff (generic)
- Donald&rsquo;s Dreamland III (91 laff)
    - +1 laff (generic)
    - +2 laff (generic)
    - +3 laff (generic)
    - +4 laff (generic)
- Donald&rsquo;s Dreamland IV (100 laff)
    - +1 laff (generic)
    - +2 laff (generic)
    - +3 laff (generic)
    - +3 laff (generic)

</details>

An easy way to lower the overall amount of max-laff awarded by tasks is by
lowering only the rewards of tasks that award &ge;2 max-laff. This way, the
entire structure of the taskline is totally intact. Here is what this approach
looks like if taken to the extreme (all max-laff-awarding tasks giving exactly
+1 max-laff):

<details>
<summary>all max-laff-awarding toontasks awarding +1</summary>

- Toontown Central (21 laff)
    - +1 laff (Professor Pete)
    - +1 laff (Honey Haha)
    - +1 laff (Professor Wiggle)
    - +1 laff (Sticky Lou)
    - +1 laff (generic)
    - +1 laff (generic)
- Donald&rsquo;s Dock (26 laff)
    - +1 laff (Billy Budd)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
- Daisy Gardens (31 laff)
    - +1 laff (Sofie Squirt/Artie/Inkeeper Janet/Barber Bjorn)
    - +1 laff (Sofie Squirt/Artie/Inkeeper Janet/Barber Bjorn)
    - +1 laff (Postman Felipe)
    - +1 laff (sprocket recovery/generic)
    - +1 laff (Uncle Mud/Uncle Spud/Aunt Hill)
- Minnie&rsquo;s Melodyland (36 laff)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
- The Brrrgh (41 laff)
    - +1 laff (Chicken Boy/Wynne Chill/Eddie the Yeti)
    - +1 laff (Chicken Boy/Wynne Chill/Eddie the Yeti)
    - +1 laff (Sweaty Pete)
    - +1 laff (Lounge Lassard)
    - +1 laff (generic)
- Donald&rsquo;s Dreamland I (45 laff)
    - +1 laff (Powers Erge)
    - +1 laff (Lawful Linda)
    - +1 laff (Rocco)
    - +1 laff (Zari)
- Donald&rsquo;s Dreamland II (49 laff)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
- Donald&rsquo;s Dreamland III (53 laff)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
- Donald&rsquo;s Dreamland IV (57 laff)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)
    - +1 laff (generic)

</details>

In combination with other propositions, e.g. the nerfing of gag tracks like
sound &amp; lure, the buffing of cog attacks, &amp;c., this particular approach
is probably too steep of a nerf; starting The Brrrgh with 36 laff is tough.
Also, without changes to other sources of max-laff increases, the amount of
max-laff available from toontasks alone is worryingly similar to the amount of
laff available from other sources: 42 from tasks, and 37 from elsewhere (plus
15 starting laff, for an absolute maximum laff of 94).

The good news is that exactly how much laff you distribute via toontasks, and
exactly *when* in the taskline you distribute it, is very tweakable: setting
all max-laff-awarding tasks to award +1 laff works as one extreme, and some
middle ground between that and something much more high-powered like vanilla
TTO/TTR can easily be achieved by tweaking the rewards within any of the
various neighborhoods/playgrounds.

Ultimately, to what degree it makes sense to cripple (or perhaps boost?)
max-laff accumulation is *wildly dependent* on what other changes are made (or
not made) to the game.

The quantity of max-laff increases available from non-task sources can be
tweaked to better match the max-laff increases available from tasks, which
brings us to the topic of how to nerf these non-task sources if necessary.

When it comes to non-task sources of max-laff increases, all of them are given
+1 at a time, so the technique used for toontasks doesn&rsquo;t apply. Instead,
we have two (not mutually exclusive) options: some (or all) of the increases
granted by a given activity have to be removed outright, and/or an overall cap
can be placed on the total number of max-laff points that can be obtained from
non-task sources. If we break down the non-task sources of max-laff increases,
we see that most of them are from leveling up cog HQ suits:

- +7 (fishing)
- +5 (Sellbot HQ)
- +5 (Cashbot HQ)
- +5 (Lawbot HQ)
- +5 (Bossbot HQ)
- +4 (gardening)
- +3 (golfing)
- +3 (racing)

Besides the obvious options that we have for each non-task source of max-laff
increases &mdash; viz. leaving it alone, or removing all of its max-laff
increases &mdash; we&rsquo;ll quickly consider ways of partly removing the
max-laff increases from each source listed above. Note that one invariant that
we maintain is always giving one of the max-laff increases as an award for
totally maxing out the activity.

- Fishing gives an odd number of max-laff increases (7), so it may make sense
  to only award a max-laff increase every *other* time, starting with the
  first. This would mean getting an increase for catching a total of 10, 30,
  50, &amp; 70 species, for a total of +4 max-laff from maxing fishing. Another
  possibility is just removing one or more of the earliest max-laff rewards,
  e.g. removing two of them to end up with awards at 30, 40, 50, 60, &amp; 70
  species caught, for a total of +5 max-laff from maxing fishing. Yet another
  possibility comes from 70 being divisible by 14: awarding a max-laff increase
  at each multiple of 14 species caught. Awards at 14, 28, 42, 56, &amp; 70
  would place the total max-laff awarded for maxing fishing at +5.
- Lowering the number of max-laff increases awarded by cog HQs is more
  difficult, mostly because it is engrained in the way that cog suit promotions
  work: at the highest-rank suit (e.g. Mr. Hollywood for Sellbot HQ), the
  number of merits (using the term &ldquo;merit&rdquo; generically) needed to
  achieve each successive promotion follows a vaguely [sawtooth][sawtooth]
  pattern, with an increase in max-laff accompanying each fall. The purpose of
  having this kind of payoff is obvious, and it only makes sense to replace any
  removed max-laff increase with some other suitable reward. Short of changing
  the merits-for-promotion progression itself, removing some max-laff increases
  from cog HQs will require more creativity than is warranted in this document;
  you might try, for example, awarding things like a single extra tree spot at
  the toon&rsquo;s estate.
- There are basically 4 viable options for gardening: max-laff increases at 20,
  30, &amp; 40 species, or at 20 &amp; 40 species, or at 30 &amp; 40 species,
  or only at 40 species.
- Golfing and racing are similar to gardening, but with just 3 trophies to
  choose from. Generally, you can grant max-laff increases for the
  1<sup>st</sup> &amp; 3<sup>rd</sup>, or the 2<sup>nd</sup> &amp;
  3<sup>rd</sup>, or the 3<sup>rd</sup> only.

Note that in the case that you use one or more of these methods, it may make
sense to replace the now-missing max-laff increases with something else to fill
in the missing space; even just a cosmetic reward.

Capping the amount of max-laff that can be obtained from non-task sources is
fairly straightforward, except that you have to choose a particular number to
cap at. The considerations for choosing such a number (if any) must heed the
following considerations, in descending order of importance:

- Balance against the rest of the game, including the amount of max-laff
  available from toontasks, and general toon-cog balancing considerations.
- Not capping so low as to make too many sources of laff useless, but also not
  so high as to make the viability of toons in combat very reliant on doing
  unrelated minigames like racing.
- Aesthetic concerns about the
  [regularity](https://en.wikipedia.org/wiki/Regular_number) of numbers used
  (including the capping number itself, as well as the highest max-laff
  achievable in the game).

Here&rsquo;s a summary of the pros &amp; cons of stripping (some) max-laff
awards from non-task sources, as well as the pros &amp; cons of putting an
overall cap on the number of max-laff available from such sources (note that
these two things are *not* mutually exclusive):

##### pros (of lowering max-laff awards for non-task activities)

- On its own, this technique lowers the max-laff-granting power of non-task
  activities while keeping some incentive for each toon to do each such
  activity.
- On its own, this technique is not very invasive; it doesn&rsquo;t require a
  new mechanic to be added. At its core, all that really needs to be done is
  changing some max-laff awards from +1 to +0, or something very similar.
- Using this technique can allow the balancing of these various activities. For
  example, in vanilla TTO/TTR, fishing alone grants more max-laff than racing
  &amp; golfing combined.

##### cons (of lowering max-laff awards for non-task activities)

- In some cases, now-missing max-laff rewards will create a void that will
  either have to be left open, or filled with some other sort of reward.
- In some cases, this may skew non-task activities towards power players that
  are willing to invest the time into maxing these activities, because only
  investing *some* time into a given activity won&rsquo;t give much (if any)
  up-front rewards.

##### pros (of capping max-laff gain attainable from non-task activities)

- Skews away from excessively rewarding power players by allowing players to
  more easily get to the laff cap without having to completely max out every
  possible source of max-laff. It should be noted that this is much more
  important than in TTR, because in TTR getting from 100 max-laff (no non-task
  activities completed) to 137 max-laff (all non-task activities completed;
  maximum possible laff) is not much of an advantage gameplay-wise. 100 laff is
  more than enough to do even the most challenging things in TTR.
- Allows putting a hard limit on attainable max-laff without tampering with the
  various ways of getting it.

##### cons (of capping max-laff gain attainable from non-task activities)

- There is some pressure to add extra rewards (cosmetic or otherwise) to fill
  in the &ldquo;gaps&rdquo; that are here created by refusing to award max-laff
  to players that have already hit the cap, even though they continue to
  achieve further progress in non-task activities. This pressure is eased by
  &ldquo;completionist&rdquo; urges, which urge players to complete things even
  if there is no reward <i>per se</i> for doing so. The pressure is eased as
  well by the activities themselves being high quality, and thus motivating
  players to do the activities for the sake of the activities themselves being
  enjoyable.
- Related to the previous point: placing the cap too low could make excessively
  many sources of laff useless (or at least, less useful). A player that has
  already reached max-laff now has less incentive to do non-task activities
  that they haven&rsquo;t maxed out; this is trivially not the case if the cap
  is removed, since anyone whose laff is maxed out has already maxed out all
  activities anyways.
- It&rsquo;s somewhat invasive; a new mechanic needs to be introduced that caps
  the overall max-laff gain attainable from non-task sources.

### tweaking cog attacks

When it comes to tweaking cogs&rsquo; attacks, there are two main concerns that
we want to address here: disparity between single-target and multi-target
attacks, and the overall power level of cogs.

#### single-target vs. multi-target attacks

It&rsquo;s well understood in TTR that multi-target cog attacks are more
formidable than their single-target counterparts. The reason is that
multi-target attacks tend to do the same per-toon damage as single-target ones;
furthermore, multi-target attacks are never &ldquo;duds&rdquo;. By
&ldquo;dud&rdquo;, we mean attacks like the Glad Hander&rsquo;s Fountain Pen or
the Yesman&rsquo;s Razzle Dazzle. With a multi-target attack&rsquo;s damage
effectively being multiplied by the number of toons that it hits, the total
damage output is much more impressive.

Of course, this impressive damage being spread evenly between two or more toons
*does* dilute its impact to some extent. But the amount of resources (in terms
of both gag expenditure, and the number of gags in each round that have to be
dedicated just to toonup rather than other gags) required to patch up the
damage is definitely much higher. This imbalance may be acceptable to some
extent; it all depends on how neck-breakingly sharp you want the variation to
be between cog attacks, including the variation between the attacks of a given
cog species, as well as the variation between the arsenal of different cog
species. It also makes sense to want *some* single-target attacks to really
&ldquo;sting&rdquo;; it really stings when a level 11 Mingler uses Paradigm
Shift and (assuming no misses; the accuracy is 90%) dishes out a whopping
24&nbsp;&times;&nbsp;4&nbsp;=&nbsp;96 damage! There are a number of approaches
that can be taken here. So here are a few of them (note that none of them are
mutually exclusive with any of the others), each accompanied by at least some
discussion/deliberation:

##### nerfing multi-target attacks directly

The most obvious choice is to directly nerf multi-target attacks by tweaking
the numbers. This further splits our options into nerfing damage and/or nerfing
accuracy.

Nerfing accuracy might *sound* like a somewhat poor idea given that it
introduces more of the &ldquo;dumb luck&rdquo; and &ldquo;fickleness&rdquo;
that is lamented elsewhere in this document. However, it actually turns out to
not be that bad of an idea, for at least two reasons. First is that, unlike
making toons&rsquo; gags more fickle, making cog attacks more fickle
doesn&rsquo;t have the same negative impact on gameplay. When adding dumb luck
to player-controlled elements of gameplay, it can quickly become frustrating,
because players feel (often justifiably) that their planning &amp; actions have
been in vain just because of some dumb luck that seems to have no purpose, no
way of being predicted, and no way of being controlled. But when adding luck
reliance to NPCs (adversaries, in this case), the effect is much more mild. The
player already sees the NPCs as being somewhat opaque, so leaving their
decisions &mdash; and the effects that they have on the game world &mdash;
totally or partly up to chance doesn&rsquo;t necessarily make the opacity worse
or make anything seem fickle. Indeed, the methodic use of chance is often to
great effect whenever it makes NPCs seem more organic (although that particular
use is not directly relevant here).

The other reason that adding dumb luck to cog attacks is less of a problem here
is that we are talking specifically about multi-target attacks, which perform
[independent](https://en.wikipedia.org/wiki/Statistical_independence)
[rolls](https://en.wikipedia.org/wiki/Dice) for each toon in the battle. This
causes the number of toons that are hit (or, conversely, the number of toons
that are missed) to be selected from a [binomial
distribution](https://en.wikipedia.org/wiki/Binomial_distribution)
*B*(*n*,&nbsp;*p*), where *n* is the number of toons in the battle and *p* is
the probability of the attack hitting a given toon. Because of the [central
limit theorem](https://en.wikipedia.org/wiki/Central_limit_theorem), this looks
very similar to a normal distribution; particularly, with the binomial
distribution it looks quite normal even with an *n* as low as
*n*&nbsp;=&nbsp;4. The [variance](https://en.wikipedia.org/wiki/Variance) of
said distribution is *np*(1&nbsp;&minus;&nbsp;*p*), so with 4 toons in the case
of maximum variance<sup>\[1\]</sup>:

*np*(1&nbsp;&minus;&nbsp;*p*)<br />
=&nbsp;4&nbsp;&times;&nbsp;0.5(1&nbsp;&minus;&nbsp;0.5)<br />
=&nbsp;2&nbsp;&times;&nbsp;0.5<br />
=&nbsp;1

So the expected number of toons struck is obviously 2, but with a variance (and
therefore also [standard
deviation](https://en.wikipedia.org/wiki/Standard_deviation), in this case) of
&pm;1. This interval, \[1,&nbsp;3\], contains 87.5% of all result
values.<sup>\[2\]</sup> And this is only the &ldquo;worst&rdquo; case; higher
or lower values of *p* will yield smaller variances/standard deviations.

As a result of this central tendency, high levels of &ldquo;dumb luck&rdquo; in
cogs&rsquo; multi-target attacks actually doesn&rsquo;t make cogs terribly
fickle in terms of raw damage output. That being said, there is, of course,
more significant variation to be expected when it comes to exactly *which*
toons are struck, as *p* decreases.

When deciding to nerf multi-target attacks directly, the following pros and
cons of nerfing the accuracy (by itself) should be taken into consideration,
although do note that nerfing damage and nerfing accuracy are not mutually
exclusive:

Pros of nerfing accuracy in particular:

- Less revisionist in some sense, because you can nerf accuracy without
  actually changing the observed effects of toons being struck by said attacks.
- Makes multi-target attacks less disruptive without actually changing the
  particular number of laff points required to survive a particular barrage of
  cog attack(s). This makes cog attacks *basically* just as deadly overall,
  while being significantly less of a drain on toon resources.

Cons of nerfing accuracy in particular:

- Less deterministic. This is mostly a problem in dire situations, where the
  lowered likelihood of a cog making you go sad might be nice &mdash; but
  hardly a guarantee or reassurance. However, it should be noted that although
  multi-target attacks are generally more powerful than the corresponding
  multi-target ones in TTR, the *per-toon* damage is typically roughly the
  same, so this point applies to essentially any cog attack with an accuracy
  that is &ldquo;significantly&rdquo; less than 100%.
- Because *only* nerfing accuracy keeps cog attacks at basically the same level
  of deadliness, this form of nerf is not as effective when reduced access to
  laff points is what demands the nerf.

And now, we will take a look at the pros and cons of nerfing multi-target
attacks directly, on its own:

###### pros

- Weakens cogs. This can be a good thing when it is warranted due to cogs being
  too powerful in comparison to toons.
- Not very invasive; all that need to be tweaked are damage and/or accuracy
  numbers.
- Can be an effective way of balancing single-target and multi-target cog
  attacks.

###### cons

- Weakens cogs. This can be a bad thing when it is unwarranted due to cogs
  already being as powerful as, or less powerful than, toons.
- Revisionist towards the set of cog attacks that exist in TTR, because the
  attacks themselves have to be modified.
- This method requires some meticulousness, because all cogs with multi-target
  attacks have to be balanced, against themselves and against all other cogs of
  a similar level. This includes balancing the damage/accuracy values for the
  attack *at each cog level* (of which there are 5 for a given cog species),
  for each such attack.

---

<details>
<summary>
footnotes for &ldquo;nerfing multi-target attacks directly&rdquo;
</summary>

1. Maximum variance occurs at *p*&nbsp;=&nbsp;0.5, because for a given *n*, the
   variance is [proportional][proportional] to
   *p*(1&nbsp;&minus;&nbsp;*p*)&nbsp;=&nbsp;*p*&nbsp;&minus;&nbsp;*p*<sup>2</sup>.
   Since this is [quadratic](https://en.wikipedia.org/wiki/Quadratic_equation)
   in *p*, the global maximum [is just where the derivative is
   zero](https://en.wikipedia.org/wiki/Parabola). The
   [derivative](https://en.wikipedia.org/wiki/Derivative) w.r.t. *p* is then
   1&nbsp;&minus;&nbsp;2*p*, by the [power
   rule](https://en.wikipedia.org/wiki/Power_rule). Finding where the
   derivative is zero:<br />
   1&nbsp;&minus;&nbsp;2*p*&nbsp;=&nbsp;0<br />
   &minus;2*p*&nbsp;=&nbsp;&minus;1<br />
   *p*&nbsp;=&nbsp;&frac12;&nbsp;=&nbsp;0.5.
2. The [probability mass
   function](https://en.wikipedia.org/wiki/Probability_mass_function) for a
   particular outcome *k* over a binomial distribution
   *X*&nbsp;&#x223c;&nbsp;*B*(*n*,&nbsp;*p*) is
   Pr(*X*&nbsp;=&nbsp;*k*)&nbsp;=&nbsp;<sub>*n*</sub>C<sub>*k*</sub>&nbsp;&times;&nbsp;*p*<sup>*k*</sup>(1&nbsp;&minus;&nbsp;*p*)<sup>*n*&minus;*k*</sup>.
   The sum of this PMF over *k*&nbsp;&isin;&nbsp;{1,&nbsp;2,&nbsp;3}, where
   *n*&nbsp;=&nbsp;4 and *p*&nbsp;=&nbsp;0.5, is 0.875&nbsp;=&nbsp;&frac78;.
   Note that this is not representative of [approximating the binomial
   distribution with the normal
   distribution](https://en.wikipedia.org/wiki/Central_limit_theorem) (where
   &pm;&sigma; contains [roughly
   68.3%](https://en.wikipedia.org/wiki/68%E2%80%9395%E2%80%9399.7_rule) of the
   result values) because there is no [continuity
   correction](https://en.wikipedia.org/wiki/Continuity_correction) (and *n* is
   small).

</details>

##### buffing single-target attacks directly

The considerations for buffing single-target cog attacks directly are largely
similar to (or rather, inverse to) the considerations for nerfing multi-target
ones. One notable difference is that changing accuracy values is no longer
really an option here; most cog attacks (especially those from cogs that are a
high level for their species<sup>\[1\]</sup>) have accuracy reasonably close to
100% anyways, and single-target attacks are not affected by accuracy changes in
the same way as their multi-target counterparts.

It should also be noted that buffing single-target cog attacks has the effect
of raising the threshold for how much laff a toon needs to have left to
withstand a given number of cog attacks. This is not necessarily the case when
tampering with multi-target attacks.

So let&rsquo;s take a look at the pros and cons of buffing single-target cog
attacks directly, on its own:

###### pros

- Strengthens cogs. This can be a good thing when it is warranted due to cogs
  being less powerful than toons.
- Not very invasive; all that need to be tweaked are damage numbers.
- Can be an effective way of balancing single-target and multi-target cog
  attacks.

###### cons

- Strengthens cogs. This can be a bad thing when it is unwarranted due to cogs
  already being as powerful as, or more powerful than, toons.
- Revisionist towards the set of cog attacks that exist in TTR, because the
  attacks themselves have to be modified.
- This method requires some meticulousness, because all cogs have to be
  balanced, against themselves and against all other cogs of a similar level.
  This includes balancing the damage values for the attack *at each cog level*
  (of which there are 5 for a given cog species), for each such single-target
  attack.

---

<details>
<summary>
footnotes for &ldquo;buffing single-target attacks directly&rdquo;
</summary>

1. &ldquo;Species&rdquo; here refers to particular named species, like
   Telemarketer or Corporate Raider.

</details>

##### attack limiting

Now we are brought to options more &ldquo;radical&rdquo; than just changing
some of the numbers, by introducing additional mechanic(s): first, attack
limiting. The basic idea is to treat cogs slightly more like toons, in that
they will have *some* attacks in limited quantity, just like toons can only
carry e.g. 3 Birthday Cakes. It should be noted that attack limiting is
discussed here as a way of balancing multi-target cog attacks against
single-target ones, but is actually potentially more useful. Attack limiting
can act as a general strategy to be used for game-balancing, as well as a way
to simply make cog fights more interesting.

It doesn&rsquo;t really make sense to allow cogs to run out of attacks
entirely, lest we fall into the trap of making cogs mirror toons for no other
reason than &ldquo;symmetry&rdquo; for its own sake; some asymmetry between
toons and cogs is intentional and beneficial to the game&rsquo;s design.
Rather, when applying attack limiting, it is expected that each cog species
will possess at least one attack that is unlimited in use.

Attack limiting should not break in the presence of v2.0 cogs or similar. If,
for example, a v2.0 cog has a one-time-only attack and uses it, and then has
their first shell defeated, their skelecog form should not be able to use that
attack.

The main issue left to hash out here (short of actually proposing a particular
attack limiting scheme for every cog species) is the issue of which numbers it
makes sense to use. Generally, it is expected that any limit greater than 3 or
so is not going to be very useful, because cogs are not expected to last very
long on the battlefield and perform a lot of attacks. Limits greater than 3 are
going to make the attack *effectively* unlimited most of the time in practice,
and even a limit of 3 on a single attack is probably pretty high. Again, it
depends on how you choose to balance the rest of the game as to how many
attacks you expect cogs to actually be able to perform in various situations.
Additionally, the effects of an attack being limited are dependent on the
probability of that attack occuring in general; an attack that is limited to
one time only, but has a 10% usage chance, is only *somewhat* limited by the
one-time-only bit. In general, most attacks that are limited should be limited
to either 1 or 2.

It *is* possible to slightly extend this concept by pooling some of the attacks
that a given cog species has into a group, and then putting a limit on that
group, rather than a separate limit for each attack in the group. However, this
complicates things considerably for no apparent benefit. Potentially, this is
useful when a cog has many attacks in their arsenal and you want to limit the
use of any of those attacks that aren&rsquo;t a particular one or two of them,
but that seems like a niche usecase. Any other benefits are a mystery as of
yet.

###### pros

- Weakens cogs (usually). This can be a good thing when it is warranted due to
  cogs being too powerful in comparison to toons.
- Doesn&rsquo;t require revising attacks; the attacks stay the same, and
  cogs&rsquo; use of them is what changes.
- Makes cog behavior somewhat more deterministic, in a way that toons can
  strategize around (viz. it is possible to know that a cog has exhausted some
  attack and cannot use it again).
- Flexible &amp; multi-purpose.

###### cons

- Weakens cogs (usually). This can be a bad thing when it is unwarranted due to
  cogs already being as powerful as, or less powerful than, toons.
- Invasive, because a new mechanic must be added into the game, which
  complicates the game&rsquo;s mechanics.
- This method requires some meticulousness, because any cog attack by any cog
  species is potentially the subject of attack limiting.

##### varying target numbers

Toying around with exactly how many toons can be hit by a given multi-target
cog attack is a possibility. The obvious way to do this is to set the (maximum)
number of targets for each of a species&rsquo;s multi-target attacks on a
per-attack-per-level basis, or just on the somewhat coarser per-attack basis.

Balancing on the level of target count could allow for more fine-grained
balance adjustments. It also could make the cog aggro mechanic more relevant
and a bigger part of toon strategy, because normally multi-target attacks
ignore aggro since they don&rsquo;t have to make any choice as to which toon to
target. On the other hand, while this is interesting, it is the most invasive
of all suggestions here in lieu of balancing multi-target vs. single-target
attacks.

###### pros

- Weakens cogs. This can be a good thing when it is warranted due to cogs being
  too powerful in comparison to toons.
- Can be an effective way of balancing single-target and multi-target cog
  attacks.
- Makes the cog aggro mechanic more relevant by making multi-target attacks
  possibly rely on aggro in terms of which toons they target.

###### cons

- Weakens cogs. This can be a bad thing when it is unwarranted due to cogs
  already being as powerful as, or less powerful than, toons.
- By far the most invasive method listed in this section. This is presumably
  *very* difficult to implement properly, since it requires messing with cog
  attack animations.
- This method requires some meticulousness, because all cogs with multi-target
  attacks have to be balanced, against themselves and against all other cogs of
  a similar level. This includes balancing the target count values for the
  attack *at each cog level* (of which there are 5 for a given cog species),
  for each such attack. Less demanding is setting the target count values on a
  per-species-per-attack basis rather than *also* varying by cog level.

## toontasks

Many &ldquo;generic&rdquo;/&ldquo;randomly generated&rdquo; toontasks are
excessively difficult in comparison to other tasks available in their stead,
for the same reward. The infamous tasks like &ldquo;defeat 200 5+ story cog
buildings&rdquo; obviously fall into this category, but so do many others. In
many cases it&rsquo;s unclear why the tasks exist in the first place, other
than perhaps as a cruel practical joke played on those who accidentally accept
them. In other cases, the tasks just need to be a bit more balanced to be in
line with other comparable tasks with the same reward.

This calls for some adjustment of the random task generation algorithm.
Toontasks need not be extremely balanced; balancing them with one another is
not a huge part of improving the game, and some variation in balance is
acceptable, because different toons will have different preferences and
priorities at different times. Additionally, super difficult tasks (like our
infamous example of &ldquo;defeat 200 5+ story cog buildings&rdquo;) need not
be removed entirely, so long as one is willing to invent new rewards, e.g.
15000 jellybeans, or perhaps a *permanent* goofy cosmetic effect to add to
one&rsquo;s cosmetic effect inventory, to be used at any time (like clothing in
one&rsquo;s wardrobe).

Probably the easiest way to come up with a reasonably fair algorithm is by
assigning point values to objectives (and modifiers thereof). Also, point
values have to be determined for particular rewards; not just assigned to the
reward itself, but to the combination of the reward with the chapter that it
belongs to (e.g. Daisy Gardens, or Donald&rsquo;s Dreamland II). Then, when
randomly generating a task for a particular reward, one simply chooses some
sensical assortment (for example, it doesn&rsquo;t make sense to have to defeat
5 4+ story coin mints&hellip;) and adds together their point values. Then, one
divides the point value of the reward by this sum, and rounds to the nearest
integer (to a minimum of 1). This will give the number of times that the
objective has to be acquired/completed/defeated/&amp;c.

Here, we will try to devise one such point-based scheme, although this is only
a suggestion/demonstration. We will start first with assigning point values to
requirements. Also note that the code snippets are in Python:

| requirement                                                                                      | points                               |
| ------------------------------------------------------------------------------------------------ | ------------------------------------ |
| cog defeated                                                                                     | 10                                   |
| cog is at least level `n`, in no particular area<sup>\[1\]</sup> and/or facility<sup>\[2\]</sup> | `32 // (13 - n) - 1`<sup>\[3\]</sup> |
| cog is at least level `n`, in a particular area<sup>\[1\]</sup> and/or facility<sup>\[2\]</sup>  | 4                                    |
| cog must be at least level 11                                                                    | 5                                    |
| cog must be at least level 12                                                                    | 14                                   |
| cog must be v2.0, in no particular area<sup>\[1\]</sup> and/or facility<sup>\[2\]</sup>          | 35                                   |
| cog must be v2.0, in a particular area<sup>\[1\]</sup> and/or facility<sup>\[2\]</sup>           | 15                                   |
| cog of a particular type<sup>\[4\]</sup>, in no particular facility<sup>\[2\]</sup>              | 12                                   |
| cog defeated within a particular area<sup>\[1\]</sup>                                            | 6                                    |
| cog defeated in a particular facility<sup>\[2\]</sup>                                            | 15                                   |
| cog must be of a particular species<sup>\[5\]</sup>, in no particular facility<sup>\[2\]</sup>   | 40                                   |
| cog must be of a particular species<sup>\[5\]</sup>, in a particular facility<sup>\[2\]</sup>    | 15                                   |
| building defeated                                                                                | 60                                   |
| building must be at least `n` floors                                                             | `15 * (n**2 + n - 2)`                |
| building of a particular type<sup>\[4\]</sup> (minimum floor count of `n`)                       | `75 * n`                             |
| building within a particular area<sup>\[1\]</sup> (minimum floor count of `n`)                   | `45 * n`                             |
| factory defeated                                                                                 | 360                                  |
| &hellip;                                                                                         | &hellip;                             |

There are some subtleties here, many of which are captured by the expectations
already set forth by TTO. For example, tasks requiring cogs of a particular
species *and* a certain minimum level should be avoided so as to not
effectively double-count points; this kind of task doesn&rsquo;t exist in
TTO/TTR anyways. One of the nice things is that this kind of scheme is quite
flexible; it can be tweaked as needed to generate better tasks, as one sees
fit.

---

<details>
<summary>footnotes for &ldquo;toontasks&rdquo;</summary>

1. &ldquo;Area&rdquo; here refers to a playground (Toontown Central,
   Donald&rsquo;s Dock, &amp;c.) or cog HQ (Sellbot HQ, Cashbot HQ, &amp;c.).
   It does not refer to more specific areas like a cog building or bullion
   mint.
2. &ldquo;Facility&rdquo; here refers to a location that is more specific than
   an &ldquo;area&rdquo;, like a cog building or bullion mint.
3. This formula only works if the maximum cog level is 12.
4. &ldquo;Type&rdquo; here refers to the four types sellbot, cashbot, lawbot,
   &amp; bossbot.
5. &ldquo;Species&rdquo; here refers to particular named species, like
   Telemarketer or Corporate Raider.

</details>

## gag tracks

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

[function]: https://en.wikipedia.org/wiki/Function_(mathematics)
[on-sbfos]: https://gist.github.com/JonathanHelianthicusDoe/e5a261941bfa0f29148a6999b6ca7a65
[sawtooth]: https://en.wikipedia.org/wiki/Sawtooth_(wave)
[proportional]: https://en.wikipedia.org/wiki/Proportionality_(mathematics)
