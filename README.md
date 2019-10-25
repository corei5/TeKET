# TeKET

TeKET is an open source python-based keyphrase extraction toolkit. It provides an end-to-end keyphrase extraction pipeline in which each component can be easily modified or extended to develop new models. TeKET also allows for easy benchmarking of state-of-the-art keyphrase extraction models.

dist: xenial
language: python
python:
  - "3.7"
# command to install dependencies
install:
  - pip install -r requirements.txt
  - python -m nltk.downloader stopwords
  - python -m nltk.downloader universal_tagset
  - python -m spacy download en
script:
  - pytest
