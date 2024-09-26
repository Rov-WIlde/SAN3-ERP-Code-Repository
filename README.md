# SAN3-ERP-Code-Repository

## Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation using UK Party Manifestos

This repository contains all of the code used to perform the analysis in the ERP "Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation, using UK Party Manifestos". 

The pipeline used consists of two components:
1)	**Topic Modelling** – BERTopic is applied to a corpus of sentence-segmented manifestos to identify issues parties emphasise, resulting in topic-labelled sentences whose frequency is used to measure issue-salience polarisation.
2)	**Cosine dissimilarity** – Politically-aware embeddings are used to calculate cosine dissimilarity between sentences of the same topic and election year across parties to measure issue-specific ideological polarisation.

## Environment Set-up
This project was done exclusively in Google Colab, which uses an isolated cloud environment when executing code. Therefore, it does not retain installed packages across sessions, and so all required packages must be installed at the start of each Colab notebook.

## Notebook - main.ipynb
This repository contains a single notebook that runs the full pipeline end-to-end using the manifestos included in the 'UK_manifestos' folder, and displays all of the figures present in the report so that results can be verified (note that the notebook must be open in Google Colab to view figure 3).

### Stage 1 - Importing and Pre-processing
- imports datasets contained in 'UK_manifestos', processes them and combines them into a single dataframe ready for topic modelling.

### Stage 2 - Topic Modelling
- handles topic modelling and produces two dataframes: 1) 'normalized_df' - contains normalised topic frequencies and 2) 'tm_results' - contains each sentence in the corpus along with topic, party and year labels.

### Stage 3 - Issue-salience Polarisation
- generates the normalised topic frequency graphs used to display issue-salience polarisation in figures 5, 7 and 8.

### Stage 4 - Issue-Specific Ideological Polarisation
- generates the topic-specific cosine dissimilarity graphs used to measure ideological polarisation in figures 6, 7, 8 and 11.
- generates the figure 9 graph that displays the cosine dissimilarity for Immigration between different embeddings types and the specific sentence examples used in figure 10.


## Reproducibility
It's important to note that the specific Python package versions used in the code are critical for achieving consistent results. Please use the same versions as those specified in the code.

