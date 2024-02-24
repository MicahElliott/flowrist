# Flowrist (fLowRiST, Technogrok, Grokkable, GeeKCoDe, gkcd)

Flowrist is a keyboard layout that focuses on offloading pinkies, minimizing
redirects and stretching (low LSBs, AKA lateral movement), and the easiest
possible (though high) SFBs. It is designed to be easy to transition to from
Colemak(-DH) with only ~10 (mostly lower-freq) keys moving. One could also
transition from QWERTY with ~13 moves (see section below for intermediate
layout). The intentionally high SFBs are almost all middle-index finger
overlaps, and applying the overlap technique actually brings the elbows
outward into a more natural wrist position.

There is a sample implementation for QMK.

```
√ j b f p x   y w o u '
  l r s t m    nh e i a
q g k c d v   n h / . ,
       ◊ ⇑  z  ⇐ _
```

It's really designed to be used with a reverse-symmetric-stagger keyboard as:

```
\   j b f p x  \    /  y w o u ' /
 \   l r s t m  \  /    ŋ e i a /
  \ q g k c d v  \/  n h / . , /
           ◊ ⇑    z   ⇐ _
```

_(It has been tried on a matrix-style keyboard and still felt good, but needs
much more trial.)_

There some novelties here:

- `q` is an extra pinky key instead of `shift` (`v` or `m` also work there but busy pinkies)
- `ŋ` (`nh`) is an _adaptive_ key, defaulting to `n`, but `h` after other letters
- bare-`h` is still convenient since you need it for words that start with `h`
- bare-`n` exists because there is a rare need for it for words like `sign`
- all the vowels and semi-vowels (`yw`) are on the right hand (only 8 letters!)
- `◊` is the "regic" (repeat/magic) key that does repeats for some (most) and
  magic (multi-letter macros) for others (a few)
- this isn't great for SFBs according to the analyzers, but it's tuned for a
  reverse-symmetric-stagger keyboard where SFBs can be good
- the `z` I end up using is actually a `gk` combo

Caveat about the designer: I am not a speedy typist; have only gotten to 100
wpm on qwerty, same on Colemak, and typically only take my own designs to 60
before getting distracted and making more changes. It's taken me ~5
significant iterations over 6 months to arrive at _Flowrist_. After a few
weeks on Flowrist I have had some bursts to 120, and that feels promising.

## Defying the analyzers

[Oxey's Layout Playground][3] gives roughly the following scores:

> - Sfb:  1.94%
> - Dsfb: 7.52%
> - Lsb:  0.95%
> - Redirects:    4.24%
> - BadRedirects: 0.12%
> - Home keys usage: 64%
> - Total Rolls: 44.7%

Some of those look not great at all, and in some ways actually worse than
Colemak so WTF. However, I don't think they tell the real story:

- If you discount the index and middle SFBs, you have this:
  > - Sfb:  0.48%
  > - Dsfb: 1.29%

- **Redirects** at _4.2_ sounds suboptimal due to the `n` on right-hand, but actually
  _feels_ ok with index: ∴ `n` on vowel-hand is ok only if index (and many
  layouts have done this). Compare this to Colemak's 10.5% and Qwerty's 13.2%.

- You could get _redirects_ down to almost nothing if you move the `nh` to
  thumb. I didn't find that worth it since redirects with index are not too
  detrimental IME. Otherwise, redirects are VERY good at 1%! But do note that
  redirects in general are something to really avoid as much as possible and
  an important decision. Try typing `stretch` on Colemak an realize the
  slowness of your left hand changing direction 3 times.

- **SFBs** are almost completely on the four "strength columns" and so mostly fine
  with index and middle (particularly with anatak). Qwerty and Colemak are
  both actually good at this too (but see next point). (I tried going up to 3
  SFBs there and that just got messy.)

- The remaining 0.48% SFBs are `br` (not `rb`) and `rk` (not much `kr`), which
  are _downward-overlap_ alts, and are reasonable with ring-middle (though I
  magic them). That's important, and in in contrast to Colemak's _upward_ `rw`
  DSFB (where you have to shift or slide or use ring-pinky). The same is true
  on the right-hand with `ui` (Colemak is pretty good in with these too).

- Having a _few_ terrible patterns is ok so long as you have **magic**
  (left-thumb) workarounds (up to maybe 8): `any` (`a◊`), `back`, `why`, `one`
  (`u◊`), `ious`, `yeah`; and these apply nicely as composable chunks:
  `anyone` -> `a◊u◊`, `many` -> `ma◊`

- **LSB** (lateral) hand-shifting by one key is feasible: `MoVe` and `SySTEM` and
  `only` move left-hand to the right one position, but it's easy enough with
  some practice; other examples: `ONlY`, `MuST`, `tHEY`

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

> - Sfb:  0.48%
> - Dsfb: 1.29%
> - Lsb:  0.19%
> - Redirects:    4.24%
> - BadRedirects: 0.12%
> - Home keys usage: 64%
> - Total Rolls: 51%

The [Cyanophage Playground][1] gives the following _effort_ scores, with a few
advantageous tweaks for Anatak, and doesn't count the adaptive `ŋ`:

> - Total Word Effort: 1032
> - Effort: 400

## Spatially tuned for code editors (Emacs and maybe others)

The most common code-editor command-letters are in strong and spatially
meaningful positions. Vim is completely ignored since it was built
specifically for qwerty and seems ridiculous to retrofit IMO for better
layouts (though modal editing with god-mode, meow, etc can be great). I found
layouts that put `n` (next) and `b` (back) on pinky were taxing it.

Notice that the `bf` pairing is spatially reflective of _back/forward_. Same
with other pairings: `pn` for _prev/next_. `ywh` for _yank/save/select_.
`ae` for _start/end_ (though backwards). `sr` for _search/reverse_. `xv` for
_cut/paste_ (but macros preferred). `SPC` and `BSPC` for next/prev page etc.

Other happy accident pairs:

- `y/n` — yes/no
- `l/r` — left/right

## Adaptive n/h

This was a really fun discovery and borrowed directly from
[horn][7]'s QMK code. It runs on a 500 ms timer so that
normally typing `sŋ` is `sh` but if you wait half a second between strokes,
it's back to `sn`. This is important for editor sequences like `(C-x) C-s` to
save your buffer and then `C-ŋ` to go to _next_ line quickly becomes `C-n` (as
intended) and not `C-h`.

#### My biases

- I don't mind stertching into center-col to `m` position. It's way better
  than `v` or `g` spots, and `g` is better than `v`.

-

## Slots for combos (very rare pairs)

There are several two-key combos that when pressed simultaneously work well as
macros. Eg, I use `xk` as the `z` key. Here is my full set, but these should
be changed to suit your prefs.

- `xk` — `x`
- `xq` — copy-paste buffer menu
- `bf` — `C-TAB`
- `rl` — `TAB` (experimental since `eaRLy`
- `fp` — screenshot
- `cd` — `C-c`
- `jr` — `C-w` (close window, cut)
- `pv` — `C-v` (paste)
- `gm` — (but `seGMent`)
- `rx` —
- `td` —
- `lj` —
- `pj` —
- `.,` — `shift`
- `,-` — `backtick`
- `nh` —

## Less natural patterns for practice

Every layout will have some challenging patterns. I like them to be well known
so that they can be practiced. Eg, although many folks may be comfortable with
the `ho` stretch-reach, I am generally not (except maybe the `hou` case), so
it is usually _index-ring_. And _index-pinky_ for `hu`.

There are a couple cases where the `ŋ` will surprise you. `own` has to be
bare-`n` since the `wŋ` sequence needs to resolve as `wh`. So you'll want to
reach for `o` with _ring_ (to actually get a nice roll out of it).

This section contains most of the patterns I've adopted, and is more for
future reference. If you find yourself ever slow (sliding) on a D/SFB, refer
to this. The `imrp` are for fingers: `i`ndex, `m`iddle, `r`ing, `p`inky. A `.`
means _uninteresting_.

- `thin`/`than` (same index for `n` and `h`)
- `han` (`mpi`)
- `rope` (`.m.i`)
- `open` (`r.mi`)
- `only` (`rm.i`)
- `who/whe` (`mir`)
- `went` (`mri.`)
- `win/won` (`mri`)
- `with` (`mr.i`)
- `new/now` (`irm`)
- `home/hope/hose` (`ir.m`)
- `hun` (`ipm`)
- `people` (`.mr...`)
- `met` (`i.m`)
- `time` (`m.i.`)
- `fact/fect/sect` (`r.mi`)
- `exp/ext` (`.im`)
- `own`  (bare-n)
- `sign` (bare-n)
- `they` (`.mri`)
- `move` (`mimi`)
- `part` (`m.pi`)
- `step` (`rmi`)
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
- `beyond`
- `moment`
- `note`
- `board`
- `consider`

If you want to focus on practicing a given letter or two (`m` and `g` in this
example), here's a way (from a terminal) — grab a list of words and:

```
echo `grep '[mg]' top1000.lst | shuf`
```

Then paste those into monkeytype's _custom_ setting.

### Fun new roll patterns somewhat unique to Flowrist

`au`, `bl`, `mp`, `wh`, `w/y/hou`, `ue`, `gr`, `ion`, `bj`, `fl`, `xp`, `xt`,
`ck`, `sm`, `sl`

Plus the usual Colemak goodies: `pt`, `sc`, `fr`

### Similarity to Colemak

```
      F P     y     u
    R S T       N E I
      C D V     H
```

I called `y` a similarity because you know it immediately from qwerty days.
`u` is a "minor" move.

If you want to keep it more similar to Colemak, or do a transitional, you can
do this:

```
  Q k F P B   Y w o u
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
- `o` -> `one`
- `w` -> `why`
- `y` -> `yeah`

The rest are repeats, and `v,k,z` are open for whatever you decide.

## Major Insights in Layout Design

Qwerty-G position (consonant hand) is way undervalued. That reach feels almost
as good as home-row, and is a waste to put `g` there. So now `m` is there.

Some SFBs are not at all. The `wh` overlap is as good as any middle-index
usage, at least on a keyboard with the right slant. I can imagine a layout
with atrocious SFB score yet is very comfy. Even `mp` is really
(qwerty-)`gr`eat.

Adaptive keys (`nh`) are a game changer for home-row (thank you [horn][7]!).
They are slightly challenging since they waste a slot and require more choice.
But there's probably room for one more if there are two other letters that
complement/combine as well (besides `n`-vowel). Other candidates are `hf` and
`ir` and `m`-vowel, though the latter two will always be bad for redirects.

There is a balance between optimal typing and editor commands location.
Designers have considered `xcv` together but it can go a lot further. If
`hjkl` is such a thing for qwerty Vimmers, why don't we emphasize its approach
in a layout. I'm tempted to even swap `p` and `w` to get the `pn` spatial
`prev/next` (but I like the `wh` too much to try).

It is soooo hard for me to learn a new layout from scratch. It would take me
many months to really be up to speed. Trying Canary wasn't bad but Graphite
was unattainable. So pushing Qwertizens to something more Qwerty-like or
transitional will enable more folks to take a plunge.

It's not unreasonable to use a combo as a key. Using `xk` for `z` is working
well for me. So it might be ok to do it for `jxk` too.

I'm uncertain about hand balance and if it matters much. The perfect letter at
Qwerty-H has big potential. Maybe that's a repeat-key. I have it as `Ctrl-c`
presently.

There are "chunks" out there with great potential for magic. I'm using `how`,
`any`, `one`, `prob`, and those are pretty good for Flowrist but there may be
opportunities here for other layouts.

The optimizers we have available to us are incredibly powerful tools. And
there is room for many other metrics and different ways to calculate what is
presently measured. My main conclusion is that there is enough uncertainty and
personal preference involved that probably the safest way to choose a layout
is simply using the one that hurts the least. For me, that means:

- finding the right SFBs on the stongest fingers, and using pinky and ring
  with the fewest contortions.
- choose the best stretches and vowel-hand shouldn't stretch much; even qwerty
  did ok at that (on the right)

## More Flowrist design explanation

Placing `w` above `h` means that although `w` _looks_ like an index key (and
thus an common SFB), it's almost as commonly a middle-finger. You'll know by
looking/thinking ahead a couple letters for a `n` or `h`. This means index
stays busy only pressing `y`, `w`, and `n/h` (and sometimes `h` and `e`). And
that `wh` is a very nice inward roll (which analyzers won't detect) for a gain
of 3+%. Note also that `wh<vowel>` is always a redirect. However, it feels
fast and natural with a little practice.

**Vowels on the right**. Most sensible layouts do this to get fewer redirects.
This is why we have `w` and `h` on the right (as an inward roll). `w` is a
semi-vowel, and `h` is arguably [not totally a
consonant](https://linguistics.stackexchange.com/questions/4834/why-is-h-called-voiceless-vowel-phonetically-and-h-consonant-phonologically)
and thus works well on the vowel hand. So the exception is `n`. It's over
there for a couple reasons: tradition (so many will already be comfortable
with it); and it's the best _adaptive_ combo IMO. It's bad for redirects there
but a worthwhile compromise. I tried swapping it with `f` (and adaptive `fh`)
but it wasn't worth it with all the _left-middle_ SFBs.

**`g` on pinky**. There are D/SFBs with `g` and `l`, and the `gl` is terrible,
so it needs magic, at which point it's great. But I'm overall pleased with the
`g` location, particularly for the `gr` in-roll.

**`y` is awkward**. It needs _magic_ for _any (a◊)_, _why_ (w◊), and _yeah_
(y◊), but is otherwise pretty good there, especially for `yo...`. And it's
familiar from Qwerty.

**Indexes are overloaded**. Yes `tpmvd` together result in 1.5% and 0.5% in
D/SFBs, but in practice almost all of their patterns work very well with
_index-middle_ dances.

**Shortcuts left the left (non-mouse) hand**. Yeah, but there was no way `a`
could stay on left. `w` is the other unfortunate victim. I use triple-click
more often now instead of `Ctrl-a`. And I QMK-mapped `jr` combo to be
`Ctrl-w`. And `bf` to be `Ctrl-Tab`. On the bright side, you now have `l` on
the left.

## What's really wrong with Colemak?

...and is it really worth switching? I have to answer this to justify it for
myself. If you have the time to switch again, I do think it's worth it. Here
are the shortcomings I see with Colemak:

- **Redirects are a killer.** The poster child is `you`. After a few years,
  you can get fast at it, but my experience was that it will always be
  error-prone. It's especially bad to have redirects involving _ring_ and
  _pinky_. At 10.1% total and 1.47% "bad", it's really hard to not feel
  crippled by them. Flowrist gets them down to 4.2% and 0.12% respectively.

- **`m` on center-right-column causes LSBs.** `m` alone is a 1.5% LSB (and
  also 2% of redirects). It definitely doesn't belong anywhere near there. And
  as soon as you move it to left-hand, lots of other moves cascade. Flowrist
  takes LSBs down to 0.2% if you discount `y` with magic.

- **Not a real vowel hand.** `a` on right causes 2% more redirects and plainly
  makes the design chaotic (even if it was good for rolls).

All that said, Colemak is pretty/really good on: **Effort, SFBs, rolls, and
underloading rings and pinkies**. But even Qwerty is good on the underloading!

## FAQs

- **Can I use this on a matrix keeb?** _Yes_

- **What about a normal keyboard?** _I think so, but right-hand will need a
  tweak to put `w` somewhere else; maybe on center-col-right-index or even
  right-pinky._

- **Do I need the adaptive `nh`?** _No, it'll work fine without._

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