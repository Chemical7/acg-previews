# ATI page · image slot reference

The Insights That Move Africa page has 8 image slots. Most are filled with SVG illustrations that work as production-ready placeholders. Two are reserved for atmospheric photography you can generate with an AI tool (or shoot / license).

## Slot inventory

| Slot | File | Status | Dimensions |
|---|---|---|---|
| Hero background (optional) | `photos/hero-bg.jpg` | NOT IN USE — gradient-only currently. Drop a file here to enable the overlay. | 1600×900 JPG |
| The binding constraint illustration | `photos/constraint-illustration.svg` | ✅ SVG art in place | 800×1000 SVG |
| Capability icon · Perception | `icons/cap-perception.svg` | ✅ SVG | 90×90 |
| Capability icon · Evidence | `icons/cap-evidence.svg` | ✅ SVG | 90×90 |
| Capability icon · Stakeholder | `icons/cap-stakeholder.svg` | ✅ SVG | 90×90 |
| Capability icon · Narrative | `icons/cap-narrative.svg` | ✅ SVG | 90×90 |
| Capability icon · Decision | `icons/cap-decision.svg` | ✅ SVG | 90×90 |
| Capability icon · Coalition | `icons/cap-coalition.svg` | ✅ SVG | 90×90 |
| Flagship paper cover | `photos/flagship-paper-mockup.svg` | ✅ SVG | 400×520 |

## To replace any slot with a real AI image

1. Generate the image to the dimensions above (or larger — the page resizes).
2. Save with the same filename (or extension change — e.g. `flagship-paper-mockup.png` instead of `.svg`).
3. If you changed the extension, update the `<img src="...">` line in `../index.html`.
4. Commit + push to GitHub Pages.

## AI image generation prompts

For DALL-E, Midjourney, Gemini Image, ImageFX, etc. All should be saved at the dimensions in the table above. JPG for photos, PNG for illustrations with transparency.

### Hero background (`photos/hero-bg.jpg`, 1600×900)

> Editorial photograph, African city skyline at dusk seen through floor-to-ceiling windows of a high-rise meeting room. Subtle warm light on the horizon, navy and deep teal tones dominate, no people visible. Cinematic, restrained, magazine-quality. No text.

Alternative:
> Abstract editorial illustration, layers of translucent geometric shapes in deep navy, emerald green and gold suggesting decision pathways converging on a focal point. African continent silhouette subtly embedded as negative space. Cinematic, no text.

### The binding constraint (`photos/constraint-committee.jpg`, 1200×1500 portrait)

> Editorial photograph, top-down view of a large committee table covered with printed reports, charts and one highlighted document in the center. Hands of three or four diverse African professionals visible at the edges of the frame, pointing at evidence. Warm morning light from window left. Magazine-quality, contemplative tone. No identifiable faces, no text.

Alternative:
> Editorial illustration in flat vector style, abstract committee scene: three figures arrayed around an elongated table covered with stacked papers, charts and a single highlighted folder at the centre. Navy, white, gold palette. No identifiable faces, no text.

### Flagship paper cover (`photos/flagship-paper-cover.png`, 800×1040)

> Photorealistic mockup of a hardcover strategic policy report titled "Investor Perceptions of Risk in Africa's Gender-Lens Funds" sitting upright at a slight angle on a clean surface. Cover: dark navy with a single bold gold horizontal rule, small ACG concentric-rings mark in the corner. Editorial product photography lighting, neutral grey background, deep drop shadow. No additional text on cover other than the title.

## Hosting via Google Drive (optional)

If you'd rather host the AI images on the work Drive instead of committing to git, the helper script at `../../bin/drive_upload.py` (see project root) handles upload and returns a public URL. Workflow:

```powershell
python ../../bin/drive_upload.py photos/hero-bg.jpg --folder "ACG Web Assets/ATI"
# Returns: https://drive.google.com/uc?export=view&id=XXXX
```

Then replace `./assets/photos/hero-bg.jpg` in `index.html` with the returned URL.

**Trade-off**: Drive-hosted images can be revoked or have their sharing changed, breaking the page. Committing images to the repo is more durable. Drive is good for staging while you iterate; commit when you're satisfied.
