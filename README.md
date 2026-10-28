# Typeface name

> Template for EPI Type typeface repositories. Use **"Use this template"** on GitHub, then replace everything in this file.

Short description of the typeface: what it is, what it is for, where it comes from.

## Specimen

Link to the specimen on [epitype.xyz](https://epitype.xyz/) or add images to `documentation/`.

## Styles and features

- Styles: ...
- Language and script support: ...
- OpenType features: ...

## Download

Ready-to-use font files are in the [latest release](../../releases/latest). Generated font files are not stored in the repository itself.

## Building the fonts

The fonts are built from the sources in `sources/` with [fontmake](https://github.com/googlefonts/fontmake) via [gftools builder](https://github.com/googlefonts/gftools-builder).

```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
gftools builder sources/config.yaml
```

The result is written to `fonts/`. A GitHub Action builds and checks the fonts on every push once sources exist. Pushing a tag like `v1.000` creates a release with a ZIP of the fonts.

## Contributing

Bug reports, glyph requests and pull requests are welcome. See [CONTRIBUTING](https://github.com/EPI-Type/.github/blob/main/CONTRIBUTING.md).

## License

This Font Software is licensed under the SIL Open Font License, Version 1.1. See [OFL.txt](OFL.txt).

## Setting up a new typeface from this template

1. Create the repository from this template.
2. Replace `<TYPEFACE NAME>` and `<REPOSITORY>` in `OFL.txt`, set the name in `sources/config.yaml`, and rewrite this README.
3. Add the source files to `sources/`.
4. Add everyone who holds copyright to `AUTHORS.txt` and everyone who contributed to `CONTRIBUTORS.txt`.
5. Make sure the same copyright line and license text end up in the font's name table.
6. Remove this section.
