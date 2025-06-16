# Deepmind Notes

# SecurID

- Generative AI is playing more and more of a role in every day life.
    - Short demo of Veo3, incredibly realistic, includes audio.
- GenAI comes with risks: lower bars for scams, manipulations, resulting in reduced trust in information and the potential for mass manipulation at scale.
- Ex: there was a company that ran “influence as a service”, utilizing Claude as the backbone for a believable actor.

## Generative AI Provenance

- The GenAI landscape needs to be robust and adaptable, which means there will be many tools to verify authentic or artificial content.
- The provenance should provide accessible transparency tools to everyone.
- Possible technologies should include fingerprinting, metadata, indexing, ai watermarks, ml detectors, and traditional search results and related links.
    - **There is no magic bullet. There needs to be a suite.**

## SynthID

- AI watermarking applied to all of Google’s AI models, all consumer facing products.
- Google has partnered with NVIDIA, Github, etc to roll out this.
- Partially open sourced.

## Watermarking

- There is a scale between robustness and imperceptibility; the less imperceptible, the less robust and vice versa.
- A unique watermark is added pixel wise; in a video, every frame has this adaptation.
- The watermarking is robust even to basic transformations, including photo screenshots.
- For audio, the watermarking is applied to the spectrogram.
- For text, applied at the token generation step
- The detection is localized. For images, you can tell which part of the image are likely to be ai generated. For videos and audio, timeframes, and for text, which parts.
- Probabilistic. It’s not all or nothing.

MAJOR limitations. Still not robust to filters, rotations, noise, or cropping/zooming.