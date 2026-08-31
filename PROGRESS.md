# Progress

**Current phase: 4 of 6 — Build**

## Where things stand

The app is built and works. It runs as a single web page hosted on GitHub
Pages — no app store, no install, just a link. Athletes can add it to their
phone home screen and it opens full-screen like a normal app.
install, just a link. Athletes can add it to their phone's home screen and it
opens full-screen like a normal app.

### Done
- All four screens: Today, Week, Times, Race
- Sessions written for 100m, 200m and 400m, adjusted for five times of year
- Coach mode: tap "Coach" in the header to edit any day and post notes
- Personal time log with automatic best times and easy-day pace
- Race splits for all three events, plus the 400 two-halves check
- Wenatchee purple (#4B1868) and gold (#EEBF00), sampled from the school logo
- Home screen icon built from the school logo

### Not done yet — this is the next session's job
**The shared coach board does not sync between phones.**

Right now every phone keeps its own copy. If the coach changes Tuesday, only
the coach's phone shows the change. Athletes see the default week for whatever
time of year is set.

Everything else works perfectly without this. It is worth shipping as-is,
letting the group use it for a week, and then adding sync.

## Resume point for the next chat

> "The app is live at https://USERNAME.github.io/panther-speed/. Time to make the coach board sync
> between phones."

The change is small and lives in one place: the `store` object at the top of
`index.html`, marked with a comment. Swapping it for a Supabase-backed version
is roughly 30 lines. Nothing else in the app has to change, because every part
of the app already talks to storage through that one object.

## Known issues

- **Coach mode isn't locked.** Any athlete can tap "Coach" and change the week.
  With a group of 15 this is probably fine. If it becomes a problem, a simple
  4-digit code is a 10-minute fix.
- **`index.html` is now compiled output.** It is one 600KB file with React built
  in and no internet dependencies. Don't hand-edit it — say what you want
  changed and it gets rebuilt from source.
- **Times are per-phone.** If an athlete gets a new phone, their logged times
  don't come with them.
