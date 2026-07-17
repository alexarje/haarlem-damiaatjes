# Eight hundred years of 9 pm: listening closely to Haarlem's Damiaatjes

Every evening at nine o'clock, two bells start ringing in the tower of the
Grote Kerk (St. Bavo) in Haarlem, and they keep going for exactly half an hour.
Standing in the city centre last night with an ambisonic recorder, I caught the
second half of this ritual — and then spent some time taking the recording
apart, strike by strike.

## The legend

The bells are called the
[*Damiaatjes*](https://en.wikipedia.org/wiki/Damiaatjes) — "little Damiettas."
The story goes back to the Fifth Crusade: in 1218–1219, crusaders besieged the
Egyptian harbour city of Damietta, whose port was closed off by a massive
chain. Haarlem's contribution, according to local legend, was decisive: a ship
fitted with a saw in its bow that cut straight through the chain. The city's
coat of arms carries a sword and stars said to commemorate the feat, and the
nightly ringing — originally the signal that the city gates were closing —
became a memorial to the Damietta heroes.

Historians are less romantic. The eyewitness account of Oliver of Cologne, who
chronicled the Dutch fleet, mentions no Haarlem saw-ship, and the
[Canon van Nederland](https://www.canonvannederland.nl/nl/noord-holland/haarlem/klokkengieter-verzon-mooi-verhaal)
tells the delicious version in which a sixteenth-century bell founder
embellished the legend to persuade the church to commission new bells. Sources
also disagree about the bells themselves — the Haarlem history site
[De Haarlemse Mug](https://www.haarlemsemug.nl/de-damiaatjes/) and others
circulate dates of 1562, 1564, and a 1732 recasting by J. A. de Grave.
Whatever the truth, the *practice* is real and continuous: the gates are long
gone, but in the tower of the
[Grote Kerk](https://en.wikipedia.org/wiki/Grote_Kerk,_Haarlem) the bells
still ring, every single night, 21:00–21:30. That makes them a textbook
example of what R. Murray Schafer called a *community soundmark* — a sound
that a community recognises as its own.

## Recording

I recorded with a Zoom H3-VR in AmbiX B-format (four channels, so the full 3D
sound field) from a street in the centre. A practical note for fellow
field-recordists: the recorder's clock turned out to be eleven minutes slow. I
could only tell because the bells stopped — the last strike, at file-time 21:06,
must have been 21:30:00. Church rituals make good clock references.

## Two bells, one clock

![Spectrogram of the ringing](analysis/spectrogram_excerpt.png)
*Thirty seconds of the ringing: each strike is a vertical attack followed by
long horizontal partial traces — two interleaved stacks, one per bell — over
the pink low-frequency carpet of evening traffic.*

The analysis (with my [ambiscape](https://github.com/fourMs/ambiscape) toolbox,
which grew a new `rhythm` module in the process) separates the two bells
cleanly by their partials:

- **Bell A** — hum 475 Hz, strike note around B♭5, with a partial series close
  to the classic minor-third bell profile (1 : 2 : 2.4 : 3 : 4).
- **Bell B** — hum 598 Hz, strike note around D6, with a flat prime and flat
  nominal: an older-sounding, less "tuned" profile.

Together they sound a slightly wide minor third, B♭–D. And they are *not*
equals rhythmically. The composite pattern repeats every **3.167 seconds**:
bell A strikes, 1.37 s later bell B answers, and after another 0.42 s bell A's
backswing strike lands — a long–short–long limp, B♭ … D–B♭, roughly 19 cycles
per minute, about 400 times over the half hour.

![The pattern: cycle clock and all 399 cycles](analysis/rhythm_pattern.png)
*The pattern at a glance. Left: one 3.167 s cycle as a clock — bell A's main
strike (filled blue), bell B (orange), A's backswing (hollow blue); the shaded
fans show timing jitter. Right: all 399 cycles stacked, one row each — the
first two columns bend in parallel (a shared, slowly wandering clock) while
the backswing column scatters on its own.*

Two things surprised me.

**First, the bells are phase-locked.** Over twenty minutes, bell B stays a
fixed 1.63 s behind bell A with a standard deviation of just *seven
milliseconds*. Two independently swinging bells could never hold that: their
pendulum periods would differ and the strikes would drift through each other.
These two behave as one mechanical system — a shared automated drive is the
likely explanation (though I confess I'd love it to be a Huygens-style
entrainment through the tower structure). The whole pattern's *tempo* does
wander — the cycle drifts by ±100 ms on a time scale of minutes — but the two
bells wander *together* (correlation 0.96 between their timing residuals).

**Second, the variation lives in one place.** Rhythm is repetition with
variation, and here the roles are cleanly split. Bell A's main strike and bell
B jitter by only ~30 ms from cycle to cycle — machine-tight (in circular
statistics: resultant length R ≈ 0.98 for each stream, and R = 0.998 for their
relative phase). Bell A's *backswing* strike is another story: 115 ms of
cycle-to-cycle jitter, and in about one cycle in eleven it fails to sound at
all. All the looseness, all the "life" in the pattern, comes from one clapper
bouncing on the backswing. The ringing is also tightest mid-bout: both the
start-up and the final minutes are audibly (and measurably, three times)
sloppier.

## The drone you don't notice

A bell is not just its strike. Bell A's hum partial rings for something like
seventeen seconds — five times longer than the gap between strikes. So for
thirty minutes, Haarlem's centre is bathed in a continuous B♭+D drone that
never decays, refreshed by each strike; the bright attack partials (which decay
in a second or two) just sparkle on top. In Schafer's terms the ringing turns
the whole city centre *lo-fi*: it masks the mid and high frequencies of
everything else. When the bells stop at 21:30, the soundscape drops by ~8 dB
and falls apart rhythmically — what remains is the slow, aperiodic breathing of
evening traffic, with modulations on time scales of six to forty seconds, and
the occasional close footstep or voice. The 3-second clock that had organised
the whole acoustic scene simply vanishes.

## Coda

The Damiaatjes have marked 9 pm for centuries. Listening closely, what they
broadcast is not just a time signal but a beautifully structured rhythm — a
3.167-second cycle, machine-locked yet humanised by one unruly clapper, riding
on a drone nobody consciously hears, dissolving at 21:30 into ordinary city
noise. Repetition with variation, every single night.

![Schafer soundscape timeline](analysis/schafer_timeline.png)
*The evening as a Schafer-style timeline: the two bell soundmarks and their
hum-drone keynote run to 21:30 sharp over the continuous traffic keynote; the
grey ticks afterwards are the close transients of the ordinary evening street.*

*Recording and analysis details: 4-channel AmbiX, Zoom H3-VR, 48 kHz/24-bit;
analysis with [ambiscape](https://github.com/fourMs/ambiscape)
(analyze / rhythm / taxonomy / iso). Figures and the full technical report are
in the session folder; the trimmed recording is on Freesound.*
