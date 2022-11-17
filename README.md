# ttf-converter

This is a Python script that converts fonts to TrueType/OpenType format. It
uses the FontForge Python bindings to read/process and write any font format.
Also, as part of the conversion process, the script tries to fix
inconsistencies and do necessary changes to the font to honor the TTF/OTF
format specs.

Though TrueType is often used synonymously with outline fonts, it supports
embedded bitmaps. ttf-converter leaves the glyph kind (outline/bitmapped)
unchanged.

For converting a font to have scalable outline glyphs, see vfontas instead.

# Dependencies

Note that this script uses the FontForge Python bindings, which need
to be installed in the system. In SLE / openSUSE Leap / openSUSE
Tumbleweed, you just need to run:

```
sudo zypper in fontforge
```

# Usage

To convert a file.pfb Type1 font to a TrueType font in this directory,
ttf-converter can be run like:

```
ttf-converter file.pfb
```

The generated file will have the name of the font family and style.

If you want to convert all fonts in a directory, use it like:

 ```
 ttf-converter --input-dir /usr/share/fonts/Type1 --output-dir generated
 ```
 
 This will read all *.pfa/*.pfb files in the `/usr/share/fonts/Type1`
 directory and generate an output file for each of them in the `generated`
 directory (which will be created if needed)
