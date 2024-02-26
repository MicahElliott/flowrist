# Flowrist Keyboard Layout

<!-- (fLowRiST, Technogrok, Grokkable, GeeKCoDe, gkcd) -->

Flowrist is a keyboard layout that focuses on:

- minimizing **redirects** and **stretching** (low LSBs, AKA lateral movement)
- the easiest possible (though high at 2%) and mostly **downward SFBs**
- a reality of **near-0 D/SFBs** with easy alt-fingerings
- **offloading pinkies** for busy indexes and middles

It is designed to be easy to transition to from Colemak(-DH) with ~12
(mostly lower-freq) keys moving, and maintaining most of its core. One could
also transition from QWERTY with ~13 moves (see section below for intermediate
layout). The intentionally high SFBs are almost all middle-index finger
overlaps, and applying the overlap technique actually brings the elbows
outward into a more natural wrist position.

There is a sample implementation for QMK.

```
√ j b f p x   y w o u '
  l r s t m   ¢ ŋ e i a
q g k c d v   n h / . ,
       ◊ ⇑  z  ⇐ _
```

(`√` is _compose_, `◊` is _magic_, `ŋ` is `nh` _adaptive_, `¢` is `Ctrl-c`,
and all of these are optional)

It's really designed to be used with a reverse-symmetric-stagger keyboard (to
make the SFB overlaps easier) as:

```
\   j b f p x  \    /  y w o u ' /
 \   l r s t m  \  /    ŋ e i a /
  \ q g k c d v  \/  n h / . , /
           ◊ ⇑    z   ⇐ _
```

_(It has been tried on a matrix-style keyboard and still felt good, but needs
much more trial.)_

The novelties/surprises here:

- `ŋ` (`nh`) is an _adaptive_ key, defaulting to `n`, but `h` after other letters
- bare-`h` is still convenient since you need it for words that start with `h`
- bare-`n` exists because there is a rare need for it for words like `sign`
  and `own`
- all the vowels and semi-vowels (`yw`) are on the right hand (only 8 letters!)
- `◊` is the "regic" (repeat/magic) key that does _repeats_ for some (most) and
  _magic_ (multi-letter macros) for others (a few)
- this isn't great for SFBs according to the analyzers, but it's tuned for a
  reverse-symmetric-stagger keyboard where SFBs can be good (rolls)
- the `z` I end up using is actually a `gk` combo (and works surprisingly well)
- `q` is an extra pinky key instead of `shift` (`v` or `m` also work there but
  busy pinkies)

There is a (barely scrutable) [example QMK implementation of Flowrist for
Anatak][17], with _magic_ and _adaptive_, where the mapping is upside-down
(note you're on the `thumbin` branch).

Caveat about the designer: I am not a speedy typist; have only gotten to 100
wpm on qwerty, same on Colemak, and typically only take my own designs and
others to 60 before getting distracted and regressing to more changes. It's
taken me ~5 significant iterations over 6 months to arrive at _Flowrist_.
After a few weeks on Flowrist I have had some bursts to 120, and didn't feel
any obvious bottlenecks that would limit faster fingers from going further.
Especially given the no-SFBs patterns listed below. It has been tested by me
on up to English-5k, plus all the potentially awkward trigrams from [this
post][12]. I'm obviously biased, but this is the most comfortable my wrists
have felt on any of the many layouts I've tried in anger.

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

- If you discount the index and middle SFBs, you're left with:
  > - Sfb:  0.48%
  > - Dsfb: 1.29%

- **Redirects** at _4.2_ sounds suboptimal due to the `n` on right-hand, but actually
  _feels_ ok with index: ∴ `n` on vowel-hand is ok only if index (and many
  layouts have done this). Compare this to Colemak's 10.5% and Qwerty's 13.2%.

  _(You could get redirects down to almost nothing if you move the `ŋ` to
  thumb. I didn't find that worth it since redirects with index are not too
  detrimental IME. Otherwise, redirects are VERY good at 1%! But do note that
  redirects in general are something to really avoid as much as possible and
  an important decision. Try typing `stretch` on Colemak an realize the
  slowness of your left hand changing direction 3 times.)_

- **SFBs** are almost completely on the four "strength columns" and so mostly fine
  with index and middle (particularly with [anatak][4]). Qwerty and Colemak are
  both actually good at this too (but see next point). (I tried going up to 3
  SFBs there and that just got messy.)

- The remaining 0.48% SFBs are `br` (not `rb`) and `rk` (not much `kr`), which
  are **_downward-overlap_ alts**, and are reasonable with ring-middle. That's
  important, and in in contrast to Colemak's _upward_ `rw` DSFB (where you
  have to shift or slide or use ring-pinky). The same is true on the
  right-hand with `ui` (Colemak is pretty good in with these too).

- Having a _few_ terrible patterns is ok so long as you have **magic**
  (left-thumb) workarounds (up to maybe 8): `any` (`a◊`), `back`, `why`, `one`
  (`u◊`), `ious`, `yeah`; and these apply nicely as composable chunks:
  `anyone` -> `a◊u◊`, `many` -> `ma◊`

- **LSB** (lateral) hand-shifting by one key is feasible: `MoVe` and `SySTEM` and
  `ONlY` move left-hand to the right one position, but it's easy enough with
  some practice; other examples: `MuST`, `tHEY` (and see many more below)

- The **LSB** (lateral) score of _0.95_ is misleading. I consider it closer to
  _0.2_ since almost all of it is due to the `yo` roll-stretch (and a little
  `ye`) which is same-row (and even less stretch on anatak).

- It's more **inward-rolly** than it looks. This is true of other layouts too,
  but Flowrist has a little more by design with `wh`. It also inherited a few
  from Colemak like `pt` (and `sc` is ok). Other decent ones are `mv`, `mp`,
  `tm`, `td`. I'd like to see layouts go further with the concept and design
  for columns 3 and 6 to have a lot more of these; slots `nh`, `td`, and even
  `pt` are missed opportunities!

- **Rolls** overall are way undercalculated. If you count `pt`, `sc`, `wh`,
  `mp`, you see another 8+%, bringing the actual total to well above 50%.

So if you take my interpretation of all that, you can _kinda_ say these are the
real numbers:

> - Sfb:  0.48% (on non-strength cols)
> - Dsfb: 1.29% (on non-strength cols)
> - Lsb:  0.19% (discounting same-row `y`)
> - Redirects:    4.24%
> - BadRedirects: 0.12%
> - Home keys usage: 64% (thanks to `ŋ`)
> - Total Rolls: 51%

The [Cyanophage Playground][1] gives the following _effort_ scores, with a few
advantageous tweaks for [Anatak][4], and doesn't count the adaptive `ŋ`:

> - Total Word Effort: 1032
> - Effort: 400

## Spatially tuned for code editors (Emacs and maybe others)

The most common code-editor command-letters are in strong and spatially
meaningful positions. Vim is completely ignored since it was built
specifically for qwerty and seems ridiculous to retrofit for better layouts
IMO (though modal editing with god-mode, meow, etc can be great). I found
layouts that put `n` (next) and `b` (back) and other repeatables on pinky were
taxing it (graphite, gallium, engram, carbyne, beakl).

Notice that the `bf` pairing is spatially reflective of _back/forward_. Same
with other pairings: `pn` for _prev/next_. `ywh` for _yank/save/select_.
`ae` for _start/end_ (though backwards). `sr` for _search/reverse_. `xv` for
_cut/paste_ (but macros preferred). `SPC` and `BSPC` for next/prev page etc.

Other happy accident pairs: `y/n` — yes/no; `l/r` — left/right

## Adaptive n/h

This was a really fun discovery and borrowed directly from
[horn][7]'s QMK code. It runs on a 500 ms timer so that
normally typing `sŋ` is `sh` but if you wait half a second between strokes,
it's back to `sn`. This is important for editor sequences like `(C-x) C-s` to
save your buffer and then `C-ŋ` to go to _next_ line quickly becomes `C-n` (as
intended) and not `C-h`.

## Slots for combos (very rare pairs)

There are several two-key combos that when pressed simultaneously work well as
macros. Eg, I use `gk` as the `z` key. Here is my full set, but these should
be changed to suit your prefs.

- `gk` — `x`
- `gq` — copy-paste buffer menu
- `bf` — `C-TAB`
- `rl` — `TAB` (experimental since `eaRLy`
- `fp` — screenshot
- `cd` — `C-c`
- `jr` — `C-w` (close window, cut)
- `pv` — `C-v` (paste)
- `gm` — (but `seGMent`)
- `tm` —
- `td` —
- `lj` —
- `pj` —
- `.,` — `shift`
- `,-` — `backtick`
- `nh` —

## Less natural patterns for practice (for no D/SFBs!)

Every layout will have some challenging patterns. I want them to be well known
so that they can be practiced. The fastest typists in the world mostly still
use Qwerty, and they do that by constantly shifting and contorting their hands
to avoid SFBs. Flowrist was designed to turn the tort into comfortable
overlaps and minor shifts.

This section contains most of those patterns I've adopted, and is more for
future reference. If you find yourself ever slow (sliding) on a D/SFB, refer
to this. The `imrp` are for fingers: `i`ndex, `m`iddle, `r`ing, `p`inky. A `.`
means _uninteresting_.

Eg, although many folks may be comfortable with the `ho` index-middle (`im`)
stretch-reach, I am generally not (except maybe the `hou` case), so it is
usually _index-ring_ (which leaves _middle_ open for `n`). And _index-pinky_
for `hu`.

There are a few rare cases where the `ŋ` will surprise you. Eg, `own` has to be
bare-`n` since the `wŋ` sequence needs to resolve as `wh`. So you'll want to
reach for `o` with _ring_ (to actually get a nice roll out of it).

- `thin`/`than` (same index for `n` and `h`)
- `own/sign/snow` (bare-n)
- `han` (`mpi`) (long pinky stretch)
- `rope` (`.m.i`)
- `open` (`r.mi`)
- `one` (`rim`) (or magic)
- `only` (`rm.i`) (hand-shift)
- `who/whe` (`mir`)
- `went` (`mri.`)
- `win/won` (`mri`)
- `with` (`mr.i`)
- `new/now` (`irm`)
- `home/hope/hose` (`ir.m`)
- `hun` (`ipm`)
- `people` (`.mr...`)
- `goes/does` (`.ri.`)
- `met` (`i.m`)
- `middle` (`i.m◊p.`)
- `time` (`m.i.`)
- `face` (`r.i.`)
- `fact/fect/sect` (`r.mi`)
- `exp/ext` (`.im`)
- `they` (`.mri`) (shift)
- `move` (`mimi`)
- `pit/pat/put/pet/pot/peat` (`m.i`) (`p` is often middle)
- `part` (`m.pi`) (very often!)
- `step` (`rmi`)
- `soft` (`m.ri`)
- `complete` (`m.imp...`)
- `vid` (`i.m`)
- `way` (`mpi`)
- `dev` (`m.i`)
- `show` (`.irm`)
- `simple` (`r.imp.`)
- `post` (`m.ri`)
- `hey` (`mri`)
- `they` (`.mri`) (home-`h`)
- `second` (`mmirii`)
- `stop` (`rim`)
- `most/must` (`irm`)
- `break` (`rm..i`) (if you wanna get crazy)
- `drop` (`ir.m`)
- `dep` (`i.m`)
- `ber` (`r.m`)
- `number` (`..ip.r`)
- `tod` (`m.i`)
- `empty` (hard!)
- `minu` (`.rip`)
- `himself` (`..i.mpr`) (hard!)
- `str` (terrible redirect from colemak!)
- `eco` (`m.r`)
- `leg` (`p.r`)
- `committee` (repeat practice)
- `quiet` (`.rmi.`) (or `qu◊et`)
- `techno` (`...ii.`)
- `note` (`ir.m`) (hard!)

And these are a few of the particularly challenging, and could be magic or
just slowly typed (or really interesting alts):

- `beyond`
- `moment`
- `board`
- `consider`

If you want to focus on practicing a given letter or two (`m` and `g` in this
example), here's a way (from a terminal) — grab a list of words and:

```
echo `grep '[mg]' top1000.lst | shuf`
```

Then paste those into monkeytype's _custom_ setting.

**Note on the left-thumb:** It takes quite a while to get used to using
a _regic_ key, even moreso when it's a new thumb. It took me a few weeks to
get comfortable.

## Fun new roll patterns somewhat unique to Flowrist

`au`, `bl`, `mp`, `wh`, `w/y/hou`, `ue`, `gr`, `ion`, `bj`, `fl`, `xp`, `xt`,
`ck`, `sm`, `sl`, `sk`, `lk`

Plus the usual Colemak goodies: `pt`, `sc`, `fr`

## Similarity to Colemak

```
      F P     y     u
    R S T       N E I
      C D V     H
```

I called `y` a similarity because you know it immediately from qwerty days.
`u` is a "minor" move.

If you want to keep it more similar to Colemak, or do a transitional, you can
do this, where the only 6 major moves are `wolavm`:

```
  Q k F P B   Y w o U
  l R S T G   j N E I a
  v X C D m   z H
```

## Magic config

Here are the fiddly/stretchy/logjammy (or very common) words from top-1000
that I feel are worth macro-ing via [repeat key][16]:

- `a` -> `any`
- `b` -> `behind`
- `'` -> `\bI'`
- `h` -> `how`
- `i` -> `ious`
- `j` -> `\bback` (that's a backspace to remove the `j`!)
- `q` -> `\bprob`
- `o` -> `one` (maybe, but `oo` is probably more important)
- `w` -> `why`
- `y` -> `yeah`

The rest are repeats (`◊e` is `ee`), and `v,k,z` are open for whatever you decide.

## Major Insights in Layout Design

Qwerty-G position (consonant hand only) is way undervalued. That reach feels
almost as good as home-row, and is a waste to put `g` there. So now `m` is
there.

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
Designers have considered `xcv` together but it can go a lot further. If
`hjkl` is such a thing for qwerty Vimmers, why don't we emphasize its approach
in a layout. I'm tempted to even swap `p` and `w` to get the `pn` spatial
`prev/next` (but I like the `wh` too much to try).

It is soooo hard for me to learn a new layout from scratch. It would take me
many months to really be up to speed. Trying Canary wasn't bad but Graphite
was unattainable. So pushing Qwertizens to something more Qwerty-like or
transitional will enable more folks to take a plunge.

It's not unreasonable to _use a combo as a key_. Using `gk` for `z` is working
well for me. So it might be ok to do it for any of `jxk` too.

I'm uncertain about _hand balance_ and if it matters a lot. The perfect letter at
Qwerty-H has big potential. Maybe that's a repeat-key. I have it as `Ctrl-c`
presently (for Emacs etc).

There are "chunks" out there with great potential for magic. I'm using `how`,
`any`, `one`, `prob`, and those are pretty good for Flowrist but there may be
opportunities here for other layouts.

_Rolls_ are great (though some prefer alternates, and they're great too of
course). However, to achieve really high rolls, you'd need to intermix vowels
and consonants on the hands. But this is so bad for redirects, so you have to
choose your tradeoff.

The optimizers we have available to us are incredibly powerful tools. And
there is room for other metrics and different ways to calculate what is
presently measured. My main conclusion is that there is enough uncertainty and
personal preference involved that probably the safest way to choose a layout
is simply using the one that hurts the least. For me, that means:

- finding the right SFBs on the stongest fingers, and using pinky and ring
  with the fewest contortions.
- choose the best stretches, and vowel-hand shouldn't stretch much; even qwerty
  did ok at that (on the right)

## More Flowrist design explanation

Placing `w` above `h` means that although `w` _looks_ like an index key (and
thus an common SFB), it's almost as commonly a middle-finger. You'll know by
looking/thinking ahead a couple letters for a `n` or `h`. This means index
stays busy only pressing `y`, `w`, and `n/h` (and sometimes `h` and `e`). And
that `wh` is a very nice inward roll (which analyzers won't detect) for a gain
of 3+%. Note also that `wh<vowel>` is always a redirect. However, it feels
fast and natural with a little practice.

**Vowels on the right**. Most sensible layouts have a vowel-hand to get fewer
redirects. This is why we have `w` and `h` on the right (as an inward roll);
`w` is a semi-vowel, and `h` is arguably [not totally a
consonant](https://linguistics.stackexchange.com/questions/4834/why-is-h-called-voiceless-vowel-phonetically-and-h-consonant-phonologically)
and thus works well on the vowel hand. So the exception is `n`. It's over
there for a couple reasons: tradition (so many will already be comfortable
with it); and it's the best _adaptive_ combo IMO. It's bad for redirects there
but a worthwhile compromise. I tried swapping it with `f` (and adaptive `fh`)
but it wasn't worth it with all the _left-middle_ SFBs on `n`.

**`g` on pinky**. There are D/SFBs with `g` and `l`, and the `gl` is terrible,
so it needs magic, at which point it's great. But I'm overall pleased with the
`g` location, particularly for the `gr` in-roll.

**`l` on pinky.** I haven't seen any other layouts that do this, but it feels
great and the stats are great — better than `c` or other possibilities I've
seen/tried for that spot.

**`y` is awkward**. It needs _magic_ for _any (a◊)_, _why_ (w◊), and _yeah_
(y◊), but is otherwise pretty good there, especially for `yo...`. And it's
familiar from Qwerty.

**Indexes are overloaded**. Yes `tpmvd` together result in 1.5% and 0.5% in
D/SFBs, but in practice almost all of their patterns work very well with some
practice on their _index-middle_ dances.

**Shortcuts left the left (non-mouse) hand**. Yeah, but there was no way `a`
could stay on left. `w` is the other unfortunate victim. Outside of Emacs, I
use triple-click more often now instead of `Ctrl-a`. And I QMK-mapped `jr`
combo to be `Ctrl-w`. And `bf` to be `Ctrl-Tab`. On the bright side, you now
have `Ctrl-l` on the left. And it does help to have a `Ctrl` on the right hand
too. You can probably re-bind some alternate on left-hand to handle the
missing shortcuts.

## What's really wrong with Colemak?

...and is it really worth switching? If you have the time and energy to switch
again, I do think it's worth it. Here are the major shortcomings I see with
Colemak:

- **Redirects are a killer.** The poster child is `you`. After a lot of
  practice, you can get fast at it, but my experience was that it will always
  be error-prone. It's especially bad to have redirects involving _ring_ and
  _pinky_. At 10.1% total and 1.47% "bad", it's really hard to not feel
  crippled by them (`you` is half of those bad ones btw). Flowrist gets them
  down to 4.2% total and 0.12% bad.

- **`m` on center-right-column causes LSBs.** `m` alone is a 1.5% LSB (and
  also 2% of redirects). It definitely doesn't belong anywhere near there. And
  as soon as you move it to left-hand, lots of other moves cascade. Flowrist
  takes LSBs down to 0.2% if you discount `y` with magic.

- **Not a real vowel hand.** `a` on left causes 2.2% more redirects and plainly
  makes the design chaotic (even if it was good for rolls). It also accounts
  for the other half of the bad ones.

All that said, Colemak is pretty/really good on: **Effort, SFBs, rolls, and
underloading rings and pinkies**. But even Qwerty is good on the underloading!

Applying _magic_ to Colemak may be a much simpler approach to solving its
shortcomings. I didn't discover magic until too late in the game (and so
haven't tried to invent the right patterns for it there), but that's a good
place to start, if you're not fully convinced that you need something new.

## So why not just use Canary?

As a Colemak variant, I wanted to make [Canary][6] work for me. It made some
good steps to reduce redirects, especially some bad ones, and SFBs are
fantastic. `crst` works well, and `g` is nice there, and `f` is good on
RHS. But here's what I couldn't live with:

- `m` could never work alongside `n` on right-hand. Way too much LSB and
  redirects from it.

- More divergent from Colemak than was necessary, especially in the core with
  `f` and `c` moving.

- `r` and `l` together on ring was breaking my wrist with the upward DSFBs.

- Reaching for `w` didn't suit my hand.

Side note: I originally hated the `one` pattern, but ended up with it in
Flowrist anyway, and decided that it was acceptable since I had a magic
workaround for it. But then I got used to it, and now don't feel that it's so
godawful.

## FAQs

- **Can I use this on a matrix keeb?** _Yes_

- **What about a normal keyboard?** _I think so, but right-hand will need a
  tweak to put `w` somewhere else; maybe on center-col-right-index or even
  right-pinky._

- **Do I need the adaptive `nh`?** _No, it'll work fine without, but you lose
  the crazy-high home-row stats._

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
