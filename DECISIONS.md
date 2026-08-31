# Decisions

One or two lines each. Newest at the bottom.

**Aug 2026 — Sprinters only, 100/200/400.** Not the whole track team. Distance,
throws, jumps and hurdles need completely different programming, and trying to
serve everyone would have made the app useless to everyone.

**Aug 2026 — Coach posts, athletes read.** The first version asked athletes what
their last session was and let them pick the day's focus. They don't know those
things, and they shouldn't have to. Coaching decisions moved behind a "Coach"
toggle; the athlete screen is read-only.

**Aug 2026 — No training jargon anywhere an athlete reads.** "Max velocity"
became "Top speed." "Extensive tempo" became "Easy day." "Set to a 10% velocity
decrement" became "set light — you should barely feel it slowing you." The
coaching science is unchanged; only the words are.

**Aug 2026 — The school logo goes in as a file, not a redraw.** Tracing the
Panthers mark into code would be making a copy of the district's property.
The app loads the actual image file instead.

**Aug 2026 — Website, not an app store app.** The coach wants to text a link.
The App Store means developer accounts ($99/year for Apple), review queues, and
a week of waiting for every change. A web link is free, instant, and can still
be added to a phone's home screen where it looks and opens like a real app.

**Aug 2026 — No build tools.** The whole app is one `index.html` file that runs
straight in a browser. Slightly slower to load, but it means no Node, no npm, no
install steps, and the whole project can be dragged into a hosting site as a
folder. Correct tradeoff for a 15-athlete app maintained by a coach.

**Aug 2026 — Ship without board sync, add it next.** Getting a working link into
kids' hands this week beats a perfect app in three weeks. Sync is the only thing
missing and it's an isolated change.

**Aug 2026 — GitHub Pages for hosting.** Matches how the other training tools in
this account are published, so there's one place to find everything and one
workflow to remember. Requires a public repo, which is fine for workout content
but does mean the logo file is publicly downloadable.

**Aug 2026 — No CDN, nothing loaded from the internet.** The first hosted build
went blank on GitHub Pages. It relied on three files from unpkg, one of which
was a 3MB compiler that turned the code into something browsers understand,
every single time the page opened. Now that conversion happens once, ahead of
time, and React is bundled directly into `index.html`. The page needs nothing
but itself. It's a 600KB file, which is fine, and it works on bad track wifi.

**Aug 2026 — The app says what broke.** If it ever fails to start it now prints
the error on screen instead of showing a blank page.
