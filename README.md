# mwe-annotation-ita #
This repository contains a corpus of spoken Italian manually annotated with Multiword Expressions.

# Data #
The corpus is built from data of the KIP module of the KIParla Corpus ([Mauri et al., 2019](https://ceur-ws.org/Vol-2481/paper45.pdf)), available for consultation [here](https://kiparla.it/search/).

Data in this corpus corresponds to files BOA1010, BOA3015, BOC1007, BOD1003, BOD2018, TOA1005, TOA3012, TOC1005, TOD1005, TOD2005 of the KIP module. Small changes were made to the text regarding punctuation and tokenization of words.

The text has been lemmatised and POS-tagged using Treetagger (with Marco Baroni's [POS tagset](https://sslmit.unibo.it/~baroni/collocazioni/itwac.tagset.txt)).

Then the corpus has been manually annotated for Multiword Expressions.

# Data download and license #
The corpus is available for download, and is covered by the Creative Common License BY-NC-SA 4.0 provided in this repository

# How to read files #
Data is organized in 10 files, each corresponding to the documents from KIParla mentioned above.
First lines of every file contain the name of the document and the link to the original html page.

The text is organised as it follows:

For each sentence there is:
  - a line that starts with "#Text=" and the complete sentence
  - a line for each token of the sentence, followed by POS-tag, lemma, and MWE tag

Sentences are separeted by blank lines

MWE tags follow the BIO-bio format:

B = First token of an MWE, not inside a gap

b = First token of an MWE, inside the gap of another MWE

I = Token continuing an MWE, not inside a gap

i = Token continuing an MWE, inside the gap of another MWE

O = Not part of or inside any MWE

o = Not part of any MWE, but inside the gap of an MWE

