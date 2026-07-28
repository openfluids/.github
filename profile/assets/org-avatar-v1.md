# Org avatar v1

Asset: `profile/assets/org-avatar-v1.jpg` (1024x1024, 225 KB)

Tool/model: xAI Grok CLI, built-in `image_gen` tool.

## GitHub's constraints

From the [profile reference](https://docs.github.com/en/account-and-profile/reference/profile-reference):
PNG, JPG or GIF; **under 1 MB**; **smaller than 3000x3000**; **~500x500
recommended**. It must be square, and GitHub crops it to a **circle** in most
views.

This asset: 1024x1024 JPEG q95, 225 KB. Square, inside every limit, and large
enough to stay sharp on a retina org header while comfortably above the
recommended 500 px.

The previous avatar (`openfluids-avatar.png`, 1254x1254 PNG) was **1.76 MB**,
over GitHub's 1 MB limit.

## Design constraints that actually mattered

An avatar spends most of its life at 20-40 px in a contributor list or a commit
row, so it was designed for that first:

- One bold shape, centred, with thick well-separated arms. Fine detail vanishes
  below about 60 px.
- Everything important inside the inscribed circle, corners left as plain dark
  background, because the circle crop discards them.
- High contrast between the cyan arms and the near-black ground so the silhouette
  survives being shrunk.

Candidates were reviewed as circle-cropped thumbnails at 40 px and 20 px, not at
full size, since full size flatters everything.

## Prompt

```text
A square 1:1 abstract scientific emblem for an open-source fluid dynamics
organisation. A single powerful spiral vortex, viewed face-on, centred exactly in
the frame: broad clean glowing arms of electric cyan and teal winding into a
brilliant hot coral and amber core. Bold simple spiral geometry with few, thick,
well-separated arms — graphic and emblematic rather than finely detailed. Deep
near-black charcoal background, volumetric glow, strong contrast, luminous
highlights, subtle film grain. Elegant, iconic, expensive, museum-quality.
ABSOLUTELY NO TEXT, no letters, no words, no numbers, no logos, no watermarks.

[plus, for all candidates: this is a GitHub organisation avatar, displayed as a
CIRCLE at sizes as small as 20 pixels; keep the subject bold, simple, centred and
readable at thumbnail size, with the four corners plain dark background that can
be cropped away without loss; full bleed, no border, no frame, no vignette ring.]
```

## Rejected alternatives

- **Twin counter-rotating vortices**, cyan above and coral below. Tied most
  directly to the org banner, which is a vortex street of alternating-sign
  vortices, and its two-tone signature read best at 20 px — but the silhouette
  can be mistaken for an "S" or an "8" at the smallest sizes.
- **Radial mandala** with many arms. Collapsed into a fuzzy disc at 20 px.
- **Cylinder and wake**, the previous avatar's subject restyled. Its streamlines
  ran to the frame edge and were clipped by the circle crop, and the off-centre
  composition read as mush at thumbnail size.

## Applying it

There is no REST endpoint for an organisation avatar, so this cannot be scripted:
upload it at **https://github.com/organizations/openfluids/settings/profile**.
