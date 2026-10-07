# Reference decomposition and implementation

## Observed references
IMG_2273 2.jpg and IMG_2307.PNG show the same visual idea across different clothing and playlists. One is a finished photograph, the other a screenshot with Instagram chrome: do not render status bars, account text, likes or comments into the generated photograph.

The visual anchor is a strongly foreshortened extended hand close to camera; the torso/face lies behind and is softer. The foreground hand carries rings in these references, but rings are source details, not effect requirements. The first composition appears to have an open palm plus a second upright hand: preserve the actual anatomy of a new source instead of forcing this configuration. Cards form a loose fan of diagonal planes: large left/right cards beside the hand, a larger cropped diagonal at lower left, and small receding cards below. Some lettering disappears naturally behind fingers. The cards' similar UI establishes a family while different cover art, scale and tilt provide rhythm.

Their transparent charcoal surfaces, fine light rim and white icons resemble compact system music widgets. Cover art sits left, metadata/control/progress sit right or below according to available size. Near cards can extend beyond the photo. This is a design observation, not proof of the original editor, layers or generation method. Do not promise a live player, Spotify/Apple integration or actual AR from a static collage.

## Shooting guidance
Ask a friend to shoot vertically, preferably normal 1x rather than extreme wide-angle distortion, slightly above eye level if comfortable. Extend one hand toward the lens with fingers relaxed and separated; keep the other hand farther back or naturally supporting it. Leave space left/right and below. Focus on the close hand; let the face be a little softer naturally. Keep the fingertip, palm and wrist within frame. A plain wall/door is convenient but not required. Avoid motion blur that destroys finger edges and strong light that blows the skin out. A new source need not duplicate the exact pose.

## Customization specification
Collect a run-specific record:
- Source image and output ratio (default source ratio).
- Each card: exact title, artist, verified cover file/URL and cover mode (supplied / official / original), optional secondary label.
- Main versus secondary card ordering. Optional count, theme tint, progress fraction and time fields.
- Approved occluders: which real fingers, palm, wrist or clothing sit in front; layout chosen from photo geometry.

A user can supply several songs, one album, or one song. Artwork may be a user's own picture when requested, but identify it as a custom cover. If the user wants genuine Apple/Spotify UI assets or exact screenshot reproduction, use supplied/correctly sourced components rather than claiming invented icons are official.

## Card asset method
Create a flat card face first using SVG or HTML: rounded background, subtle rim, supplied artwork with crop, exact Unicode title/artist and vector controls. Use a CJK-capable font for Chinese, measure available line length, shorten only with user approval or ellipsis that preserves supplied source data. Never squeeze text so small it cannot be read. Transport icons are balanced within the content column; do not place controls over the cover. Secondary small cards may omit minor metadata to reduce clutter, with no invented text.

Then transform the ENTIRE card with a projective transform into its assigned photo plane. Rounded corners and cover rectangle must share this perspective. Adjust far-card softness and translucency independently; no common huge drop shadow for floating objects. Card planes may differ in angle but must belong to a plausible camera scene. For precise typography, generate atmosphere/effect staging separately from actual card typography instead of trusting model-drawn letters.

Compose around the protected original hand. Restore only the required original occluders above particular cards; do not use an all-person silhouette that destroys intentional foreground cards. Contact edges around fingertips should be clean; avoid bright cutout outlines, glass passing through flesh, and card borders jumping in front and behind the same finger. Maintain the original scene exposure and color. A thin rim/highlight sells the interface; avoid excessive glow or plastic extrusion.

## Review stages
1. Confirm song/cover input and source suitability, with a brief planned fan direction and overlap map.
2. Produce one aesthetic preview. Check hand anatomy, card hierarchy, metadata and cover integrity; disclose model changes if present.
3. Apply the user's narrow correction, then recheck only affected relationships plus obvious regressions.
4. Exact-source delivery requires real compositing and a separate fidelity check; do not label an image-generated preview as pixel-locked.
