# Flowrist Keyboard Layout

<!-- (fLowRiST, Technogrok, Grokkable, GeeKCoDe, gkcd) -->

Flowrist is a keyboard layout that focuses on:

- minimizing **redirects** and **stretching** (low LSBs, AKA lateral movement)
- the easiest possible (though high at 2%) and mostly **downward SFBs**
- a reality of **near-0 D/SFBs** with designed alt-fingerings
- **offloading pinkies** for busy indexes and middles

It is designed to be **easy to transition to from Colemak(-DH),** keeping most
of its core intact (only 2 of the top-10 freqs changed: `a` and `o`; and ~10
lower-freq tweaks). One could also transition from QWERTY with ~13 moves (see
section below for intermediate layout). The intentionally high SFBs (still
under 2%) are almost all middle-to-index finger overlaps, and applying that
overlap technique actually brings the elbows outward into a more natural wrist
position. See the [transitional](#transitional) section below to try Flowrist
with just 5 total moves from Colemak.

```
` √ b f p x   y w o u '
^ l r s t m   ¢ ŋ e i a
q g k c d v   n h / . ,
       ◊ ⇑     ⇐ _
```

(`√` is _compose_, `◊` is _magic_, `ŋ` is `nh` _adaptive_, `¢` is `Ctrl-c`,
`j` (`cd`) and `z` (`gk`) are combos, and all of these are optional)

It's originally designed to be used optimally with a reverse-symmetric-stagger
keyboard (to make the SFB overlaps easier) as:

```
\ ` √ b f p x  \    /  y w o u ' /
 \ ^ l r s t m  \  /  ¢ ŋ e i a /
  \ q g k c d v  \/  n h / . , /
           ◊ ⇑        ⇐ _
```

_(It has been tried on a matrix-style keyboard and still felt good, but needs
much more trial.)_

Flowrist harmonizes from the beginning: an adaptive key, a different kind of
keyboard, two active thumbs, all vowel-likes on the right hand (even `w`),
editor spatial awareness, `l` where it's maybe never been, three letters
hidden or in odd places, a magic/repeat multi-purpose key, and an easy-compose
for non-English. Here you'll also find an alt-fingering practice guide and a
one-step tarmak-like 5-move transitional layout.

The novelties/surprises here:

- `ŋ` (`nh`) is an _adaptive_ key, defaulting to `n`, but `h` after other
  letters (which is surprisingly easy to learn)
- bare-`h` is still convenient since you need it for words that start with `h`
- bare-`n` exists because there is a rare need for it for words like `siGn`
  (vs `gh`), `oWn` (vs `wh`), `fiTness` (vs `th`), and `Snake` (vs `sh`)
- all the vowels and semi-vowels (`yw`) are on the right hand (only 8
  letters!), enabling all shortcuts on the left hand (explanation below)
- `◊` is the "regic" (repeat/magic) key that does _repeats_ for some and
  _magic_ (multi-letter macros) for others
- this isn't great for SFBs according to the analyzers, but it's tuned for a
  reverse-symmetric-stagger keyboard where SFBs can actually be good rolls
- the `z` I end up using is actually a `gk` combo (and works surprisingly
  well), and `j` is `cd`
- `q` is an extra pinky key instead of `shift` (`v` or `m` also work there but
  busy pinkies)
- left-hand rides low, right is high, and that seems fine (this being thanks
  to Colemak heritage)
- the symmetric-stagger's elbows-out twist makes patterns like `ue`, `on`,
  `mp`, `ft`, especially comfortable, and even 2-row hops like `f.c`
  (_middle-index_) are easy

There is a (barely scrutable)
[example QMK implementation of Flowrist for Anatak][17], with _magic_ and
_adaptive_ keys, where the mapping is
upside-down (because the keyboard is an upside-down [Katana60][18]). Note
you're on the `thumbin` branch.

Caveat about the designer: I am not a speedy typist; have only gotten to 100
wpm on qwerty, same on Colemak, and have a history of only taking my own
designs and others to <60 before getting distracted and making more changes.
It's taken me ~5 significant iterations over 6 months to arrive at _Flowrist_.
After over a month on Flowrist I'm at 60 wpm on English-5k, 80 wpm on
English-100, have some bursts to 120+, and didn't feel any obvious bottlenecks
that would limit faster fingers from going further. Especially given the
no-SFBs patterns listed below (~60 of them). It has been tested by me on up to
English-10k, plus all the potentially awkward trigrams from [this post][12],
and even Spanish, French, Portuguese, and German. I'm obviously biased, but
this is the most comfortable my wrists have felt on any of the many layouts
I've tried.

## Defying the analyzers

[Oxey's Layout Playground][3] gives roughly the following scores:

> - Sfb:  1.94%
> - Dsfb: 7.52%
> - Lsb:  0.95%
> - Redirects:    4.24%
> - BadRedirects: 0.12%
> - Home keys usage: 64%
> - Total Rolls: 44.7%

The SFBs in particular look not great at all, and in some ways actually worse
than Colemak. However, I don't think they tell the real story:

- If you discount the index and middle SFBs (because most of the others are designed
  to be easy-alts), you're left with:
  > - Sfb:  0.48%
  > - Dsfb: 1.29%

- **Redirects** at _4.2_ sounds suboptimal due to the `n` (with `h`) on
  right-hand, but actually _feels_ ok with index: ∴ `n` on vowel-hand is ok
  only if index (and many layouts have done this), especially since it's
  adaptive (eg, `tHiNk` is a same-finger redirect). _Compare this to Colemak's
  10.5% and Qwerty's 13.2%._

  _(You could get redirects down to almost nothing if you move the `ŋ` to
  thumb. I didn't find that worth it since redirects with index are not a
  showstopper IME. Otherwise, redirects are VERY good at 1%! But do note that
  redirects in general are something to really avoid as much as possible and
  an important decision. Try typing `stretch` on Colemak an realize the
  slowness of your left hand changing direction 3 times.)_

- **SFBs** are almost completely on the "strength columns" and so mostly fine
  with index and middle (particularly with [anatak][4]). Qwerty and Colemak are
  both actually good at this too (but see next point). (I tried going up to 3%
  SFBs there and that got messy.)

- The remaining 0.48% SFBs are `br` (not `rb`) and `rk` (not much `kr`), which
  are **_downward-overlap_ alts**, and are reasonable with ring-middle (or
  magic). That downward part is important, and in in contrast to Colemak's
  _upward_ `rw` DSFB (where you have to shift or slide or use ring-pinky). The
  same is true on the right-hand with `ui` (Colemak is pretty good with these
  too).

- Having a _few_ terrible patterns is ok so long as you have **magic**
  (left-thumb) workarounds (up to maybe 8): `any` (`a◊`), `back`, `why`, `one`
  (`u◊`), `ious`, `how`, `yeah`; and these apply nicely as composable chunks:
  `anyone` -> `a◊u◊`, `many` -> `ma◊`, `glorious` -> `g◊ori◊`

- Those "terrible patterns" happen in any layout, and addressing them with
  magic is a huge win, considering that those 3+-letter chunks (or full words)
  comprise nearly 1% of the top-10,000 words (and 3% of the top-1,000). That
  means nearly 100 of the hardest words are practically free to type.

- **LSB** (lateral) hand-shifting by one key is feasible: `MoVe` and `ONlY`
  move a hand to one position, but it's easy enough with some practice; other
  examples: `MuST`, `tHEY` (and see many more below; those are all hard
  examples!)

- The **LSB** (lateral) score of _0.95_ is misleading. I consider it closer to
  _0.2_ since almost all of it is due to the `yo` roll-stretch (and a little
  `ye`) which is same-row (and even less stretch on anatak). And compare that
  to Colemak/DH's atrocious 3.5/2%!

- It's more **inward-rolly** than it looks. This is true of other layouts too,
  but Flowrist has a little more by design with `wh`. It also inherited a few
  from Colemak like `pt` (and `sc` is ok). Other decent ones are `m.v`, `mp`,
  `t.m`, `t.d` (if you can call those true rolls). I'd like to see layouts go
  further with the concept and design for strength columns to have a lot more
  of these; slots `nh`, `td`, `oe`, and even `pt` are missed opportunities!
  Well, so are `fp` and `cd`, but at least we have a lot of these for combos.

- **Rolls** overall are way undercalculated. If you count `pt`, `sc`, `wh`,
  `mp`, you see another 8+%, bringing the actual total to well above 50%.

So if you take my interpretation of all that, you can _kinda_ say these are the
real numbers:

> - Sfb:  0.48% (on non-strength cols)
> - Dsfb: 1.29% (on non-strength cols)
> - Lsb:  0.19% (discounting same-row `y`, and magic)
> - Redirects:    4.24%
> - BadRedirects: 0.12%
> - Home keys usage: 64% (thanks to `ŋ`)
> - Total Rolls: 51%

The [Cyanophage Playground][1] gives the following _effort_ scores, with a few
advantageous tweaks for [Anatak][4], and doesn't count the adaptive `ŋ`:

> - Total Word Effort: 1032
> - Effort: 400

## Spatially tuned for code editors (Emacs, shells, and maybe others)

The most common code-editor command-letters are in strong and spatially
meaningful positions. Vim is completely ignored since it was built
specifically for qwerty and seems ridiculous to retrofit for better layouts
IMO (though modal editing with god-mode, meow, etc can be great). I found
layouts that put `n` (next) and `b` (back) and other repeatables on pinky were
taxing it (graphite, gallium, engram, carbyne, beakl).

Here are the directional/spatial pairings:

- `bf`  — _back/forward_
- `pn`  — _prev/next_ (`p` is high, `n` is low)
- `ywh` — _yank/save/select_ (clustered, all right-index)
- `ae`  — _start/end_ (though backwards)
- `sr`  — _search (forward)/reverse_
- `qgk` — _quit/cancel/kill_ (Emacs, these are really cool!)
- `cl`  — _capitalize/lowercase_ (though backwards)
- `cxv`  — _cut/paste_ (non-editor apps; still kinda together, but macros preferred)
- `SPC`/`BSPC` — next/prev page etc.

Other happy accident pairs: `y/n` — yes/no; `l/r` — left/right

## Adaptive n/h

This was a really fun discovery and borrowed directly from [horn][7]'s QMK
code. It runs on a 500 ms timer so that normally typing `sŋ` is `sh` but if
you wait half a second between strokes, it's back to `sn`. But this is just
important for editor sequences like `(C-x) C-s` to save your buffer and then
`C-ŋ` to go to _next_ line fairly quickly becomes `C-n` (as intended) and not
`C-h`.

## Slots for combos (very rare pairs)

There are several two-key combos that when pressed simultaneously work well as
macros. Eg, I use `gk` as the `z` key. Here is my full set, but these should
be changed to suit your prefs.

- `gk` — `x`
- `cd` — `j`
- `gq` — copy-paste buffer menu
- `bf` — `C-TAB` (browser previous)
- `rl` — `TAB` (experimental since `eaRLy`)
- `fp` — `=`
- `tm` — `:`
- `cd` — `C-c`
<!-- - `jr` — `C-w` (close window, cut) -->
<!-- - `pv` — `C-v` (paste) -->
<!-- - `gm` — (but `seGMent`) -->
- `td` —
- `pb` —
- `.,` — `shift`
- `,-` — `backtick`
- `nh` —
- `h/` — `_`

## Less natural patterns for practice (for no D/SFBs!)

Every layout will have some _challenging patterns_. They should be well known
so that they can be practiced. The fastest typists in the world mostly still
use Qwerty, and they do that by constantly shifting and contorting their hands
to avoid SFBs. Flowrist was designed to turn the tort into comfortable
overlaps and minor shifts.

This section contains most of those patterns I've adopted (which are
optional), and is more for future reference, rather than a starting point. If
you find yourself ever slow (sliding) on a D/SFB, refer to this. The `imrp`
are for fingers: `i`ndex, `m`iddle, `r`ing, `p`inky. A `.` means
_uninteresting_.

Note that some patterns are not listed because they're expected to happen
without much thought or training. Eg, the word `type` naturally _starts_ the
_index_ on `t` and then the _middle_ actually wants to rotate above it to hit
the `p`, thus avoiding the DSFB. With `case` it's the same but with _middle_
then _ring_ for `c` and `s`. Contrast these with `put` where you have to train
your _middle_ to _start_ the word with an alted position; that's one of many
trainable patterns this section focuses on.

Although many folks may be comfortable with the `ho` index-middle (`im`)
stretch-reach, I am generally not (except maybe the `hou` case), so it is
usually _index-ring_ (which leaves _middle_ open for `n`). And _index-pinky_
for `hu`. Hungry now? :)

There are a few rare cases where the `ŋ` will surprise you. Eg, `own` has to be
bare-`n` since the `wŋ` sequence needs to resolve as `wh`. So you'll want to
reach for `o` with _ring_ (to actually get a nice roll out of it).

- `thin`/`than` (same adaptive index for `n` and `h`)
- `own/sign/snow` (bare-n)
- `han` (`mpi`) (long pinky stretch)
- `rope` (`.m.i`)
- `open` (`r.mi`)
- `one` (`rim`) (scrunch, or magic)
- `only` (`rm.i`) (hand-shift and hard down-up))
- `deny` (`.rmi`) (shift)
- `phy` (`.mi`)
- `hydro` (`im...`)
- `who/whe` (`mir`)
- `went` (`mri.`)
- `win/won/wen` (`mri`)
- `with` (`mr.i`)
- `new/now` (`irm`) (or magic for `new`)
- `home/hope/hose` (`ir.m`)
- `hun` (`ipm`)
- `people` (`.mr...`)
- `goes/does` (`.ri.`)
- `met/mat/` (`i.m`) (etc)
- `move` (`mmii`)
- `middle` (`i.m◊p.`)
- `admit` (`.mi.m`)
- `time` (`m.i.`) (shift)
- `tive` (`m.i.`)
- `advice` (`.mi.m.`)
- `dev/divide` (`m.i.m.`)
- `dep` (`i.m`)
- `det` (`i.m`)
- `dim` (`m.i`)
- `exp/ext` (`.im`)
- `pit/pat/put/pet/pot/peat` (`m.i`) (`p` is often middle; just look ahead for `t`)
- `face` (`r.i.`)
- `fact/fect/sect/fast` (`r.mi`)
- `they` (`.mri`) (shift)
- `part` (`m.pi`) (very often!)
- `post` (`m.ri`)
- `step` (`rmi`)
- `soft` (`m.ri`)
- `complete` (`m.imp...`)
- `vid` (`i.m`)
- `way` (`mpi`)
- `show` (`.irm`)
- `simple` (`r.imp.`)
- `enh/inh` (`rmi`)
- `hey` (`mri`)
- `they` (`.mri`) (home-`h`)
- `second` (`mmirii`)
- `stop` (`rim`)
- `most/must` (`irm`)
- `break` (`rm..i`) (if you wanna get crazy)
- `drop` (`ir.m`)
- `ber` (`r.m`)
- `fast/bars` (`r.mi`)
- `ying` (`ipm.`) (shift)
- `number` (`..ip.r`)
- `tod/ted` (`m.i`)
- `empty/assumption` (`.irm.`) (hard!)
- `minu` (`.rip`)
- `honor` (`irmr.`)
- `updated` (`.mi.m.i`) (still dsfb but not bad)
- `himself` (`..i.mpr`) (hard!)
- `str` (terrible redirect from colemak!)
- `eco` (`m.r`)
- `leg` (`p.r`)
- `quiet` (`.rmi.`) (or `qu◊et`)
- `techno` (`...ii.`)
- `garbage` (`p.rp.p.`)
- `exact` (`.i.rm`) (left-shifted)
- `note` (`ir.m`) (hard!)
- `wheat` (`mirp.`)
- `log/leg/lug/lag/lig` (`p.r`)
- `mark` (`..rm`)
- `gold/gild` (`r.p.`) (rare)
- `committee/keenness/whippoorwill/barrenness/unsuccessfully`
  (_repeat_ practice, full coverage! But also try monkeytype's "doubleletter"
  practice.)

There are some squirrely/surprising words involving `ŋ`:

- `ahead`
- `snow`
- `snake`
- `dawn`
- `own`
- `sign`
- `fitness`

Here they all are as full words if you want to paste them into Monkeytype:

```
thin than sign snow hand rope open one only deny hydro who when went win won went with new now home hope hose hunt people goes does met move middle time face fact fect sect fast expect extra they pit pat put pet pot peat part post step soft complete video way admit relative develop determine dimension matter metal advice show simple enhance inhibit hey they second stop most must break drop depend number fast bars lying today rated empty minus honor updated himself string eco leg physics quiet techno exact note remark gallery gold committee keenness garbage whippoorwill barrenness unsuccessfully ahead snow snake dawn own sign fitness
```


Once you've spent some time painstakingly practicing those funny feeling
patterns, you'll have a new typing paradigm that eliminates nearly all D/SFBS!

Here are a few of the particularly challenging, and could be magic or
just slowly typed (or really interesting alts):

- `beyond`
- `moment`
- `board`
- `consider`
- `marble`

If you want to focus on practicing a given letter or two (`m` and `g` in this
example), here's a way (from a terminal) — grab a list of words and:

```
echo `grep '[mg]' top1000.lst | shuf`
```

Then paste those into monkeytype's _custom_ setting.

For more general practice, I recommend starting with [keybr][23] and then
using [monkeytype][9] _words_ levels increasingly up to **English 5k**.

**Note on the left-thumb:** It takes quite a while to get used to using
a _regic_ key, even moreso when it's a new thumb. It took me a few weeks to
get comfortable.

## Fun new roll patterns somewhat unique to Flowrist

`au`, `bl`, `mp`, `wh`, `w/y/hou`, `ue`, `gr`, `ion`, `oi`, `fl`, `xp`, `xt`,
`ck`, `sm`, `sl`, `sk`, `lk`

Plus the usual Colemak unrecognized goodies: `pt`, `sc`, `fs`

## Similarity to Colemak

```
      F P     y     u
    R S T       N E I
      C D V     H
```

I called `y` a similarity because you know it immediately from qwerty days.
`u` is a "minor" move (though admittedly not that easy).

## Transitional

If you want to keep it more similar to Colemak, or do a transitional approach,
you can do the following, where the only 5 significant moves are `wolam` (but
don't get too settled with the pinky `m`!). This will give you a pretty good
taste of Flowrist without _all_ the upfront mental effort:

```
  Q z F P B   Y w o U
  l R S T G   j N E I a
  m X C D V   K H
```

After you've got that down, the next most important moves are `m/g`, and then
`b/z`.

## Magic config

Here are the fiddly/stretchy/logjammy/SFB (or very common) words from top-1000
that I feel are worth macro-ing via [repeat key][16]:

- `a` -> `any`
- `b` -> `between`
- `'` -> `\bI'`
- `h` -> `how`
- `i` -> `ious`
- `b` -> `between` (just convenient and easy to rememmber)
- `o` -> `one` (maybe, but `oo` is probably more important)
- `w` -> `why`
- `y` -> `yeah`
- `u` -> `ui`
- `g` -> `gl`
- `j` -> `dj` (since `j` is a combo)
- `k` -> `\bnew`
- `q` -> `\bprob`
- `x` -> `\bexcept`
- `^` -> `\bback` (above `b`; that's a backspace to remove the `"`!)
- `v` -> `\btogether` (why not, long common word)
- `;` -> `\bwithout` (above `w`)

The rest are repeats (eg, `◊e` is `ee`).

Here is a list of good practice words using magic (not repeats), that can be
pasted into Monkeytype and randomized:

```
however anywhere anyhow show scrumptious knew exceptional backward together between without problem probably quit quiet adjust gluten igloo neglect I'll I'm
```

## Personal Insights in Layout Design

Qwerty-G position (consonant hand only) is way undervalued. That reach feels
almost as good as home-row, and it's a waste to put `g` there. So now `m` is
there. Besides _whorf_, I've not seen this done. It is a heavyweight SFB there
and combines to alt there very well to "MiX" with `ptdvx`, and became a major
design characteristic of Flowrist.

_Some SFBs are not_ at all. The `wh` overlap is as good as any middle-index
usage, at least on a keyboard with symmetric slant. I can imagine a layout
with pretty bad SFB score yet is very comfy. Even `mp` is really
(qwerty-)`gr`eat.

_Adaptive keys_ (`nh`) are a game changer for home-row (thank you [horn][7]!).
They are slightly challenging since they waste a slot and require more choice.
But there's probably room for one more if there are two other letters that
complement/combine as well (besides `n`-vowel). Other candidates are `hf` and
`ir` and `m`-vowel, though the latter two will always be bad for redirects.

There is a balance between optimal typing and _editor commands location_.
Designers have considered `zxcv` together but it can go a lot further. If
`hjkl` is such a thing for qwerty Vimmers, why don't we emphasize its approach
in a layout. I'm tempted to even swap `p` and `w` to get the `pn` spatial
`prev/next` (but I like the `wh` too much to try).

It is soooo hard for me to learn a new layout from scratch. It would take me
many months to really be up to speed. Trying Canary wasn't terrible but
Graphite was unattainable in the time I had. So pushing Qwertizens to
something more Qwerty-like or transitional will enable more folks to take a
plunge.

It's not unreasonable to _use a combo as a key_. Using `gk` for `z` and `cd`
for `j` is working well for me. So it might be ok to do it for any of `x` and
`k` too. If you really want a first-class `j`, repace the `"` with it at
upper-left-pinky.

I'm uncertain about _hand balance_ and if it's overrated. The perfect letter at
Qwerty-H has big potential. Maybe that's a repeat-key. I have it as `Ctrl-c`
presently (for Emacs etc). So right-hand does a lot of work, but it feels like
not a problem.

There are "chunks" out there with great potential for magic. I'm using `how`,
`any`, `one`, `prob`, `new`, and a few others, and those are pretty good for
Flowrist but there may be opportunities here for other layouts.

_Rolls_ are great (though some prefer alternates-heavy, and they're great too
of course). However, to achieve really high rolls, you'd need to intermix
vowels and consonants on the hands. But this is so bad for redirects, so you
have to choose your tradeoff.

The somewhat infrequent keys are the hardest to place. Once you've got the
most important ~16, you can then put the lowest 4 somewhere really bad without
concern, but then you've got a few semi-important letters with nowhere to go.
This was the case for `b` and `y` (and kinda `g`). I tried several spots, but
no matter where you put them, there's going to be workarounds needed. Where
they landed iws simply the least bad. Comparing the `b` location to Colemak, I
find Flowrist

It was challenging to separately fit both a _repeat_ and _magic_ key, for
cognitive load, and lack of real estate. I found that a single key (I call
_regic_) sufficed for both purposes, since there wasn't too much magic needed,
and there were enough non-repeating keys to use for magic.

The optimizers we have available to us are incredibly powerful tools. And
there is room for other metrics and different ways to calculate what is
presently measured. My main conclusion is that there is enough uncertainty and
personal preference involved that probably the safest way to choose a layout
is simply using the one that hurts the least, and still keeps SFBs below
~3%. For me, that means:

- finding the right SFBs on the stongest fingers, and using pinky and ring
  with the fewest contortions.
- choose the best stretches, and vowel-hand shouldn't stretch much; even qwerty
  did ok at that (on the right)

## More Flowrist design explanation

Placing `w` above `h` means that although `w` _looks_ like an index key (and
thus a common SFB), it's almost as commonly a middle-finger. You'll know by
looking/thinking ahead a couple letters for a `n` or `h`. This means index
stays busy only pressing `y`, `w`, and `n/h` (and sometimes `h` and `e`). And
that `wh` is a very nice inward roll (which analyzers won't detect) for a gain
of 3+%. Note also that `wh<vowel>` is always a redirect. However, it feels
fast and natural with a little practice.

**Vowels on the right**. Most performant layouts have a vowel-hand to get
fewer redirects. This is why we have `w` and `h` on the right (as an inward
roll): `w` is a semi-vowel, and `h` is arguably [not totally a
consonant](https://linguistics.stackexchange.com/questions/4834/why-is-h-called-voiceless-vowel-phonetically-and-h-consonant-phonologically)
and thus works well on the vowel hand. So the exception is `n`. It's over
there for a couple reasons: tradition (so many will already be comfortable
with it); and it's the best _adaptive_ combo IMO. It's bad for redirects there
but a worthwhile compromise. I tried swapping it with `f` (and adaptive `fh`)
but it wasn't worth it with all the _left-middle_ SFBs on `n`. I can further
justify `n` being with the vowels since it (ignoring `ç`) is the one non-vowel
diacritic in Spanish (and French?).

Hand shape is a big consideration. With a non-column-staggered keyboard,
middle fingers naturally sit high (Qwerty-`f` and -`u` spots) and pinkies sit
low (Qwerty-`z` and -`/` spots). This is why Flowrist places `o` high on
right-middle, and `g` and `,` on low-pinkies, making for strong keys. (`f` is
too low a freq for there but keeping for Colemak compat; `,` is good as an
editor "leader key".) I would argue that those four spots are the next best
thing to homem-row.

**`g` on pinky**. There are D/SFBs with `g` and `l`, and the `gl` is terrible,
so it absolutely needs magic there, at which point it's great. But I'm overall
pleased with the `g` location, particularly for the `gr` in-roll.

**`l` on pinky.** I haven't seen any other layouts that do this, but it feels
great to me and the stats are great — better than `c` or other possibilities
I've seen/tried for that spot.

**`y` is awkward**. It needs _magic_ for _any (a◊)_, _why_ (w◊), and _yeah_
(y◊), but is otherwise surprisingly good there, especially for `yo...`. And it's
familiar from Qwerty.

**`v` and `m` look like stretches ... but aren't.** It's exciting when you
find spots for things that just fit. The only downside I feel with `v` is that
`Ctrl-v` is very common in Emacs (and others' paste) and is a far stretch.
However, _god-mode_ takes care of this.

**`w/h/n` DSFB takes practice.** With some lookahead, you'll know when to
adjust index/middle/ring. Once you get used to it, they work well. This is
probably the quirkiest arrangement in Flowrist, but will hopefully grow on
you.

**Indexes are overloaded**. Yes `tpmvd` together on left-index result in 1.5%
and 0.5% in D/SFBs, but in practice almost all of their patterns work very
well with some practice on their _index-middle_ alt dances.

**Some `Ctrl-` shortcuts left the left (non-mouse) hand**. There was no way
`a` could stay on left. `w` is the other unfortunate victim. But for
right-handed mousing, you want all the shortcuts to be fully left-handed.
Outside of Emacs, I use triple-click more often now instead of `Ctrl-a`. And I
QMK-mapped `fs` combo to be `Ctrl-w`. And `bf` to be `Ctrl-Tab`. On the bright
side, you now have `Ctrl-l` on the left. It helps to have a `Ctrl` key on the
right hand too. You can re-bind some alternatives on left-hand to handle the
missing shortcuts. In fact, when I have to switch over to a Mac, I remap some
of the Mac shortcuts to use `Ctrl-` instead of `Cmd-` to get the consistency
across OSs. This way, the same macros, `kd`, `xm`, `mv`, `fs`, `lq` work
across OSs for copy, cut, paste, close, select-all.

## Eurolang layer (ligatures and diacritics)

Flowrist takes the [Compose][21] key into strong consideration for typing
international characters, by placing the following into easy unshifted reach:
`'^~"` (and `grave/backtick`). Here are the top two rows to enable just about
any imaginable diacritic characters, such as `éàôñçüøœŭȧłå` (here `√` is
Compose).

```
 . . ^ ~ . . .   . . . " . .
 ` √ b . . . .   . . . u ' .
 . l r s t . .
```

You may have already noticed from typing words like `beauty`, `question`,
`cruel`, `saint` (and `lieu` isn't so bad), etc, that Français works very well
with Flowrist, given its vowel layout. Español and Portuguese are great too.
The `eu/ue` being nice rolls really helps several languages, and most modern
layouts struggle here in having made those an SFB. And, how many times a day
do you type `true`?!

More fun French words:

- oeil
- étaient
- avouer

The following layer would likely be good for covering just about all of
French, Spanish, German, Italian, Portuguese, Esperanto (and most of [these
others][20]), but I haven't yet figured out how to get [key sequence
macros][19] (eg, `Compose-~-n` -> `ñ` should be `LangLayer-n` since
the former is more tedious to type) working.

```
 . . ß ĵ . .    ŭ õ
 . . . ĥ . .    ù ò è ì à ã
 . . . ŝ . .    ú ó é í á ñ
 . ĝ ç ĉ . .    û ô ê î â õ
 . . . . . .    ü ö ë ï ä
```

## What's really wrong with Colemak?

...and is it really worth switching? If you have the time and energy to switch
again, I do think it's worth it. Here are the major shortcomings I see with
Colemak:

- **Redirects are a killer.** The poster child is `you`. After a lot of
  practice, you can get fast at it, but my experience was that it will always
  be error-prone. It's especially bad to have redirects involving _ring_ and
  _pinky_. At 10.1% total and 1.47% "bad", it's really hard to not feel
  crippled by them (`you` is half of those bad ones btw). _Flowrist gets
  redirects down to 4.2% total and 0.12% bad._

- **`m` on center-right-column causes LSBs.** `m` alone is a 1.5% LSB (and
  also 2% of redirects). It definitely doesn't belong anywhere near there. And
  as soon as you move it to left-hand, lots of other moves cascade with it.
  _Flowrist takes LSBs down to 0.2% if you discount `y` with magic._

- **Not a real vowel hand.** `a` on left causes 2.2% more redirects and plainly
  makes the design chaotic (even if it was good for rolls). It also accounts
  for the other half of the bad ones. In contrast, _Flowrist has an extreme
  vowel-hand._

The above problems result in a list of [very challenging Colemak words][22],
almost all of which become easy words with Flowrist.

Furthermore, Colemak(-DH) wasn't easy to learn. It managed to keep some
infrequent keys the same as Qwerty: `zxqwg`, but the only core keys that
really stayed the same were: `ac`. And that was a problematic location for `a`
anyway! Plus, moving `s` over one spot was unnecessarily cruel.

All that said, Colemak is pretty/really good on: **Effort, SFBs, rolls, and
underloading rings and pinkies**. But even Qwerty is good on the underloading!

Applying _magic_ to Colemak may be a much simpler approach to solving some of
its shortcomings. I didn't discover magic until too late in the game (and so
haven't tried to invent the right patterns for it there), but that's a good
place to start, if you're not fully convinced that you need new a new layout.

## So why not just use Canary?

As a Colemak variant, I wanted to make [Canary][6] work for me, as I was
trying move beyond Colemak. It made some good steps to reduce redirects,
especially some bad ones, and SFBs are fantastic. `crst` works well, and `g`
is nice there, and `f` is good on RHS. But here's what I couldn't live with:

- `m` could never work alongside `n` on right-hand. Way too much LSB and
  redirects from it. It does help rolls being on right, but not worth the
  cost, IMO.

- More divergent from Colemak than was necessary, especially in the core with
  `f` and `c` moving.

- `r` and `l` together on ring was breaking my wrist with the upward-to-pinky
  DSFBs. `grep 'r..?l' 10k.lst` exposes this problem that I can't see any
  workaround for.

- `w` was tiring out pinky in that high-reach spot.

Side note: I originally hated the `one` pattern, but ended up with it in
Flowrist anyway, and decided that it was acceptable since I had a magic
workaround for it. But then I tried typing it enough (`mir`) and got
used to it, and now don't feel that it's so godawful.

## FAQs

- **Can I use this on a matrix keeb?** _Yes_

- **What about a normal keyboard?** _I think so, but right-hand will need a
  tweak to put `w` somewhere else; maybe on center-col-right-index or even
  right-pinky._

- **Do I need the adaptive `nh`?** _No, it'll work fine without, having it be
  a normal `n`, but you lose the crazy-high home-row stats._

## Possible Variations

One of my least favorite positions is `b` (for the `br` D/SFBs). It could be
moved to Qwerty-`h`, but that doubles the LSBs and makes redirects slightly
worse. It can also go to Qwerty-`t` (like Colemak), swapped with `x`, but I
like that even less, and it's BaD for your BoDy, and the DeBT is not open for
DeBaTe (and I type `db` a lot).

Some people may not like `g` on low-pinky. It could be moved up to Qwerty-`q`
position if you use a col-stag keyboard.

## Shortcomings / Unsolved Problems

- `g.l` — eg, `gallery`, `legal`, `girl`, `highly`, `changelog`. Only thing I
  can think of is to hit `g` with _ring_. And I'm getting better at it.

- It's pretty slow to learn to use thumb for things, particularly a repeat
  key.

- Some common proper names have odd patterns and don't do well with adaptive
  ŋ: John, Micah, etc.

## Transitional Intermediate from QWERTY

This keeps half the letters roughly the same as QWERTY, and gets you most of
the benefits of the full Flowrist layout, without the final ~6 swaps (`a/l`
pinky swap being the most important for redirects). Use this for maybe a
couple weeks before making the final swaps (or skip all this and go
cold-turkey directly to full Flowrist).

```
 Q b f p k   Y w O u '
 A r s t G   H n e i L
 Z X C d V   J M , . /
```

[1]: https://cyanophage.github.io/
[2]: https://www.worldwidewords.org/qa/qa-ini1.htm
[3]: https://oxey.dev/playground/index.html
[4]: https://github.com/MicahElliott/anatak60
[5]: https://github.com/rdavison/graphite-layout
[6]: https://github.com/Apsu/Canary
[7]: https://lykt.xyz/horn/
[8]: https://www.keybr.com/
[9]: https://monkeytype.com/
[10]: https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md
[11]: https://oxey.dev/index.html
[12]: https://www.reddit.com/r/typing/comments/172umsd/896_trigrams_in_200_words_a_new_selection_of/
[13]: https://sites.google.com/alanreiser.com/handsdown/home
[14]: https://forum.colemak.com/topic/1858-learn-colemak-in-steps-with-the-tarmak-layouts/
[15]: https://apps.apple.com/my/app/keybuild/id1547174534
[16]: https://github.com/qmk/qmk_firmware/blob/master/docs/feature_repeat_key.md
[17]: https://github.com/MicahElliott/anatak60/blob/thumbin/keymap.c
[18]: https://candykeys.com/product/katana60-pcb-V2
[19]: https://getreuer.info/posts/keyboards/macros/index.html
[20]: http://letterfrequency.org/letter-frequency-by-language/
[21]: https://en.wikipedia.org/wiki/Compose_key
[22]: https://github.com/MicahElliott/colemak-practice/blob/master/best.lst
[23]: https://www.keybr.com/

## Thanks!!

- _Oxey_ and _Cyanophage_ for their analyzers
- _Pascal Getreuer_ for all the QMK additions
- The tireless layout designers
- The many avid posters on _r/KeyboardLayouts_
- _Giorgi Chavchanidze_ for the Horn layouts (and other research)

<!-- Hi! Wanted to share the "Flowrist" layout I finally landed on. It might not be -->
<!-- practical for some, given the "inverted symmetric-stagger" (aka upside-down) -->
<!-- keyboard I use (though katana60 boards are available!), but it should also -->
<!-- work with ortholinears, and hopefully some of the ideas in the write-up I made -->
<!-- here are interesting/useful to some: https://github.com/MicahElliott/flowrist -->

<!-- ``` -->
<!-- \     b f p x  \    /  y w o u ' / -->
<!--  \   l r s t m  \  /    ŋ e i a / -->
<!--   \ q g k c d v  \/  n h / . , / -->
<!--            ◊ ⇑        ⇐ _ -->
<!-- ``` -->

<!-- What I hope makes this worth a read is that it tries to harmonize from the -->
<!-- beginning: an adaptive `nh` key, two active thumbs, all vowel-likes on the -->
<!-- right hand (even `w`), editor spatial awareness, `l` where it's maybe never -->
<!-- been, three letters hidden or in odd places, a magic/repeat multi-purpose key, -->
<!-- a different kind of keyboard, and an easy-compose for non-English. There's -->
<!-- also an alt-fingering practice guide and a one-step tarmak-like 5-move -->
<!-- transitional layout. -->

<!-- I think it could be used on a matrix-style keyboard too, so if any Colemakkers -->
<!-- wanna give it a try, it aims to be a close derivative. -->

<!-- I'm not planning presently to change much about it since it's working well for -->
<!-- me, but certainly interested in hearing from the knowlegdeable folks I've -->
<!-- learned so much from reading here (and really anyone): if there are any -->
<!-- obvious flaws or expected eventual pain points or clear improvements or WTFs, -->
<!-- etc, so I could consider fixing them. Also a big shout-out to Oxey, and -->
<!-- Cyanophage, phbonacci, and several others for their analyzers, open analysis -->
<!-- discussions, and layouts that have been so inspiring to make it possible for -->
<!-- plebs like me to be able to make a layout! -->
