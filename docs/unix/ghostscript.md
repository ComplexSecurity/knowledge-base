icon:fontawesome/solid/terminal

# Ghostscript

Suite of software based on an interpreter for Adobe Systems' PostScript and Portable Document Format (PDF) page description languages.

## Usage

```bash
gs [switches] [file1.ps file2.ps ...]
```

## Flags

```bash
Most frequently used switches: (you can use # in place of =)
 -dNOPAUSE           no pause after page   | -q       `quiet', fewer messages
 -g<width>x<height>  page size in pixels   | -r<res>  pixels/inch resolution
 -sDEVICE=<devname>  select device         | -dBATCH  exit after last file
 -sOutputFile=<file> select output file: - for stdout, |command for pipe, embed %d or %ld for page #
```

## Examples

##### PDF to Text Conversion

```bash
$ gs -sDEVICE=txtwrite -o pdf_dump.txt LOG.pdf
GPL Ghostscript 10.0.0 (2022-09-21)
Copyright (C) 2022 Artifex Software, Inc.  All rights reserved.
This software is supplied under the GNU AGPLv3 and comes with NO WARRANTY:
see the file COPYING for details.
Processing pages 1 through 2.
Page 1
Page 2
```

##### PDF to JPEG

```bash
gs -q -dBATCH -dNOPAUSE -dFirstPage=1 -dLastPage=1 -sDEVICE=jpeg -r<OUTPUT RESOLUTION> -sOutputFile=<OUTPUT>.jpg <INPUT>.pdf
```

##### Normalize PDF

```bash
gs -dSAFER -dBATCH -dNOPAUSE -dNOCACHE -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -sOutputFile=output.pdf input.pdf
```

##### Color PDF to greyscale

```bash
gs -dSAFER -dBATCH -dNOPAUSE -dNOCACHE -sDEVICE=pdfwrite -sColorConversionStrategy=Gray -dProcessColorModel=/DeviceGray -sOutputFile=output.pdf input.pdf
```

## References

- [Ghostscript.com](https://www.ghostscript.com/)
- [Ghostscript.com - ReadMe](https://ghostscript.com/docs/9.56.1/Readme.htm)
