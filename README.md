# SAN3-ERP-Code-Repository

## Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation, using UK Party Manifestos

This repository contains all of the code used to perform the analysis in the ERP "Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation, using UK Party Manifestos". 

The pipeline used consists of two components:
1)	Topic Modelling – BERTopic is applied to a corpus of sentence-segmented manifestos to identify issues parties emphasise, resulting in topic-labelled sentences whose frequency is used to measure issue-salience polarisation.
2)	Cosine dissimilarity – Politically-aware embeddings are used to calculate cosine dissimilarity between sentences of the same topic and election year across parties to measure issue-specific ideological polarisation.

## Environment Set-up
This project was done exclusively in Google Collab, which uses an isolated cloud environment when executing code. Therefore, it does not retain installed packages across sessions, and so all required packages must be installed at the start of each Colab notebook.

## Notebooks
This repository contains 5 separate Google Collab Notebooks:

### preprocessing.py
- imports datasets contained in 'UK_manifestos', processes them and combines them into a single dataframe ready for topic modelling.

### topic_modelling.py
- handles topic modelling and produces two dataframes: 1) 'normalized_df' - contains normalised topic frequencies and 2) 'tm_results' - contains each sentences in the corpus along with topic, party and year labels.

### issue_salience.py
- generates the normalised topic frequencies graphs used to display issue-salience polarisation in figures 5,7 and 8.

### cosine_dissimilarity.py
- generates the topic-specific cosine dissimilarity graphs used to measure ideological polarisation in figures 6,7,8 and 11.

### main.py
- A final notebook that ties all of the scripts together to run the full pipeline end-to-end and displays all of the figures present in the report so that results can be verified.


## Reproducibility
It's important to note that the specific Python package versions used in the code are critical for achieving consistent results. Please use the same versions as those specified in the code.

