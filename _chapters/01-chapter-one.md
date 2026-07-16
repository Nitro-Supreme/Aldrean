---
layout: chapter
title: "Chapter One"
subtitle: "The First Star"
chapter_number: 1
part: 1
audio_file: null
audio_duration: null
---

Begin your story here. This is a template chapter to show you how to structure your novel.

When you're ready, replace this content with your actual chapter text.

## How to Add Chapters to Parts

Each chapter needs these fields in front matter:

```yaml
---
layout: chapter
title: "Chapter Two"
subtitle: "Optional subtitle here"
chapter_number: 2
part: 1
audio_file: null
audio_duration: null
---
```

The `part` field (1, 2, 3, or 4) determines which part the chapter appears under in the Table of Contents.

## Adding Audio Narration

When you're ready to add MP3 files:

1. Create an `assets/audio/` folder (if it doesn't exist)
2. Upload your MP3 file there (e.g., `chapter-01.mp3`)
3. Update the front matter:
   - Change `audio_file: null` to `audio_file: /assets/audio/chapter-01.mp3`
   - Set `audio_duration: "XX minutes XX seconds"`

The audio player will appear automatically at the top of the chapter.

---

*This is an example chapter. Edit or delete and add your own chapters!*
