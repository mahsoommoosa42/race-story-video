---
name: race-story-video
description: >-
  Create or revise portrait racing highlight videos from onboard or track footage with selectable editorial themes, preserved widescreen action, restrained captions, and patient setup-to-outcome storytelling. Defaults to the black/red/white Race_P5_Final_Flag style. Use for race recap edits and matching this reference, not driving analysis or unrelated video styles.
---

# Race Story Video

Make the race understandable before making it short. Default to the supplied reference's editorial style; the current user's brief overrides these defaults.

Read [the style reference](references/style.md) and inspect its linked stills before designing. They document the actual reference, not a requirement to reuse its race facts.

## Choose a theme

Use [the theme options](references/themes.md) to select Trackside Red (default), Heritage Ivory, Night Telemetry, British Racing, or Monochrome Journal. Honor an explicit choice. Otherwise retain an established project theme; for a new project briefly present the options and proceed with Trackside Red if no preference is given. Theme selection must not block media inspection or story planning.

Themes change colour, typography and graphic treatment, not the race facts, chronology or pacing rules. Keep one theme consistent throughout a video. Record its name and any overrides in the working manifest. For a theme-only revision, preserve footage, cut points, caption timings and audio unless separately asked to change them.

## Establish the story

- Check Mem for the relevant race/project and latest corrections when available. Use one project collection and record meaningful decisions and delivered versions. Current user corrections override older notes. Do not assume a prior edit was accepted merely because it was delivered.
- Inspect supplied media, durations, dimensions, frame rates and audio. Build a source inventory and a short edit decision table: source file, source in/out, event, evidence, caption intervals and output start. Watch candidate moves with their approach and exit, not isolated screenshots alone.
- Distinguish confirmed facts from editorial observations. Confirm important missing chronology, finish position or ambiguous incident attribution; meanwhile continue media inspection. Export timestamps and filenames do not prove race order. Do not invent lap numbers, positions, passes or reasons a move succeeded.
- Give a concise proposed story before an expensive first render. This is not an extra approval gate when the user has already authorized creation and supplied enough context.

## Cut for comprehension

- Preserve setup, manoeuvre and aftermath as a continuous real-time shot where possible. Start early enough to establish the cars and gap; end after the outcome and settling phase. Review each exit in motion. Do not cut at the instant of a pass or recovery merely to shorten runtime.
- Let useful action determine duration unless the user gives a hard limit. If a limit conflicts with clarity, remove a lower-priority event rather than truncate every event. Do not inherit the reference's exact runtime.
- Use simple cuts and original speed by default. No artificial freeze, slow motion, speed ramps or invented footage to compensate for missing coverage.
- Introduce the situation before the move. Reveal outcome captions only after the visible outcome. Keep captions concise, factual and spatially helpful. Avoid technical causal claims unsupported by the user or evidence.
- Use the actual finish/flag crossing when supplied, then let the footage continue under the result graphic. If unavailable, say so and use a truthful alternative rather than substituting a start sequence or fake crossing.

## Compose and render

- Default to 1080 x 1920 portrait, retaining the full landscape action across the width. Follow the reference geometry and hierarchy with the selected theme's palette and typography. Keep graphics outside the footage and legible at phone size. Use no driver name or dramatic title unless requested.
- Keep synced original car audio. Default to no embedded music; the reference was prepared for music added separately. A historical song choice is not a standing soundtrack instruction. If music is requested, establish the supplied/authorized track and mix so race sound remains useful.
- Use available FFmpeg or an appropriate editor; prefer existing tools over a new rendering framework. FFmpeg may be available through Python's `imageio_ffmpeg.get_ffmpeg_exe()` when absent from PATH. Preserve originals and render to new files.
- Keep source-based caption anchors: after changing an in-point, recompute output caption time from the source event time, rather than leaving captions at old clip-relative times. Recompute all later sequence timings and music cues after trims. Clamp titles to retained footage.
- For resource-heavy renders, encode sections sequentially with identical dimensions, frame rate, codecs and audio settings, then concatenate. Check continuity and stream duration at joins. Deliver H.264/yuv420p MP4 with AAC audio and fast-start metadata unless another format is requested.
- Retain a small editable timeline/manifest and caption text alongside the project working files. Offer an editing handoff only if requested; do not call a media kit a native editable project. In particular, FCPXML is not a native Final Cut Pro for iPad project.

## Completion checks

Fully decode the export, confirm expected duration/frame count and matching audio/video duration, and inspect every caption state plus the first and last frames. Review each cut with several seconds on both sides in motion; listen for sync, clipping and abrupt audio joins when playback is available. Check captions never anticipate a result or survive into the wrong event, and that side-by-side action remains visible.

Deliver the actual playable MP4 and state material verification limits. A plan or storyboard alone does not finish a video creation request. Save the current version, user corrections and obsolete timing cues in the project record. Publishing or uploading publicly is separate from rendering.
