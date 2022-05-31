# Software developed for the MaCoCu Action

Massive collection and curation of monolingual and bilingual data: focus on under-resourced languages (MaCoCu) is an action funded by the European Union's Connecting Europe Facility 2014-2020 - CEF Telecom, under Grant Agreement No. INEA/CEF/ICT/A2020/2278341. The project focuses on collecting monolingual and parallel data from the Internet, specially for under-resourced languages and DSI-specific data. All the software developed for this action will be released under free/open-source licenses.

At the moment, the first data release has been published for seven languages targeted in the Action: Bulgarian, Croatian, Icelandic, Maltese, Macedonian, Slovene, Turkish. The steps followed to collect this data started with a top-level domain crawling process. In this way, the national top-level domains of the countries where the targeted languages are official plus several generic top-level domains, such as .eu, .com, or .org, were crawled for a few months, and all the documents downloaded in the targeted languages (and also in English) were stored. The tool used for this purpose was the [MaCoCu crawler](https://github.com/macocu/MaCoCu-crawler).

Crawled documents were then processed using two pipelines: [Monotextor](https://github.com/bitextor/monotextor/), aimed at building monolingual corpora, [Bitextor](https://github.com/bitextor/bitextor), aimed at building parallel corpora. The specific versions of the pipelines used to produce the corpora included in the first data release, are:
- Bitextor: https://github.com/bitextor/bitextor/releases/tag/macocu-data-1
- Monotextor: https://github.com/bitextor/monotextor/releases/tag/v1.0

The main purpose of Bitextor is to preprocess, identify and align parallel content within a collection of multilingual documents. However, it also includes several curation components aimed at improving the quality of the final corpora. These components are:
- [Bifixer](https://github.com/bitextor/bifixer): Tool to fix typos and minor errors in a parallel corpus, and tag near-duplicates for removal.
- [Bicleaner AI](https://github.com/bitextor/bicleaner-ai): Tool that aims at detecting noisy sentence pairs in a parallel corpus. The models used for the first data release in MaCoCu are available at: https://github.com/bitextor/bicleaner-ai-data/releases/tag/v1.0)
- [BiROAMer](https://github.com/bitextor/biroamer): Utility that will help you to ROAM (Random, Omit, Anonymize and Mix) your corpus and detect entities in text.

Apart from these components integrated in the pipeline, two independent tools were also applied on the clean corpora to enrich them with metadata. These two components are:
- a minimalistic [American/British English variant classifier](https://github.com/macocu/American-British-variety-classifier) based on spelling- and vocabulary, and
- a [translationese detector](https://github.com/RikVN/TranslationDirection) to determine translation direction of parallel sentences, this is, to identify which sentence is the original and which is the translation.

The Monofixer pipeline is aimed at building monolingual corpora from a collection of multilingual documents. One of the key components of this pipeline is: [Monocleaner](https://github.com/bitextor/monocleaner), a tool that aims at detecting disfluent sentences in a monolingual corpus. For the first data release of the project, BiROAMer was also used on machine-translated content to identify fragments of text containing personal data.

Finally, the first data release of the project contains a version of the English-Spanish and English-Dutch parallel corpora from the [Paracrawl project](https://paracrawl.eu) with DSI relevance probabilities, which are computed by the [MaCoCu DSI](https://github.com/macocu/DSI) tool. This tool provides, given a pair of segments, how relevant they are for a specific DSI among the list of targeted DSIs in the MaCoCu project: e-Health, e-Justice, Online Dispute Resolution, Europeana, Open Data Portal, Business Registers Interconnection System, e-Procurement, Safer Internet, Cybersecurity, and Electronic Exchange of Social Security Information.

## Disclaimer
The contents of this document are the sole responsibility of the members of the MaCoCu consortium, and do not necessarily reflect the opinion of the European Union. 
