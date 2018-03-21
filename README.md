# Summary

The Galician-TreeGal is a treebank for Galician developed at LyS Group (Universidade da Coruña).

# Introduction

The resource derives from a subset (called *xeral*) of the XIADA corpus (v2.6), created at the Centro Ramón Piñeiro para a Investigación en Humanidades (http://corpus.cirp.es/xiada/).

All the information except the syntactic one was semi-automatically converted to UD from the original resource. The dependency labels were assigned using cross-lingual parsing techniques, and then manually corrected by a linguist (see the references for more information).

Galician-TreeGal v0.4 contains 1000 sentences of the xeral corpus (~25k tokens), and it is divided 20-40-40 splits (train-dev-test).

# Differences from the generic Galician guidelines

## Morphology

### Tags
* The Galician-TreeGal treebank uses [AUX]() also in the following cases:
  * Pseudo-copulative verbs: are tagged as [AUX]() when they function as copula (e.g., "Miguel Barros *permanecerá*
relegado").
  * Modal, temporal and aspectual verbs: These verbs are considered auxiliary of the verb they depend on (e.g., "*debe* conducirnos" or "*deixa* de ser"). Similarly, auxiliary verbs in verbal periphrases are also tagged as [AUX]() (e.g., "*vai* gañar").

### Features
* The Galician-TreeGal treebank uses the following morphological features:
  * Nouns have inherent or inflected [Gender]() (common, feminine, or masculine) and [Number]() (singular or plural).
  * Verbs can have four different [VerbForm]() features (finite, gerund, participle, or infinitive):
    * Forms in participle inflect in [Gender]() (feminine or masculine) and in [Number]() (singular or plural).
    * Both finite and infinitive verb form may inflect for [Number]() (singular or plural) and for [Person]() (1, 2, 3).
    * Finite forms also inflect in [Tense]() (present, future, past, imperfect, and pluperfect) and [Mood]() (indicative, subjuntive, imperative, and conditional).
  * Adjectives agree with nouns with respect to the features [Gender]() and [Number](). In addition, some adjectives inflect for [Degree]() (comparative, superlative).
  * Negative adverbs have negative [Polarity]() in Galician-TreeGal. Also, relative and interrogative adverbs are labeled with *Rel* and *Int* [PronType](), respectively.
  * Few adpositions (e.g., *sen*) and conjunctions (*nin*) are also labeled with a negative polarity.
  * [PronType]() is used to differentiate the following pronouns and determiners: Demonstrative, indefinite, relative, interrogative, personal, and article. Personal (Prs) stands for personal and for possessive pronouns and determiners ([Poss] disambiguates between these two types). [PRON]() Articles (Art) are those determiners acting as pronouns (heads) when a noun is elided (e.g., "*a* [elided noun] de Abel")).
  * Determiners and pronouns inflect for [Number]() (singular or plural) and for [Gender]() (feminine, masculine, common, and neutral).
  * Possessive determiners and pronouns ([Poss]()) also have a language-specific feature: [Number[psor]]() (singular or plural).
  * Clitic pronouns inflect for [Case]() with three values (nominative, accusative, dative).
  * Determiners agree with nouns in the same way as adjectives.

For more information, see the list of [Galician features](/feat/index.html) and Garcia, Marcos (2016), [Universal Dependencies Guidelines for the Galician-TreeGal Treebank](http://www.grupolys.org/~marcos/papers/GL_UD_guidelines.pdf).

## Syntax

* Apart from the verbs *ser*, *estar*, and *parecer*, Galician-Treegal labels as [aux] pseudo-copulative verbs as well as modal, temporal and aspectual auxiliary verbs (see the POS-tags section above).

# Acknowledgments

* Garcia, Marcos, 2016. *Universal Dependencies Guidelines for the Galician-TreeGal Treebank.* Technical Report. LyS Group, Universidade da Coruña.

* Garcia, Marcos, Carlos Gómez-Rodríguez and Miguel A. Alonso, 2018. *New treebank or repurposed? On the feasibility of cross-lingual parsing of Romance languages with Universal Dependencies.* Natural Language Engineering, 24(1): 91-122.

* Rojo, Guillermo, Marisol López Martínez, Eva Domínguez Noya and Fco. Mario Barcala, 2015. *Corpus de adestramento do Etiquetador/Lematizador do Galego Actual (XIADA),* v2.6. Centro Ramón Piñeiro para a Investigación en Humanidades.

# Stats
* Tree count:  1000
* Word count:  25548
* Token count: 23478
* Dep. relations: 37 of which 4 language specific
* POS tags: 16
* Category=value feature pairs: 44

# Issues
* There are a few tokens with blank spaces (telephone numbers: "xxx xxx xxx").
* The morphological features of some tokens (analyzed as part of proper nouns in the original corpus) are not available.
* The dependency labels need to be reviewed by another expert to calculate inter-annotator agreement.

# Changelog
* 2018-03-21 v0.41:
  * Few features and POS corrections.
  * 'orphan' dependency correction.

* 2017-06-02 v0.4:
  * POS-tags, morphological features and dependency relations adapted do UDv2.
  * Multiword expressions expanded (previously as single tokens).
  * Complex proper nouns expanded (previously as single tokens).
  * General review.
  * Added original text.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Documentation status: partial
Data source: manual
Data available since: UD v1.4
License: LGPLLR
Genre: news
Includes text: yes
Lemmas: manual native
UPOS: manual native
XPOS: manual native
Features: converted with corrections
Relations: manual native
Contributors: Garcia, Marcos
Contributing: elsewhere
Contact: marcos.garcia.gonzalez@udc.gal
===============================================================================
</pre>
