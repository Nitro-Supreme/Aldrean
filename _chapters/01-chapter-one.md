---
layout: chapter
title: "Chapter One"
subtitle: "The First Star"
chapter_number: 1
slug: "chapter-one"
audio_file: null
audio_duration: null
---

Begin your story here. This is a template chapter to show you how to structure your novel.

When you're ready, replace this content with your actual chapter text.

## How to Add More Chapters

Create new files in the `_chapters/` folder following this naming convention:

- `01-chapter-one.md`
- `02-chapter-two.md`
- `03-chapter-three.md`

Each file needs this front matter:

```yaml
---
layout: chapter
title: "Chapter Two"
subtitle: "Optional subtitle here"
chapter_number: 2
slug: "chapter-two"
audio_file: null
audio_duration: null
---
```

## Adding Audio Narration

When you're ready to add MP3 files:

1. Create an `assets/audio/` folder (if it doesn't exist)
2. Upload your MP3 file there (e.g., `chapter-01.mp3`)
3. Update the front matter:
   - Change `audio_file: null` to `audio_file: /assets/audio/chapter-01.mp3`
   - Set `audio_duration: "XX minutes XX seconds"`

The audio player will appear automatically at the top of the chapter.

## Formatting Your Content

- Use `##` for section headers within chapters
- Use `**text**` for **bold** emphasis
- Use `*text*` for *italics*
- Separate scenes with a blank line for readability

---

*This is an example chapter. Edit or delete and add your own chapters!*
