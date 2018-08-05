libmscore.py
============

Python library for interacting with [MuseScore]'s native MSCX and MSCZ file
formats, for the rare occasion this is necessary.

[MuseScore]: https://github.com/musescore/MuseScore

Before using this library, you should consider whether the standardized
[MusicXML format][MusicXML] would be more suitable for your needs.
[MuseScore's command line interface][mscore] can be used to convert MSCX and
MSCZ files into MusicXML, which can then be parsed using the excellent
[music21 toolkit][music21].

[MusicXML]: https://github.com/w3c/musicxml "MusicXML Specification"
[mscore]: https://musescore.org/en/handbook/command-line-options "MuseScore Handbook - Command line options"
[music21]: https://github.com/cuthbertLab/music21 "music21 Toolkit for Computational Musicology"

## Valid uses

This library is good for cases that only a native format can handle, such as:

1. Parsing syntax that is specific to MuseScore
    - i.e. where no equivalent syntax exists in MusicXML

2. Editing scores, when the result is to be re-imported into MuseScore
    - i.e. when conversion to MusicXML would result in loss of information

For all other cases you should consider converting the scores to MusicXML.

## WARNING!!!

__THIS LIBRARY MAY BREAK AT ANY TIME!__

MuseScore's file formats are not intended to be edited or parsed outside of
MuseScore itself. The formats are not documented outside of MuseScore's
source code, and they are subject to change without notice.
If you need to interact with scores outside of MuseScore,
you should consider using the standardized [MusicXML format][MusicXML].

## License

This software is released under version 2 of the
[GNU General Public License][GPL-2]. See [LICENSE.txt] for details.

[GPL-2]: http://www.gnu.org/licenses/gpl-2.0.html "GNU General Public License, version 2"
[LICENSE.txt]: LICENSE.txt "Project license - GPL v2"
