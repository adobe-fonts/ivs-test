# IVS Test

IVS Test is a special-purpose OpenType/CFF font that is intended to be used to test the extent to which applications and other text-handling environments support IVSes (*Ideographic Variation Sequences*) through the use of multiple instances of two functional glyphs. One glyph, which looks like U+24B8 (&#x24B8;) and for which there are 256 instances to map code points in blocks of 256, serves to mark CJK Unified Ideographs being displayed as-is. The other glyph, which looks like U+24BE (&#x24BE;) and for which there are 240 instances, one for each of the 240 Variation Selectors in Plane 14 (U+E0100 through U+E01EF), serves to mark correct display of an IVS.

This font supports all current and future CJK Unified Ideographs by covering entire blocks: U+3400 through U+4DBF (Extension A), U+4E00 through U+9FFF (URO), U+FA0E, U+FA0F, U+FA11, U+FA13, U+FA14, U+FA1F, U+FA21, U+FA23, U+FA24, U+FA27 through U+FA29 (CJK Unified Ideographs in the CJK Compatibility Ideographs block), U+20000 through U+2A6DF (Extension B), U+2A700 through U+2F7FF (Extension C and beyond).

A total of 91,052 CJK Unified Ideograph code points are supported, and for each one, a total of 240 IVSes are specified. This means that the total number of IVSes that are defined in the Format 14 'cmap' subtable, as non-default UVSes (*Unicode Variation Sequences*), is a mind-boggling 21,852,480.

## Font installation instructions

* [OS X](http://support.apple.com/kb/HT2509)
* [Windows](http://windows.microsoft.com/en-us/windows-vista/install-or-uninstall-fonts)
* [Linux/Unix-based systems](https://github.com/adobe-fonts/source-code-pro/issues/17#issuecomment-8967116)

## Building the font from source

### Requirements

To build the binary font file from source, you need to have installed the [Adobe Font Development Kit for OpenType](http://www.adobe.com/devnet/opentype/afdko.html) (AFDKO). The AFDKO tools are widely used for font development today, and are part of most font editor applications.

### Building the font

In this repository, all necessary files are in place for building the OpenType/CFF font, and the COMMANDS.txt file provides the command lines that are used.

## Getting Involved

Send suggestions for changes to the IVS Test project maintainer, [Dr. Ken Lunde](mailto:lunde@adobe.com?subject=[GitHub] IVS Test), for consideration.
