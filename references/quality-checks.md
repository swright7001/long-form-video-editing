# Quality checks

Validate the actual render, not just the edit record or source footage.

## Machine checks

Probe stream presence, codec, displayed dimensions, frame rate, pixel/color metadata, sample rate, channel layout, duration and start times. Decode the render to detect corrupt frames/packets. Compare duration against the timeline with a tolerance derived from frame and audio packet granularity; investigate a larger discrepancy. Check final audio loudness and true peak against the selected target. Missing audio is acceptable only when intended.

Validate all caption and overlay time bounds. Check source hashes remain unchanged when source preservation needs verification. Verify every requested export and sidecar exists, is nonempty, and corresponds to the intended timeline version.

## Audiovisual review

Review opening, ending, each new graphic/caption treatment, crop changes, uncertain transcript regions and every risky speech splice. For short clips, play the complete output when possible. For long episodes, run machine checks across the whole file and sample throughout, including beginning/end for sync drift; disclose that playback was sampled. Inspect cut boundaries in short rendered windows. Contact sheets and waveforms help locate issues but cannot prove audio is free of clicks or that the edit preserves meaning.

Check for clipped syllables, unnatural pauses, lip-sync errors, abrupt room-tone changes, pumping noise reduction, overpowering music, and missing reactions. Check blank/duplicate/frozen frames, damaged transitions, incorrect orientation, awkward speaker crops and mismatched skin tones. Read captions at delivery size and verify they do not obscure faces, UI, lower thirds or expected platform controls. Confirm overlays begin at their intended frame and remain readable long enough.

For podcast clips, check the retained statement against surrounding source context. For product videos, ensure cuts and graphics do not imply unsupported capabilities. Verify names, numbers and branded wording in both captions and graphics.

## Status language

Record exact checks and sampled time ranges in `qc.md`. Distinguish `draft`, `verified export`, and `needs review`. If hearing or full playback was unavailable, say so; do not claim that ffprobe or images verified audio quality. Keep failed exports clearly labeled and preserve useful diagnostics. Handoff should link the requested files and identify any remaining review needed without claiming publishing occurred.
