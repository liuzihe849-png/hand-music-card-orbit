---
name: hand-music-card-orbit
description: Turn a supplied outstretched-hand portrait into a floating personalized playlist collage with rounded music cards, accurate song and cover assets, hand occlusion and varied perspective depth. Use for hand-led music-card fashion photos rather than a single full-body player frame.
---

# Hand Music Card Orbit

Create a personalized playlist suspended around an outstretched hand. The hand is the depth anchor; cards are separate planes, not a flat UI wall. Read [references/design-and-production.md](references/design-and-production.md) before planning a composition.

## Fresh-chat reference loading

Before production, read [fresh-chat visual contract](references/fresh-chat-visual-contract.md), inspect the bundled visual reference. For a generative preview, pass it together with the new user source to the image-generation call; for deterministic production, follow the bundled composition/script route and preserve source pixels. Do not assume earlier chat images are visible to the generator. Use this package as the style source; treat custom fields and occlusion choices as per-photo inputs.

## Inputs
Distinguish the user's raw portrait from the finished style references. Preserve source identity, actual fingers, rings, pose, clothes, crop, scene and photographic light. Do not import the reference model, door, pink shirt or jewelry. Do not reconstruct a missing face or change a hand into the reference gesture.

Before image production collect missing items in one concise question: photo, song-title/artist pairs (or one song if requested), cover choice, and any requested card color or secondary label. Reuse provided values; never ask again for a confirmed song. Song lists belong to this run, not Skill defaults. Suggest 3–5 cards when the user has no count preference, adapting to source space; do not fabricate extra songs to reach that count. If only one song is supplied, offer a single-card layout or ask whether variants of that song are desired.

Cover choices: user-supplied album artwork; verified official artwork found online; or explicitly requested original/custom image such as their own photo. Identify which choice was used. Never generate a lookalike album cover and label it authentic. If retrieval fails, request the asset or offer an original cover; do not silently substitute. Exact music title, artist and cover are production data. Do not add lyrics, invented duration, explicit-content badge, official-service claims or a playback connection without supporting input. Progress/times are optional visual fields and must be supplied or explicitly treated as illustrative.

## Source suitability
For a new shoot suggest a clear outstretched hand toward camera, relaxed spread fingers, torso farther back and available space beside the hand. No exact gesture, jewelry or background is mandatory. Hand anatomy and natural depth matter more than matching the pose. Use an existing unsuitable photo only with an adapted layout; explain when the signature hand-interaction effect cannot be achieved without a new source. Never invent fingers to fit cards. Preserve sharpness already in the source; do not globally blur the person.

## Composition
Use the real hand position as origin. Main cards fan irregularly outward behind selected fingers, with smaller cards receding below or beside the hand. Vary scale, tilt and projective perspective; use cropped near cards only where the source has room. Avoid fixed symmetry, identical card sizes, stacks on a common flat plane, and obligatory five-card layouts. Keep source face and main palm readable.

Cards are landscape rounded rectangles with a dark neutral translucent panel, restrained thin rim, square rounded cover at one end, title/artist beside it, a balanced transport row and an optional progress line. A card may use a subtle cover-derived tint. Avoid thick glossy 3D slabs or glowing neon. All card content undergoes the SAME perspective transform, including cover, typography, controls and rounded edge; never rotate the text independently.

Occlusion is deliberate: source background/body -> assigned cards -> original finger/palm masks -> selected near cards only outside important hand/face regions. Review every visible finger boundary. A card can pass behind a finger or beside the hand; it must not slice through a finger or arbitrarily erase jewelry. No forced card insertion between fingers when the source has no visible gap. No universal requirement to restore the entire person over every card.

## Production and review
For analysis/Skill creation, deliver decomposition and usable Skill files only. For a requested test, explain the source-specific card arrangement, produce ONE preview with an available image-generation tool, inspect it and stop for human review.

A generated full-photo edit is an aesthetic preview, not proof of source-pixel or text/cover fidelity. For exact delivery, construct card faces with deterministic SVG/HTML typography and real supplied artwork, then use an available compositing workflow to apply perspective, source-hand masks and restrained depth blur. Obtain explicit authorization if a tool choice requires new paid services. Do not claim deterministic compositing was performed when only an image-generation edit exists.

Check: recognizable source; intact fingers/rings; precise requested title/artist; matching cover choice; cover/control/text alignment; coherent perspective and hand occlusion; varied depth without UI clutter; credible daylight; one reviewable output. Structural Skill validation does not establish aesthetic approval. Subsequent corrections change only the named region/property and preserve established occlusion elsewhere.

## Author and public reference

Created and maintained by **理智画** (GitHub: [liuzihe849-png](https://github.com/liuzihe849-png)). Inspect [the original sample](assets/reference-original.png) and read [sample scope and limitations](references/public-sample.md). The sample is a visual aid, not a user identity or proof of exact fidelity. Do not copy sample-specific defects into new outputs.
