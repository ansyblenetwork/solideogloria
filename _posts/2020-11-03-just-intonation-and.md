---
title: "Just intonation and ordering the intervals by consonance"
---

Previously, we discussed why there are at least [twelve notes]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of %}) in Western music, and why they [suffice]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}). In a nutshell, the selection of twelve notes prioritizes the ability to play perfect fifths, and the choice of temperament compromises this with the ability to play other consonant intervals.

Today, we look for such consonances approximated by these 12 notes. Not all 12 intervals will be consonant: This corresponds with the fact that slamming a piano with random notes does not sound good, and why despite enormous combinatorial possibilities, simultaneous notes in classical music almost always stem from canonical chords and triads.

### Justifying the intervals

Recall that we have 12 notes corresponding to the following wavelengths, derived from successive extension by perfect fifths:

$$\frac{2}{3}, \frac{2^3}{3^2}, \frac{2^4}{3^3}, \frac{2^6}{3^4}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{2^{12}}{3^8}, \frac{2^{14}}{3^9}, \frac{2^{15}}{3^{10}}, \frac{2^{17}}{3^{11}}, \frac{2^{19}}{3^{12}}.$$

Here, by choosing the numerators to be appropriate powers of 2, we have used the octave equivalents with wavelength between 1/2 and 1, lying within an octave above the root note. We perform successive approximations which justify the intervals:

1) Recall the approximations for the major third and closing the circle of fifths, respectively:

$$\frac{4}{5} \approx \frac{2^6}{3^4}, \qquad 1 \approx \frac{2^{19}}{3^{12}}.$$

We implement these approximations in our list of notes, keeping in mind this also provides approximations for inversions:

$$\frac{2}{3}, \frac{8}{9}, \frac{2^4}{3^3}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{5}{8}, \frac{3^3}{2^5}, \frac{9}{16}, \frac{3}{4}, 1.$$

2) Recall the last member of our list of [small integer ratios]({{ "" | relative_url }}{% post_url 2020-11-01-the-circle-of %}), 3/5. This corresponds to a major sixth and has the approximation

$$\frac{3}{5} \approx \frac{2^4}{3^3}.$$

We implement this and its inversion:

$$\frac{2}{3}, \frac{8}{9}, \frac{3}{5}, \frac{4}{5}, \frac{2^7}{3^5}, \frac{2^9}{3^6}, \frac{2^{11}}{3^7}, \frac{5}{8}, \frac{5}{6}, \frac{9}{16}, \frac{3}{4}, 1.$$

3) The remaining intervals may be viewed as dissonant, since they do not come naturally from our list of small integer ratios. Still, we may mildly temper three of them with the approximations

$$\frac{8}{15} \approx \frac{2^7}{3^5},$$

where the ratio 8/15 corresponds to a major seventh. Implementing this and its inversion, we have

$$\frac{2}{3}, \frac{8}{9}, \frac{3}{5}, \frac{4}{5}, \frac{8}{15}, \frac{32}{45}, \frac{15}{16}, \frac{5}{8}, \frac{5}{6}, \frac{9}{16}, \frac{3}{4}, 1.$$

### Ordering by consonance

We list our final set of wavelengths, which are the wavelengths used in _just intonation_:

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 8/9 | major second (inversion of minor seventh)  |
| 3/5 | major sixth (inversion of minor third) |
| 4/5 | major third (inversion of minor sixth) |
| 8/15 | major seventh (inversion of minor second) |
| 32/45 | diminished fifth (inversion of itself) |
| 15/16 | minor second (inversion of major seventh) |
| 5/8 | minor sixth (inversion of major third) |
| 5/6 | minor third (inversion of major sixth) |
| 9/16 | minor seventh (inversion of major second) |
| 3/4 | perfect fourth (inversion of perfect fifth) |
| 1/2 | octave |

In modern music, these wavelengths are only approximate due to [equal temperament]({{ "" | relative_url }}{% post_url 2020-11-02-temperament-compromising-consonances %}), but this analysis explains why and how we can order the intervals by consonance:

| Wavelength | Name |
| ------------- | ------------- |
| 2/3 | perfect fifth (inversion of perfect fourth) |
| 4/5 | major third (inversion of minor sixth) |
| 3/5 | major sixth (inversion of minor third) |
| 8/9 | major second (inversion of minor seventh) |
| 8/15 | major seventh (inversion of minor second) |
| 32/45 | diminished fifth (inversion of itself) |

The first row consists of the perfect consonances, the next two consist of imperfect consonances, and the last two consist of dissonances. The 8/9 ratio and its inversion, which did not come from the small integer ratios, depends on which resource you consult. Wikipedia lists it as consonant with a "citation needed" caveat.
<div id="controller1"></div>
<script>	
makeInteractive("controller1",`
X:1
K:C
Q:1/4=60
CG[CG]2|CE[CE]2|CA[CA]2|CD[CD]2|CB[CB]2|C_G[C_G]2|
`);	
</script>
