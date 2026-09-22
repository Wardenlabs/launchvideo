# Warden launch film

The launch video for [Warden](https://github.com/Wardenlabs/warden), built as a
[HyperFrames](https://hyperframes.heygen.com) composition: HTML + GSAP, rendered
to MP4. Eight frames, no cuts, light mode throughout, all copy in English.

## Where the state lives

- `STORYBOARD.md` — the film, frame by frame, and a dated log of every change
  and every idea that was tried and rejected. **Read the "Changes from" log
  before proposing something**; most obvious ideas have already been built,
  watched and cut, and the log says why.
- `BRIEF.md` — the original brief. Where it disagrees with the storyboard, the
  storyboard wins.
- `frame.md` — the design spec: palette, type, components, and the Figma nodes
  they come from. The design system is Figma's, not the product's CSS.
- `index.html` — the timeline: one entry per frame, start and duration. Frames
  overlap by 0.6s and sit under the previous one, so changing one frame's
  length moves every start after it.
- `compositions/frames/NN-*.html` — one file per frame.

## Working on it

```bash
npm run check                          # validate the composition
npx hyperframes@0.8.57 snapshot --at 9.5,12.9 --no-end   # stills at given seconds
npm run dev                            # Studio preview on localhost:3002
npm run render                         # full MP4 into renders/ (slow)
```

Verify a change with `check` and snapshots of the frames you touched. Don't
render the whole film for every change.

`renders/`, `snapshots/` and `.thumbnails/` are gitignored: they are output,
not source.

## Rules the film follows

- Statements are five words or fewer and never repeat what a component already
  shows. Fragments, not whole screens.
- Colour means a verdict (mint allowed, yellow held, red blocked) or the
  employee's send button (orange). Everything else is greyscale.
- No accuracy numbers, no third-party logos or vendor names, hooks not claimed
  verified, nothing dark.
- Entrances `expo.out` / `power4.out`, exits `power4.in`, camera `power4.inOut`,
  stillness before every snap.
