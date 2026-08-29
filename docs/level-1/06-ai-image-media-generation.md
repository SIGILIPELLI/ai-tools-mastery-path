# 06 · AI Image & Media Generation Basics

Image and media generation tools let you produce visual or audio content
from a text description or a reference input. This module covers the core
concepts, prompting basics that transfer across tools, and — importantly —
the practical and ethical considerations that apply regardless of which
specific tool you use.

## 1. What these tools generally do

| Category | Typical capability |
|---|---|
| Text-to-image | Generate an image from a written description |
| Image-to-image | Modify or restyle an existing image based on a prompt |
| Text-to-video / image-to-video | Generate short video clips from a description or a starting image |
| Text-to-speech / voice generation | Generate spoken audio from text, sometimes in a chosen voice style |
| Music/audio generation | Generate background music or sound from a description |
| Editing assistance | AI-assisted background removal, upscaling, object removal within existing media |

## 2. Prompting basics for image/media generation

Unlike chat prompting (Module 8), visual generation prompting benefits from
being descriptive and specific about visual attributes rather than
conversational.

| Element | Why it helps | Example addition |
|---|---|---|
| Subject | The core content, stated plainly | "a small wooden cabin" |
| Style | Sets the overall visual treatment | "in the style of a watercolor illustration" |
| Composition | Framing and perspective | "wide shot, low angle" |
| Lighting/mood | Affects tone significantly | "warm evening light, soft shadows" |
| Level of detail | Guides how much the tool "fills in" | "simple, minimal" vs. "highly detailed" |
| Negative constraints (where supported) | Rules things out explicitly | "no text, no people" |

A practical loop: generate, look at what's wrong or missing, adjust one or
two elements at a time, regenerate. Changing everything at once makes it
hard to tell which change caused which effect.

## 3. Common limitations to expect

| Limitation | What it means in practice |
|---|---|
| Inconsistency across multiple generations | The same prompt run twice can produce very different results — expect to generate several options and pick |
| Difficulty with precise text in images | Generated text within images is often garbled — treat as unreliable, verify or add text manually afterward |
| Anatomical/structural errors | Hands, small objects, and fine structural details are common failure points — inspect closely |
| Style drift across a series | Getting a consistent look across multiple images/frames often requires deliberate technique or tool features built for it |

## 4. Rights, attribution, and appropriate use

This is the section most beginners skip and shouldn't.

| Consideration | What to check before using generated media |
|---|---|
| Commercial use rights | Whether the specific tool's terms allow commercial use of what you generate, and under what license |
| Training data concerns | Some tools disclose more than others about training sources; if this matters for your use case (e.g., a client project), check the tool's documentation directly |
| Depicting real people | Generating realistic images of real, identifiable people carries distinct ethical and often legal risk — avoid unless you have clear rights and a legitimate purpose |
| Disclosure norms | Many contexts (journalism, some platforms, some client relationships) expect or require disclosure that media is AI-generated — check applicable norms or policy before publishing |

## Worked example

A hobbyist podcaster wants cover art and a short intro music clip. For the
cover art, she writes a prompt with subject, style, composition, and mood
(per section 2), generates four variations, and picks the one where the
text she'll add separately won't clash with the composition — she doesn't
try to get the tool to generate the podcast title as in-image text, since
generated text is unreliable (section 3). Before publishing, she checks the
image tool's terms of service to confirm commercial use is permitted for
her paid tier, since a podcast cover counts as commercial use even for a
hobby show with ads. For the intro music, she generates a short clip,
listens for anything that sounds too close to an existing recognizable
tune (a real risk with music generation), and picks a different generation
when in doubt rather than risking an inadvertent resemblance.

## Exercise

Using any image generation tool available to you, write a prompt following
the six-element structure in section 2 for a real visual you could use (a
social media graphic, a presentation image, anything). Generate at least
two variations, note one limitation from section 3 that showed up in your
result, and check the tool's terms of service for commercial-use rights
before you write down whether you could actually use the output for your
stated purpose.
