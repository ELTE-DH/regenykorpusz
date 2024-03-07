# ELTE Novel Corpus

The ELTE Novel Corpus is a continuously expanding database developed by the [_Department of Digital Humanities at Eötvös Loránd University_](https://elte-dh.hu/). Currently, the corpus contains 400 Hungarian novels. Besides the texts, the corpus contains the annotation of structural units and the grammatical features of words in TEI XML format. The novels of the corpus are from the 19th century and from the first half of the 20th century.

## Numeric properties:

- number of novels: 400
- number of authors: 119
- number of tokens: 26.8 million
- number of words: 21.4 million

## TEI Levels

The source of the corpus was the collection of the [_Hungarian Electronic Library_](http://mek.oszk.hu).

1. The texts from the Hungarian Electronic Library were converted into TEI XML format based on the [Text Encoding Initiative](https://tei-c.org/). The TEI XML files contain the annotation of structural units and the metadata of the novels. The conversion was partly done manually (level1).
2. Then, we tokenized the novels and annotated the grammatical features of words by using [e-magyar](https://github.com/nytud/emtsv), an NLP tool chain for Hungarian texts (level2).

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

# eltec folder:

The folder contains the level1 and level2 files with headers in the format of ELTeC. These files are not valid for TEI, we do not recommend to use these files. 

# Contributors:

- [Gábor Palkó](https://github.com/gaborpalko)
- [Tímea Borbála Bajzát](https://github.com/bajzattimi)
- Emma Takács
- Bence Vétek
- [Zsófia Fellegi](https://github.com/zsofiafellegi)
- [Péter Horváth](https://github.com/horvathpeti99)
- [Balázs Indig](https://github.com/dlazesz)
- [Bence Vida](https://github.com/VidaBence)
- [Botond Szemes](https://github.com/SzemesBotond)
- [Eszter Szlávich](https://github.com/sz-eszter)


All texts of the corpus are in the public domain.

