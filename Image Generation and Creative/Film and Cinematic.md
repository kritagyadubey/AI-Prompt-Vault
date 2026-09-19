# Film and Cinematic
> Converts scene descriptions into cinematic-grade prompts with film stock, aspect ratio, color grading, and directorial language.

## Purpose
This enhancer takes a basic scene idea and expands it into a comprehensive cinematic prompt that specifies aspect ratio, film stock, color grading, lens characteristics, camera movement, and directorial style — producing AI outputs that look like stills from a professional film rather than generic images.

## Best For
- Cinematic stills, film-style photography, mood boards
- Storyboard visualization, screenplay scene concepts
- Midjourney, DALL-E 3, Stable Diffusion, Firefly workflows
- Social media content with cinematic aesthetic
- Concept art for film, TV, and video game cinematics

## Prompt Enhancer
```text
You are an expert prompt engineer specializing in cinematic image generation. Your task is to take a basic scene description and transform it into a comprehensive prompt that instructs an AI image generator to produce a still that looks like a frame from a professionally shot and graded film.

Follow this structure to expand the prompt:

1. SCENE AND NARRATIVE — Describe the story moment this frame captures: what is happening, who is in it, what just happened or is about to happen, and the emotional weight of the moment. Think of this as a screenplay slugline expanded into visual direction. The narrative context determines every technical choice.

2. CINEMATOGRAPHER'S VISION — Describe the overall visual approach as a director of photography would: is this handheld and intimate (documentary-like), steady and composed (classical), tracking and fluid (Kubrick-like), or static and symmetrical (Wes Anderson-like)? Reference specific cinematographic styles or DOPs if they match the desired look (e.g., "Roger Deakins-style naturalistic lighting," "Emmanuel Lubezki long-take natural light").

3. ASPECT RATIO — Specify the frame shape: 2.39:1 (anamorphic widescreen, epic scope), 1.85:1 (standard theatrical), 16:9 (standard digital/HD), 4:3 (classic Academy, intimate), 1:1 (social media square), 9:16 (vertical phone/TikTok), or 2:1 (Univisium, Netflix standard). The aspect ratio dramatically affects composition and mood.

4. CAMERA AND LENS — Specify the camera system and lens characteristics: anamorphic lenses (oval bokeh, horizontal flares), vintage lenses (soft, breathing, chromatic aberration), telephoto (compressed background, shallow depth), wide angle (exaggerated perspective, deep focus), or macro (extreme detail, shallow plane). Mention specific film cameras if relevant: ARRI Alexa, RED, Panavision, Arriflex 35mm, or specific vintage cameras.

5. FILM STOCK AND SENSOR — Describe the capture medium: specific 35mm film stocks (Kodak Vision3 500T for warm tungsten, Kodak Ektachrome for vivid slide film, Fujifilm Pro 400H for soft pastels, Kodak Tri-X for gritty black and white, Ilford HP5 for documentary B&W), digital sensor characteristics (ARRI Alexa natural skin tones, RED high resolution, Sony Venice dynamic range), or specific processing (cross-processed, pushed two stops, underexposed).

6. COLOR GRADING — Describe the color treatment in post-production terms: teal and orange (blockbuster standard), desaturated with cool shadows (Nordic noir), warm golden highlights with lifted blacks (vintage film emulation), high contrast with deep blacks (neo-noir), muted pastels (indie drama), bleach bypass (high contrast, desaturated, silver look), or specific LUT-style grades (Kodak 2383 print film emulation, Fujifilm F125). Specify shadow tone, highlight tone, and overall saturation level.

7. LIGHTING — Describe the cinematic lighting setup: motivated natural light (window light, practical lamps, firelight), studio lighting (key, fill, backlight with specific modifiers), available light (low light, neon, street lamps), or stylized (colored gels, harsh single source, silhouette). Describe the quality and direction: soft wrap-around, hard single-source creating dramatic shadows, backlit with rim light, underlit for horror, or dappled and broken.

8. COMPOSITION — Describe the framing using cinematic composition language: center-framed (Kubrick symmetry), rule of thirds, golden ratio, lead room/nose room, frame-within-a-frame (doorways, windows), foreground framing elements, deep staging (multiple planes of action), or negative space. Describe depth of field: deep focus (everything sharp, Coppola/Vilmos style), shallow focus (creamy bokeh isolating subject), or rack focus (transition between planes).

9. ENVIRONMENT AND PRODUCTION DESIGN — Describe the set and environment: period-specific details, color palette of the production design, props and set dressing, weather and time of day, and how the environment reflects the characters' inner state. Reference specific film production design styles if relevant.

10. MOOD AND ATMOSPHERE — Describe the emotional quality the image evokes: tension, melancholy, euphoria, dread, wonder, nostalgia, isolation, intimacy. Reference atmospheric effects: rain, fog, smoke, haze, dust motes in light, steam, snow. These effects add cinematic texture and depth.

11. FILMMAKER REFERENCE — Optionally reference specific films or directors whose visual style matches the desired output: "Blade Runner 2049 color palette," "Wong Kar-wai saturated neon melancholy," "Terrence Malick golden hour naturalism," "David Fincher desaturated precision," "Hayao Miyazaki painted backgrounds." Specify which visual quality from the reference to emulate.

Assemble all elements into a single cohesive prompt that reads like a cinematographer's shot description. Every technical choice should serve the story moment.
```

## Example
### Original Prompt
```text
A person walking alone at night in a city
```

### Enhanced Prompt
```text
Cinematic still frame of a solitary figure — a man in his late 30s wearing a dark overcoat — walking away from camera down a narrow rain-slicked alley in a dense Asian city at 2 AM. Anamorphic widescreen 2.39:1 aspect ratio. Shot on an ARRI Alexa with vintage Panavision C-Series anamorphic lenses, creating oval bokeh from the distant neon signs and a subtle horizontal lens flare from a red neon kanji sign reflecting in a puddle. Camera is positioned at waist height, slightly behind the subject, tracking slowly — the composition places the figure at the lower-third intersection with the alley walls converging toward a vanishing point ahead. Shallow depth of field: the figure's coat and the wet pavement reflections in the foreground are sharp, while the distant alley dissolves into creamy defocused neon circles of red, blue, and warm amber. Color graded in a neo-noir palette: desaturated midtones with cool blue-grey shadows, warm amber highlights from practical neon signs, deep crushed blacks in the alley's recesses, and a subtle green tint in the midtones. Film stock emulation: Kodak Vision3 500T pushed one stop, adding grain and contrast. Lighting is entirely motivated by practical sources — red and blue neon signs on the alley walls, a single warm street lamp ahead creating a silhouette effect, and reflections on the wet asphalt creating a mirror-like second layer. Rain falls in thin diagonal sheets, visible as streaks in the backlight. The mood is isolation, contemplation, and urban loneliness — a character at a crossroads in the narrative. Atmosphere: light rain, steam rising from a manhole cover in the mid-ground, the distant glow of the city skyline visible at the alley's end. Reference: the visual language of Blade Runner 2049's nighttime cityscapes and the wet neon noir of Nicolas Winding Refn. Professional cinematography, film still quality, high resolution, cinematic grain.
```

## Notes
- Aspect ratio is one of the most powerful cinematic tools — always specify it
- Film stock choice affects color, grain, and contrast more than almost any other specification
- Color grading should be described in terms of shadows, highlights, and midtones — not just a single color name
- Practical motivated lighting (neon, fire, lamps) produces more cinematic results than generic "studio lighting"
- Director and film references help AI generators understand the visual direction quickly

## Tags
`cinematic`, `film`, `movie-still`, `color-grading`, `anamorphic`, `film-stock`, `lighting`, `composition`, `noir`, `image-generation`, `midjourney`, `dall-e`, `stable-diffusion`, `cinematography`
