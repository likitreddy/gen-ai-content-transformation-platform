# gen-ai-content-transformation-platform
AI-powered platform that transforms articles, reports and PDFs into LinkedIn posts, X threads, advisories, infographics, executive summaries, slides and video packages. Built with Gradio and open LLMs.

Organisations end up manually rewriting the same source material — a report, an advisory, a threat brief — into a dozen different formats depending on who needs it and why. That's slow and inconsistent.

This is a small AI-powered tool that does the reformatting for you. Paste in an article, report, or any text, pick what you want out of it (a LinkedIn post, an executive summary, a quiz, whatever), and it generates all of them from the same source in one go.

## What it can generate

Feed it one piece of content, and pick any combination of:

- **Video script** — scene-by-scene, with narration and visual notes
- **LinkedIn post**
- **Twitter/X thread**
- **Advisory document** — structured, with recommendations
- **Infographic content** — headline + key stats + layout ideas
- **Executive summary**
- **Presentation outline** — slides + speaker notes
- **Summary**
- **MCQs** — for training/testing purposes, with answers included

You can also set the audience, tone, language, and how detailed you want it — so the same source article can come out very differently depending on who it's for.

## How it works

Nothing fancy under the hood: you give it text (typed or a PDF/DOCX/TXT upload), it builds a tailored prompt for each output type you picked, sends it to an LLM through the Hugging Face Inference API, and hands back the results — downloadable as Markdown.

## Running it

It's built to run in Google Colab, no GPU needed since the actual generation happens on Hugging Face's servers, not your machine.

1. Open the notebook in Colab
2. Grab a free token from [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)
3. Drop it into the `HF_TOKEN` variable
4. Run all cells — the last one gives you a public Gradio link you can open, share, or demo from

```python
!pip install -q gradio huggingface_hub pypdf python-docx
```

## What's in the repo
