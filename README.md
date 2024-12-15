# rewrite-bash

> Author: https://matt.might.net/articles/shell-scripts-for-passive-voice-weasel-words-duplicates/

3 shell scripts to improve your writing.

## Structure

Scripts are:

- `weasel`: Highlight weasel words.
- `passive`: Highlight passive voice.
- `dups`: Highlight duplicate words.

## Usage

You can create a local copy of the scripts in the `bin/` directory of each paper's repository. 

Then you can add a `make proof` target to your `Makefile`:

```make
# Check style:
proof:
        echo "weasel words: "
        sh bin/weasel *.tex
        echo
        echo "passive voice: "
        sh bin/passive *.tex
        echo
        echo "duplicates: "
        perl bin/dups *.tex
```
