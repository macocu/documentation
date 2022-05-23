# MaCoCu Documentation

The textual data included in the corpora built in MaCoCu project are obtained by mostly crawling the national top-level domains of the countries where the targeted languages are official.

Textual data is then processed with a monolingual and a parallel curation pipelines to produce the final version of
the corpora. The tools and models used to produce the corpora released in this project are publicly available: 

- MaCoCu crawler: https://github.com/macocu/MaCoCu-crawler
  - Web crawler used to retrieve documents from Top Level Domains (TLD).
- Bitextor: https://github.com/bitextor/bitextor/releases/tag/macocu-data-1
  - Pipeline that aligns monolingual crawled documents into bitexts.
- Bifixer: https://github.com/bitextor/bifixer
  - Tool to fix bitexts and tag near-duplicates for removal.
- Bicleaner AI: https://github.com/bitextor/bicleaner-ai (models used: https://github.com/bitextor/bicleaner-ai-data/releases/tag/v1.0)
  - Tool that aims at detecting noisy sentence pairs in a parallel corpus.
- Monotextor: https://github.com/bitextor/monotextor/releases/tag/v1.0
  - Pipeline that processes monolingual crawled documents.
- Monofixer: https://github.com/bitextor/bifixer#monofixer
  - Tool to fix segments and tag near-duplicates for removal.
- Monocleaner: https://github.com/bitextor/monocleaner
  - Tool that aims to detect disfluent sentences in a monolingual corpus.
- ROAM: https://github.com/bitextor/biroamer
  - Utility that will help you to ROAM (Random, Omit, Anonymize and Mix) your corpus and detect entities in text.
- American/British English variant classifier: https://github.com/macocu/American-British-variety-classifier
  - A minimalistic spelling- and vocabulary-based American-vs-British variety classifier.
- DSI classification: https://github.com/macocu/DSI
  - Tools for DSI classification tasks in MaCoCu project.
- Translation direction detection: https://github.com/RikVN/TranslationDirection
  - Code for determining translation direction of parallel sentences
