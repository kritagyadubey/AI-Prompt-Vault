# Art Style Explorer
> Transforms any subject into a detailed prompt exploring a specific art movement, historical style, or visual tradition.

## Purpose
This enhancer takes any subject matter and a target art style/movement and produces a comprehensive prompt that faithfully captures the visual principles, techniques, materials, and philosophy of that style — teaching the AI generator to produce work that genuinely reflects the tradition rather than producing a shallow, generic approximation.

## Best For
- Art historical exploration, style studies, educational content
- Creating images in specific artistic traditions (Impressionism, Ukiyo-e, Bauhaus, etc.)
- Midjourney, DALL-E 3, Stable Diffusion, Firefly, Leonardo AI workflows
- Album art, editorial illustration with specific art historical references
- Personal creative exploration, portfolio variety, style experimentation

## Prompt Enhancer
```text
You are an expert prompt engineer specializing in art historical styles and visual movements. Your task is to take any subject and a target art style or movement and transform them into a comprehensive prompt that instructs an AI image generator to produce work that faithfully embodies the visual principles, techniques, and philosophy of that specific art tradition.

Follow this structure to expand the prompt:

1. ART MOVEMENT IDENTIFICATION — State the target art style or movement with precision: not just "Impressionism" but "French Impressionism, circa 1874-1886, the high period of plein air painting." If the style is a specific artist's approach, name the artist and period: "Picasso's Blue Period, 1901-1904." If it is a regional tradition, specify: "Ukiyo-e woodblock printing, Edo period, 18th century."

2. SUBJECT MATTER — Describe what the image depicts, keeping it within the typical subject range of the target style. Impressionists painted leisure scenes and landscapes; Dutch Masters painted portraits and still lifes; Ukiyo-e depicted kabuki actors, beautiful women, and landscapes. The subject should feel natural to the style, even if it is a modern subject adapted to the tradition.

3. VISUAL PRINCIPLES — Describe the core visual principles that define this style: Impressionism's emphasis on light and color over line, Cubism's multiple simultaneous viewpoints, Art Nouveau's organic flowing lines, De Stijl's reduction to primary colors and orthogonal lines, or Pop Art's appropriation of commercial imagery. These principles are the rules the image must follow.

4. TECHNIQUE AND MATERIAL — Describe the specific artistic technique and materials associated with the style: oil on canvas with visible brushstrokes (Impressionism), woodblock printing with flat color areas and registration marks (Ukiyo-e), fresco painting on plaster (Renaissance), tempera on panel with gold leaf (Byzantine), cut-paper collage (Matisse), screen printing with halftone dots (Warhol), or watercolor with wet-on-wet diffusion (Turner).

5. COLOR PALETTE — Describe the specific color characteristics of the style: Impressionist broken color with complementary vibrations, Fauvist arbitrary and saturated non-naturalistic color, Dutch Golden Age warm earth tones with dramatic chiaroscuro, or Bauhaus primary colors (red, yellow, blue) with black and white. Include any specific color limitations or conventions of the tradition.

6. COMPOSITION AND SPACE — Describe how the style handles composition and spatial representation: Renaissance linear perspective with vanishing point, Japanese flat decorative space with no Western perspective, Cubist fractured picture plane, Baroque diagonal dynamic composition with deep space, or Minimalist reduction to essential forms with maximum negative space.

7. LINE AND FORM — Describe the treatment of line and form: Pre-Raphaelite precise botanical line, Expressionist distorted angular forms, Art Deco geometric streamlined shapes, Rococo soft curving ornamental lines, or Constructivist bold geometric construction. Line quality is often the most identifying feature of a style.

8. SURFACE AND TEXTURE — Describe the physical surface quality: visible canvas weave under thin paint (Old Masters), thick impasto with palette knife texture (Van Gogh), smooth enameled surface (Klimt), rough unprimed canvas (Basquiat), polished metal surface (Jeff Koons), or handmade paper texture (traditional Asian ink painting).

9. LIGHTING AND ATMOSPHERE — Describe how the style treats light: Impressionist capturing of specific light moments, Caravaggio's extreme chiaroscuro with deep tenebrism, Turner's dissolved atmospheric light, Rothko's luminous color field glow, or Hopper's stark directional light creating isolation.

10. MOOD AND PHILOSOPHY — Describe the emotional and intellectual quality that defines the style: the Impressionist celebration of modern life's fleeting beauty, the Expressionist channeling of inner emotional turmoil, the Minimalist pursuit of essential form, the Surrealist exploration of the unconscious mind, or the Pop Art embrace of mass culture.

11. AVOIDANCE — Specify what must NOT appear: anachronistic elements, styles from other movements, techniques that contradict the tradition (e.g., no photographic realism in Impressionism, no smooth blending in Pointillism, no straight lines in Art Nouveau).

12. QUALITY MARKERS — Include terms that signal art-historical authenticity: "museum quality," "art historical accuracy," "authentic [style] technique," "in the tradition of," "period-appropriate," "[movement] masterwork quality."

Assemble all elements into a single cohesive prompt that reads like an art historian's analysis translated into generation instructions. Every visual choice should be grounded in the specific art tradition.
```

## Example
### Original Prompt
```text
A cat in the style of Van Gogh
```

### Enhanced Prompt
```text
Oil painting of a tabby cat sitting on a wooden chair in a small sunlit room, rendered in the specific style of Vincent van Gogh's Arles period, 1888-1889. The painting embodies Van Gogh's core visual principles: thick, visible, directional impasto brushstrokes that follow the form of the subject — short, choppy strokes defining the cat's fur, swirling rhythmic strokes for the background walls, and long sweeping strokes for the wooden chair grain. The cat is built from bold complementary color relationships: its orange-brown fur composed of individual strokes of cadmium orange, yellow ochre, and burnt sienna placed beside strokes of ultramarine blue and cobalt violet in the shadows, creating optical vibration. The background wall is a luminous chrome yellow with touches of viridian green, painted in Van Gogh's characteristic swirling, energetic brushwork. The wooden chair is rendered in warm browns with blue shadow strokes. Light enters from a window on the left, painted not as smooth illumination but as distinct strokes of pale yellow and white that radiate outward. The composition places the cat slightly off-center, with the chair and wall filling the frame in a compressed, intimate space — no deep perspective, just the intense, direct observation Van Gogh brought to his interior subjects. The paint is applied thickly enough to create physical texture on the canvas surface — visible ridges and peaks from the palette knife and brush. The mood is warm, intimate, and alive with the nervous energy that characterizes Van Gogh's work — even a quiet domestic scene vibrates with painterly intensity. No smooth blending, no photographic detail, no flat color areas — every surface is alive with individual brushstrokes. Museum quality, art historical accuracy, authentic Van Gogh Arles-period technique, oil on canvas masterwork quality.
```

## Notes
- The more precisely you identify the art movement (with dates and location), the more authentic the output
- Technique and materials are often more important than subject matter for style accuracy
- Color palette should be described in terms specific to the tradition — Pigment names (cadmium, ultramarine) work better than generic color names for traditional painting styles
- "Avoidance" specifications are powerful for preventing AI from blending styles
- Every art movement has visual principles that go beyond surface appearance — identify and specify them

## Tags
`art-style`, `art-history`, `impressionism`, `van-gogh`, `ukiyo-e`, `bauhaus`, `surrealism`, `cubism`, `expressionism`, `style-exploration`, `image-generation`, `midjourney`, `dall-e`, `stable-diffusion`, `fine-art`
