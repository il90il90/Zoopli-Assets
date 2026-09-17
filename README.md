# Zoopli-Assets

Content pack for **[Zoopli](https://github.com/il90il90/Zoopli)** — a Hebrew/English animal
learning game for young children.

The app downloads everything here on first launch, which is why the app itself installs at under
two megabytes. Publishing to this repository updates every installed copy: no Play release needed
to add an animal.

- **Content version:** 16
- **Animals:** 105
- **Manifest:** [`manifest.json`](manifest.json)
- **Attribution and licences:** [`CREDITS.md`](CREDITS.md)

## How the app reads this

```
https://cdn.jsdelivr.net/gh/il90il90/Zoopli-Assets@main/manifest.json
```

`manifest.json` lists every animal with its text in both languages and, for each media file, a
path, a byte count and a SHA-256 hash. The app downloads only files whose hash it does not already
hold, and verifies each one before use — so adding a single animal costs a single small download.

## Rebuilding

This tree is generated. Edit
[`content-pack/animals.json`](https://github.com/il90il90/Zoopli/blob/main/content-pack/animals.json)
in the app repository, then:

```bash
python3 tools/build_content.py --content-version N
tools/publish_assets.sh
```

## Licensing

Every image and sound is redistributed under a free licence, listed per file in
[`CREDITS.md`](CREDITS.md). Nothing here is proprietary.
