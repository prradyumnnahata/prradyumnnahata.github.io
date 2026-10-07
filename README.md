# pradyumn nahata — essays

Live at: https://prradyumnnahata.github.io

## Adding a new essay

Open `essays.json` (click it on GitHub, then the pencil/edit icon) and add a new
object to the array, in the same shape as the existing one:

```json
{
  "slug": "a-short-url-safe-id",
  "title": "The Essay Title",
  "date": "2026-10-07",
  "image": "",
  "excerpt": "One sentence description (not shown on the site yet, but good to keep).",
  "body": "First paragraph.\n\nSecond paragraph.\n\nThird paragraph."
}
```

Notes:
- `slug` must be unique and URL-safe (lowercase, hyphens, no spaces/punctuation).
- `date` is `YYYY-MM-DD`; essays are sorted newest-first automatically.
- Paragraphs in `body` are separated by a blank line (`\n\n` in JSON). A single
  `\n` inside a paragraph becomes a line break.
- `image` can stay `""` for now, or point to an image file path in this repo
  once you add one (see below).
- Don't forget the comma between essay objects if you're adding one after
  another.

Commit the change (GitHub's web editor lets you commit directly from the
browser — no need to clone anything). The site rebuilds automatically within
about a minute.

## Adding an image to an essay

Upload the image file to this repo (drag and drop into the GitHub web UI, or
add it alongside everything else if you're working locally), then set that
essay's `"image"` field to the file's path, e.g. `"image": "images/my-photo.jpg"`.

## Changing the background photo

Replace `sky.jpg` with a new image of the same name (or update the filename
referenced in `index.html`'s `background-image: url('sky.jpg')` line).

## Local editing (optional)

If you'd rather edit on your own computer:

```
git clone https://github.com/prradyumnnahata/prradyumnnahata.github.io
```

Edit `essays.json` in any text editor, then:

```
git add essays.json
git commit -m "add new essay"
git push
```
