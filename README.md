# megahr-crossling

This repository contains predictions on concreteness and imageability of words in 78 languages.

The predictions are based on supervised learning on the [MEGAHR repository](http://megahr.ffzg.hr/) for response variables and [the Facebook cross-lingual word embeddings](https://github.com/Babylonpartners/fastText_multilingual) for explanatory variables.

The experiments identifying the optimal transfer method are described in the paper cited below. Please cite this paper if you use any part of this repository.

```
@inproceedings{ljubesic18-predicting,
  author    = {Nikola Ljube\v{s}i\'{c} and Darja Fi\v{s}er and Anita Peti-Stanti\'{c}},
  title     = {Predicting Concreteness and Imageability of Words Within and Across Languages via Word Embeddings},
  booktitle = {Proceedings of the 3nd Workshop on Representation Learning for NLP, RepL4NLP@ACL 2018, Melbourne, Australia, July 20, 2018},
  year      = {2018}
}
```

Each of the files contains (word, concreteness prediction, imageability prediction) triples, one per line, with tab-separated values. Both variables were defined in the initial MEGAHR resource on a Likert scale 1--5. The predictions, however, can surpass the limits of this scale.

For each language there are three files generated, ```megahr.[lang_code]```, a frequency-sorted file, ```megahr.[lang_code].sort.c```, a concreteness-sorted file, and ```megahr.[lang_code].sort.i```, an imageability-sorted file.
