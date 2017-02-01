The Galician-TreeGal is a treebank for Galician language labeled using Universal Dependencies, developed between January and July, 2016, at LyS Group (Universidade da Coruña).

The resource derives from a subset (called *xeral*) of the XIADA corpus (v2.6), created at the Centro Ramón Piñeiro para a Investigación en Humanidades (http://corpus.cirp.es/xiada/).

All the information except the syntactic one was semi-automatically converted to UD from the original resource. The dependency labels were assigned using cross-lingual parsing techniques, and then manually corrected by a linguist (see the references for more information).

Galician-TreeGal v0.4 contains 1000 sentences of the xeral corpus (~25k tokens), and it is divided 20-40-40 splits (train-dev-test).

### Stats
* Tree count:  1000
* Word count:  25383
* Token count: 24219
* Dep. relations: 37 of which 4 language specific
* POS tags: 15
* Category=value feature pairs: 44

### Issues
* Complex proper nouns have always a flat:name internal structure.
* The dependency labels need to be reviewed by another expert to calculate inter-annotator agreement.

### References
* Garcia, Marcos, 2016. *Universal Dependencies Guidelines for the Galician-TreeGal Treebank.* Technical Report. LyS Group, Universidade da Coruña.

### Changelog

2017-01-02 v0.4

* POS-tags, morphological features and dependency relations adapted do UDv2
* Multiword expressions expanded (previously as single tokens)
* Complex proper nouns expanded (internal structure as flat:name)
* General review
* Added text (automatically from the tokenized sentence)

--- Machine readable metadata ---

Documentation status: partial

Data source: manual

Data available since: UD v1.4

License: LGPLLR

Genre: news

Contributors: Garcia, Marcos

Contact: marcos.garcia.gonzalez@udc.gal

