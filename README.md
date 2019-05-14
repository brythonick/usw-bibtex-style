# University of South Wales Bibtex Style

The standard natbib styles, either `painnat` or `apa`, aren't quite formatted
as USW expect.

This repo contains a bibtex style file created to try and match what the
university has put in its [Harvard referencing guide][1].

I generated this on MacTeX using the `latex makebst` tool. This runs
interactively as a series of questions about the appearence of your references
and citations. I picked the answers that were closest to the [uni's examples][2].

To find out where to put the `.bst` file on your system. First find out where
one of the existing styles is:
```bash
kpsewhich plainnat.bst
```

Copy `usw.bst` into this folder then run `texhash` to rebuild the database of
styles. On macOS you may need to run this with `sudo` depending on where the
MacTeX home folder is.

In my main `.tex` file, I've got the following options relating to the
bibliography:
```tex
\usepackage[round, authoryear]{natbib}
\usepackage{url}

% ...

bliographystyle{usw}
```


[1]: https://library.southwales.ac.uk/collections-subject-guides/referencing/
[2]: https://library.southwales.ac.uk/documents/33/Harvard_Referencing_28_Feb_2015.pdf
