# ttf-converter
Python script that converts fonts to TrueType format (.ttf)

Note that this script uses the fontforge python bindings, which needs
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
 ttf-converter --input-directory /usr/share/fonts/Type1 --output-directory generated
 ```
 
 That will read all *.pfa/*.pfb files in the `/usr/share/fonts/Type1`
 directory and generate an output file for each of them in the `generated`
 directory (which will be created if needed)
