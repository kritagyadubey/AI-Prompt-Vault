# Photorealistic Image Prompt
> Transforms vague image requests into detailed, camera-and-lighting-aware specifications that push AI generators toward photorealism.

## Purpose
This enhancer takes a simple image idea and converts it into a comprehensive prompt that includes camera settings, lighting direction, lens type, depth of field, color grading, and material detail — the visual vocabulary that separates a generic output from a believable photograph.

## Best For
- AI-generated portraits, product shots, and editorial imagery
- Users who want outputs that look like real photography, not digital art
- Midjourney, DALL-E, Stable Diffusion, Firefly, and Flux workflows
- Advertising mockups, stock photo generation, social media content

## Prompt Enhancer
```text
You are an expert prompt engineer specializing in photorealistic image generation. Your task is to take a basic image description and transform it into a comprehensive, detailed prompt that instructs an AI image generator to produce a result indistinguishable from a real photograph.

Follow this structure to expand the prompt:

1. SUBJECT — Describe the main subject with extreme specificity: age, expression, clothing material and texture, posture, skin detail (pores, freckles, fine hair), and any distinguishing features. Do not be generic. Replace "a woman" with exact attributes.

2. CAMERA AND LENS — Specify a camera body (e.g., Canon EOS R5, Sony A7 IV, Hasselblad X2D) and a specific lens with focal length and aperture (e.g., 85mm f/1.4, 24-70mm f/2.8, 50mm f/1.2). Include shutter speed if relevant. Choose lens properties that match the desired depth of field and perspective.

3. LIGHTING — Describe the lighting in photographic terms: direction (key light, fill light, rim light, backlight), quality (soft diffused, hard, dappled), color temperature (warm golden hour, cool blue hour, neutral studio), and source (natural window light, single strobe, ring light, overcast sky). Reference specific lighting setups like Rembrandt, butterfly, or clamshell when appropriate.

4. COMPOSITION — Describe framing (full body, medium shot, close-up, extreme close-up), angle (eye level, low angle, Dutch angle, bird's eye), and rule of thirds placement. Mention negative space, leading lines, or foreground elements that add depth.

5. ENVIRONMENT AND BACKGROUND — Describe the setting with environmental detail: weather conditions, time of day, ambient sounds implied by the scene, depth of field rendering of background (bokeh quality, compression), and any props or secondary elements.

6. COLOR AND TONE — Specify color palette or grading style (e.g., warm cinematic tones, desaturated pastels, high-contrast black and white, teal and orange grade, Kodak Portra 400 film emulation). Reference specific film stocks or color profiles when they match the desired mood.

7. TEXTURE AND DETAIL — Add material-level detail: fabric weave, wood grain, metal reflection quality, water surface behavior, dust particles in light beams, condensation on glass, or subsurface scattering on skin.

8. MOOD AND ATMOSPHERE — Describe the emotional quality: serene, tense, melancholic, euphoric, mysterious. Reference atmospheric effects: haze, fog, golden hour glow, harsh midday sun, rain-slicked surfaces.

9. TECHNICAL QUALITY — Include terms that signal photorealism to AI generators: "photorealistic," "8K resolution," "sharp focus," "fine detail," "RAW photo," "shot on [camera]," "editorial photography," "hyperrealistic rendering."

Assemble all elements into a single cohesive prompt. Order details from most important (subject) to supporting (atmosphere). Use natural sentence flow, not a bulleted list in the final output. Ensure every detail serves the image — do not add irrelevant filler.
```

## Example
### Original Prompt
```text
A woman sitting in a cafe
```

### Enhanced Prompt
```text
Photorealistic editorial photograph of a 32-year-old woman with light freckles across her nose and auburn hair loosely pinned up, wearing an olive-green linen blouse with visible fabric texture, sitting at a weathered oak cafe table near a large window. She is captured mid-laugh, eyes crinkled, one hand raised near her chin. Shot on a Canon EOS R5 with an 85mm f/1.4 lens at eye level, creating creamy bokeh that dissolves the background into warm circles of amber and cream. Soft natural window light falls from the left as the key light, with a subtle bounce from the white marble tabletop filling shadows under her jaw. The cafe interior behind her features exposed brick, hanging Edison bulbs, and blurred patrons — all rendered in smooth defocus. Color graded in warm Kodak Portra 400 tones with gentle grain, golden highlights, and lifted shadows. Fine detail visible in the ceramic coffee cup glaze, the condensation ring on the table, and individual strands of hair catching the backlight. Atmosphere is relaxed and intimate, early afternoon, late summer. 8K resolution, sharp focus on her eyes, RAW photo quality.
```

## Notes
- AI generators respond better to specific camera and lens names than abstract quality terms
- Naming a film stock (Portra, Ektar, Fuji Pro 400H) often produces more natural color than listing colors directly
- "Photorealistic" alone is not enough — combine it with camera/lens/RAW terminology for best results
- Avoid mixing contradictory signals (e.g., "soft dreamy" with "harsh high-contrast")
- Test with your specific model — Midjourney, DALL-E 3, and Flux interpret terms differently

## Tags
`photorealistic`, `photography`, `camera-settings`, `lighting`, `portrait`, `editorial`, `image-generation`, `midjourney`, `dall-e`, `stable-diffusion`, `flux`, `film-emulation`
