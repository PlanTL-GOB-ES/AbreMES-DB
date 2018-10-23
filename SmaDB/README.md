# SmaDB: Spanish Medical Abbreviations DataBase

This folder contains the full database. Users are free to make the adaptations they need and prefer.

This README file explains each file in the folder:

### abbreviations.tsv

This file gathers all abbreviations in the database and displays information about them. Each column is structured the following way:
- Abbreviation ID.
- Frequency: the number of times the abbreviation has been detected in the corpora, together with the definition in the same sentence.
- Abbreviation: the abbreviation in string format.
- Definitions: definition IDs where the abbreviation has been associated to.
- Appears on: publication IDs where the abbreviation has been mentioned.

### definitions.tsv

This file gathers all definitions in the database and displays information about them. Each column is structured in the following way:
- Definition ID.
- Frequency: the number of times the definition has been detected in the corpora, together with the abbreviation in the same sentence.
- Definition: the definition in string format.
- Abbreviations: abbreviation IDs where the definition has been associated to.
- Appears on: publication IDs where the definition has been mentioned.

### pairs.tsv

This file gathers all abbreviation-definition pairs found in the corpora and displays information about them. Each column is structured in the following way:
- Pair ID.
- Abbreviation ID.
- Definition ID.
- Frequency: the number of times this abbreviation-definition pair has been detected in the corpora.
- Abbreviation: abbreviation in string format.
- Definition: definition in string format.
- Appears on: publication IDs where we the pair is mentioned.

### CoAbbreviations.tsv

This file gathers all abbreviations found in the corpora, and gathers those abbreviations with whom they share publications. Each column is structured in the following way:
- Abbreviation ID.
- Abbreviation: the abbreviation in string format.
- Co-Abbr frequency: the number of times other detected abbreviations appear in the same publication with the current abbreviation.
- Pub. frequency: the number of publications the abbreviation appears in the analyzed corpora, together with the definition explicitly mentioned in the same sentence.
- Co-abbreviations: abbreviation IDs that appear in the same publication.
- Appears on: publication IDs where we this abbreviation is mentioned.

### publications.tsv

This file gathers all analyzed publications in the corpora, and gathers those abbreviation-definition pairs that have been detected in each publications. Each :
- ID: the publications's official ID.
- Source: the name of the source where the publication can be found.
- Date: the day the publications was published.
- Publisher: publisher of the article.
- ISSN: ISSN of the journal where the article was published.
- Journal Subject Term: research field of the article.
- Abbreviations: all abbreviation IDs of the abbreviations that have been detected in the publications.
- Definitions: all definition IDs of the definitions that have been detected in the publications.
- Pairs: abbreviation-definition pair IDs that appear in the article.

### preprocessed.tsv

This is a file created after gathering all abbreviation-definition pairs detected in all the publication of the corpora. We use this file as a base to organize all the information specified in the previous files. In each line we can find:
- Line num.: an ID for each line.
- Pub. ID: official ID of each publication.
- The name of the source where the publication can be found.
- The year the article was published.
- Abbreviation ID present in the article.
- Definition ID of the abbreviation, mentioned explicitly in the document in the same sentence.
- Abbreviation in string format.
- Definition in string format.
