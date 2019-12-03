# IVS Test

*IVS Test* is a special-purpose OpenType/CFF font that is intended to be used to test the extent to which apps and other text-handling environments support IVSes (*Ideographic Variation Sequences*) through the use of multiple instances of two functional glyphs. One glyph, which looks like U+24B8 (&#x24B8;) and for which there are 256 instances to map code points in blocks of 256, serves to mark characters that have the *Ideographic* property being displayed as-is. The other glyph, which looks like U+24BE (&#x24BE;) and for which there are 240 instances, one for each of the 240 Variation Selectors in Plane 14 (U+E0100 through U+E01EF), serves to mark correct display of an IVS.

This font supports all current and future CJK Unified Ideographs by covering entire blocks: U+3400 through U+4DBF ([Extension A](https://www.unicode.org/charts/PDF/U3400.pdf)), U+4E00 through U+9FFF ([URO](https://www.unicode.org/charts/PDF/U4E00.pdf)), U+FA0E, U+FA0F, U+FA11, U+FA13, U+FA14, U+FA1F, U+FA21, U+FA23, U+FA24, U+FA27 through U+FA29 (CJK Unified Ideographs in the [CJK Compatibility Ideographs](https://www.unicode.org/charts/PDF/UF900.pdf) block), U+20000 through U+2A6DF ([Extension B](https://www.unicode.org/charts/PDF/U20000.pdf)), U+2A700 through U+2F7FF ([Extension C](https://www.unicode.org/charts/PDF/U2A700.pdf), [Extension D](https://www.unicode.org/charts/PDF/U2B740.pdf), [Extension E](https://www.unicode.org/charts/PDF/U2B820.pdf), [Extension F](https://www.unicode.org/charts/PDF/U2CEB0.pdf) and beyond), U+2FA20 through U2FFFD (the end of Plane 2), and U+30000 through U+3FFFD (Extension G and the remainder of Plane 3). Also covered are blocks for other characters that have the *Ideographic* property, specifically U+3006, U+3007, and U+3021 through U+3029 ([CJK Symbols and Punctuation](https://www.unicode.org/charts/PDF/U3000.pdf)), U+17000 through U+18AFF ([Tangut](https://www.unicode.org/charts/PDF/U17000.pdf) and [Tangut Components](https://www.unicode.org/charts/PDF/U18800.pdf)), and U+1B170 through U+1B2FF ([N&#x00FC;shu](https://www.unicode.org/charts/PDF/U1B170.pdf)).

A total of 165,411 Ideograph code points are supported, and for each one, a total of 240 IVSes are specified. This means that the total number of IVSes that are defined in the Format 14 'cmap' subtable is a mind-boggling 39,698,640. IVSes that correspond to a Base Character followed by VS17 (aka U+E0100} are treated as a default UVS (*Unicode Variation Sequence*). This means that 165,411 of the IVSes are represented as default UVSes, and the remaining 39,533,229 are represented as non-default ones.

:warning: **WARNING:** While using the Firefox app on Windows, if you experience a freeze, which lasts several minutes but eventually resumes, it is likely due to having this particular font installed and that app's need to read its 'cmap' table. The 'cmap' table, at nearly 200MB due to the nearly 40 million UVSes specified in the Format 14 subtable, literally represents 99.99% of the footprint of the OpenType/CFF font. :warning:

## Downloading the font

The OpenType/CFF font, *IVSTest-Regular.otf*, can be easily downloaded from the [Latest Release](../../releases/latest/). It is 197,687,148 bytes, and its MD5 hash is 226f20ee911aaca524d2c08b1cab1eb4.

## Building the font from source

### Requirements

To build the binary font file from source, you need to have installed the [Adobe Font Development Kit for OpenType](https://github.com/adobe-type-tools/afdko/) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF font, and the COMMANDS.txt file provides the command lines that are used.

**Special Note**: Due to its size, the UVS definition file that specifies 39,698,640 IVSes is provided as a ZIP file that was necessarily split, also due to its size (GitHub imposes a 100MB file size limit). Unfortunately, the built-in *Archive Utility* app of macOS does not support split ZIP files, and we therefore recommend that you download and install the [Unarchiver](http://unarchiver.c3.cx/unarchiver) app. To unzip, either drag *IVSTest_sequences.txt.z01* onto the *Unarchiver* app, or use Control-Click to open it by specifying that app (after installing the *Unarchiver* app, you may also be able to simply double-click that file). Either of these actions will combine the two parts and unzip them. For Windows, select the *IVSTest_sequences.txt.z01* file, then use the "Extract All" context menu to combine the two parts and unzip them. For Ubuntu and possibly other flavors of Linux, we recommend that you download and install the [Unarchiver command-line tools](https://unarchiver.c3.cx/commandline), then simply execute the *unar* command with the *IVSTest_sequences.txt.z01* file as its argument.

## Getting Involved

For any suggestions for changes, please create an issue here in GitHub for consideration.
