# Illumine — Natural voice files

The files in this repository's **releases** are downloaded by the Illumine app
(Bible Verse of the Day Widget) when a reader chooses to add the optional
**Natural voice**. The app works fully without them; nothing here is fetched
unless the reader taps *Download* in Settings ▸ Reading voice.

The voice runs entirely on the reader's phone. These are static files — there
is no server, no account, and nothing about the reader is sent anywhere.

## What is in a release

| File | What it is |
|---|---|
| `kokoro.ort` | [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) v1.0, the `uint8f16` ONNX export by [onnx-community](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX), converted to ONNX Runtime's ORT format |
| `voice_*.bin` | four of Kokoro's voice style files, unchanged |
| `core.ikp` | pronunciations (phoneme ids) for the app's own devotionals, prayers and stories |
| `<TRANSLATION>.ikp` | pronunciations for every verse of one public-domain Bible translation |
| `words.json` | word → pronunciation, used for any line not in a pack |

## Licences

- Kokoro-82M model weights and voices: **Apache-2.0**, © hexgrad — see the
  [model card](https://huggingface.co/hexgrad/Kokoro-82M).
- The ONNX export: **Apache-2.0**, onnx-community.
- The pronunciation files are data generated from public-domain Bible texts and
  the app's own original content; they contain no third-party code.

The app embeds ONNX Runtime 1.23.2 (MIT, Microsoft), built with only the
operators this model uses.
