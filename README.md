# 10 PRINT book cover generation for Python

Read more about this project in [this blog post](http://www.nypl.org/blog/2014/09/03/generative-ebook-covers).

Author of this Python port is Jens Tröger for [Bookalope](https://bookalope.net/), based on the [10 PRINT "BOOK COVER" for Processing](https://github.com/mgiraldo/tenprintcover-p5) project.

Python-based book cover-generating algorithm inspired by [10PRINT](http://10print.org/). Artwork uses the symbols found on the [Commodore PET](https://en.wikipedia.org/wiki/Commodore_PET) keyboard: ![Commodore PET keyboard](https://upload.wikimedia.org/wikipedia/commons/d/db/PET_Keyboard.svg)

### Requirements

Runs on Python 2 and 3.

Requires Python bindings for [Cairo](http://cairographics.org/) installed. While [pycairo](http://cairographics.org/pycairo/) should work but is outdated, this implementation currently uses [cairocffi](https://github.com/SimonSapin/cairocffi).

Requires Noto Sans and Noto Sans CJK SC fonts installed from [Google Internationalization](https://www.google.com/get/noto/).

### Usage

There are two ways of generating book covers with this tool: one, generate a single book cover image by passing information directly through the command line arguments; or two, by passing a JSON file with information and generate a batch of book cover images.

Note that the default dimension of the image is set to 600×900 pixels.

    tenprintcover.py --help

This prints all command line parameters.

    tenprintcover.py --author "Clive Barker" --title "Imagica" --cover barker-imagica.png

Generate a single PNG book cover file `barker-imagica.png` for the book titled *Imagica* by the novelist Clive Barker.

    tenprintcover.py --json-covers my-covers.json

This generates a book cover image for each line in the JSON file, where a single line has the following format (where `subtitle` may be set to `null`):

    {"authors": "...", "identifier": "...", "subtitle": "...", "title": "...", "identifier_type": "...", "filename": "..."}

### Other Resources

- [10 PRINT “BOOK COVER” for iOS/Objective-C](https://github.com/mgiraldo/tenprintcover-ios)
- [10 PRINT “BOOK COVER” for Processing](https://github.com/mgiraldo/tenprintcover-p5)
- [10print.org](https://10print.org/)

### License

See [LICENSE](LICENSE).
