# SAN3-ERP-Code-Repository

## Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation, using UK Party Manifestos

This repository contains all of the code used to perform the analysis in the ERP "Towards a Natural Language Processing Pipeline for Measuring Types of Issue-specific Polarisation, using UK Party Manifestos". 

The pipeline used consists of two components:
1)	Topic Modelling – BERTopic is applied to a corpus of sentence-segmented manifestos to identify issues parties emphasise, resulting in topic-labelled sentences whose frequency is used to measure issue-salience polarisation.
2)	Cosine dissimilarity – Politically-aware embeddings are used to calculate cosine dissimilarity between sentences of the same topic and election year across parties to measure issue-specific ideological polarisation.

# Reproducibility
Its important to note that the specific Python package versions used in the code are critical for achieving consistent results. Please use the same versions as those specified in the code.

