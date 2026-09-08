# Bundled fonts

Three families ship inside the APK, in `app-android/src/main/res/font/`. All three are licensed
under the **SIL Open Font Licence 1.1**, which permits bundling and redistribution inside an
application, including a commercial one, provided the fonts are not sold on their own and the
licence travels with them.

| File(s) | Family | Copyright | Source |
| --- | --- | --- | --- |
| `caprasimo_regular.ttf` | Caprasimo | Copyright the Caprasimo Project Authors | https://fonts.google.com/specimen/Caprasimo |
| `figtree_regular.ttf`, `figtree_semibold.ttf`, `figtree_bold.ttf`, `figtree_extrabold.ttf` | Figtree | Copyright the Figtree Project Authors | https://fonts.google.com/specimen/Figtree |
| `plex_mono_regular.ttf`, `plex_mono_medium.ttf` | IBM Plex Mono | Copyright IBM Corp. | https://fonts.google.com/specimen/IBM+Plex+Mono |

The licence text is identical for all three and is published with each family at the URLs above
(`OFL.txt` in each upstream repository).

**Why these three.** They are the faces the Honest Food design system specifies: Caprasimo as the single
display voice, Figtree for everything read as prose or pressed as a button, and IBM Plex Mono for
kickers and machine readings. Substituting a system face changes the app's character but not its
legibility — `HaloFonts` falls back to the platform families if these are ever removed.

**Why static cuts rather than variable files.** Only the weights the type scale actually names are
bundled (400/600/700/800 for Figtree, 400/500 for Plex Mono), which is smaller than the variable
files and avoids relying on `fontVariationSettings`, whose support varies below API 26.
