# social-biblical-networks
Results and code of MSc thesis Artificial Intelligence on VU Amsterdam, with the topic "Using social co-occurrence networks to analyze Biblical narrative" by Frederik de Vree.

Needs laf-fabric with ETCBC database with glossary (which can be found here: http://dx.doi.org/10.17026/dans-2z3-arxf), forceatlas.py (https://github.com/tpoisot/nxfa2), and some other Python packages available via pip.

Explanation of the code is available in the thesis, which also includes an appendix with pseudocode. And of course an explanation of the results is available in the Results section. The thesis can be found on Academia, at https://www.academia.edu/26149493/

---

Cooccurrences 2.ipynb added to repository. With restructured code for more clarity and easier extensibility and extra features added by request of Christiaan Erwich, PhD student at VU University, to help his research in participants in the Psalms:
* Added word distance weight next to sentence distance weight for more detailed in-sentence edge weight. Word and sentence distance weights are stored both seperately and combined as properties of the edges
* Added verse to occurence information (next to existing book and chapter information)
* Network can now also contain nodes that represent personal pronouns, demonstrative pronouns and words with suffixes that refer to persons. Unlike the existing nodes that represent proper nouns, these are added together, because it is not possible to know automatically to which person these words are referring.
* Each node now has the properties suffix, id, occurrence, lexeme, suffix_trans (transliterated suffix), gloss (English translation) and part of speech when appropriate; these properties are empty when not applicable. This means that a visualization now has more flexibility as to what information to show
