# honestfood.app

The one-page site for **Honest Food**, and the privacy policy Google Play links to.

Served by GitHub Pages from `main`, at the domain in `CNAME`.

## privacy.html is generated — do not edit it here

It is rendered from `core/ui/.../LegalText.kt` in the app repository, which is the same source the
app itself displays. That is the point: a privacy policy exists in two places, and the day the two
disagree one of them is a false statement about what the app does. The web copy is the one a
regulator reads; the in-app copy is the one a user reads. Neither may be the stale one.

To change the policy, edit the Kotlin, then:

```
./gradlew :core:ui:jvmTest --tests "*PrivacyPageTest*" -Phalo.site=render
```

and copy `site/` here. An ordinary test run compares the two and fails if they have drifted, so
forgetting to publish is a red build rather than a website quietly describing an older app.

`index.html` and `style.css` are written by hand and belong to this repository.
