# ELTE Novel Corpus

The ELTE Novel Corpus is a database developed by the [_Department of Digital Humanities at Eötvös Loránd University_](https://elte-dh.hu/). Currently, the corpus contains 601 Hungarian novels. Besides the texts, the corpus contains the annotation of structural units and the grammatical features of words in TEI XML format. The novels of the corpus are from the 19th century and from the first half of the 20th century.

## Numeric properties:

- number of novels: 601
- number of authors: 174
- number of tokens: 36.6 million
- number of words: 29.2 million

## Metadata of the novels:

The metadata.tsv file contains the main metadata for each novel.

## TEI Levels

The source of the corpus was the collection of the [_Hungarian Electronic Library_](http://mek.oszk.hu).

1. The texts from the Hungarian Electronic Library were converted into TEI XML format based on the [Text Encoding Initiative](https://tei-c.org/). The TEI XML files contain the annotation of structural units and the metadata of the novels. The conversion was partly done manually (level1).
2. Then, we tokenized the poems and annotated the grammatical features of words by using [_e-magyar_](https://github.com/nytud/emtsv), an NLP tool chain for Hungarian texts. The level2 folder contains the TEI XML files in which the morphosyntactic features (values of the msd attributes) are annotated in the format of universal dependencies, while the level2\_emMorph folder contains the same files in which the morphosyntactic features are annotated in its own, [_emMorph_](https://e-magyar.hu/en/textmodules/emmorph_codelist) format of e-magyar.

# eltec folder:

The folder contains the level1 and level2 files with headers in the format of [ELTeC](https://www.distant-reading.net/eltec/). These files are not valid for TEI, we do not recommend to use them. 

# Elements and attributes

## Level1 -- annotation of structural units and adding metadata to texts

- `<ns1:authorGender/>` : sex of author
	- `M` : male
	- `F` : female
- `<ns1:size/>` : size of the novel
	- `short` : 10 000 -- 49 999 words
	- `medium` : 50 0000 -- 99 999 words
	- `long` : more than 100 000 words 
- `<ns1:canonicity/>` : canonicity level of the novel 
	- `low` : 0 or 1 edition after 1979
	- `high` : 2 or more edition after 1979
- `<ns1:timeSlot/>` : time period of the first edition of the novel
	- `T0` : before 1840
	- `T1` : 1840--1860
	- `T2` : 1860--1880
	- `T3` : 1880--1900
	- `T4` : 1900--1920 
	- `T5` : after 1920
- `<head>` : title
- `<div>` : part, chapter
- `<milestone>` : delimiter of subchapters
- `<p>` : paragraph

## Level2 -- tokenization and annotation of grammatical features of words

- `<s>` : sentence
- `<w>` : word
- `<pc> `: punctuation mark
- `@lemma` : lemma
- `@pos `: part of speech
- `@msd` : morphosyntactic features ([Universal Dependencies](https://universaldependencies.org/))

# Contributors:

- [Gábor Palkó](https://github.com/gaborpalko)
- [Tímea Borbála Bajzát](https://github.com/bajzattimi)
- [Péter Horváth](https://github.com/horvathpeti99)
- Emma Takács
- Bence Vétek
- [Zsófia Fellegi](https://github.com/zsofiafellegi)
- [Balázs Indig](https://github.com/dlazesz)
- [Bence Vida](https://github.com/VidaBence)
- [Botond Szemes](https://github.com/SzemesBotond)
- [Eszter Szlávich](https://github.com/sz-eszter)


# License

The content of the repository is licensed under the [CC BY-NC-ND](https://creativecommons.org/licenses/by-nc-nd/4.0/) license.

All texts of the corpus are in the public domain.

# Acknowledgements

The authors acknowledge the support of the National Laboratory for Digital Heritage.
Project no. 2022-2.1.1-NL-2022-00009 has been implemented with the support provided by
the Ministry of Culture and Innovation of Hungary from the National Research, Development
and Innovation Fund, financed under the 2022-2.1.1-NL funding scheme.
