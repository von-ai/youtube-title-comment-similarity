# YouTube Title–Comment Similarity

A Natural Language Processing (NLP) system designed to analyze the semantic similarity between YouTube video titles and user comments in order to measure comment relevance to video content.

This project was developed as a final assignment for the Natural Language Processing course.

## Overview

This system analyzes text similarity using TF-IDF and Cosine Similarity, enhanced with Rule-Based Detection.
The output of the system is a binary label:
1 indicates that the comment is relevant (similar) to the video title
0 indicates that the comment is not relevant (not similar)

## Methodology

### Data Collection
User comments are collected using the YouTube Data API.
The dataset consists of 5 YouTube videos, with 500 comments collected from each video, resulting in a total of 1500 comments.

### Preprocessing
The preprocessing stage includes lowercasing all text, removing extra spaces, and eliminating non-alphanumeric characters.

### Text Similarity
Text representation is performed using TF-IDF vectorization.
Cosine Similarity is then calculated between the video title and each comment, using a similarity threshold of 0.78.

### Rule-Based Detection
- Several rules are applied to enhance the similarity detection:
- Comments with high similarity scores are considered relevant
- Short comments with dominant uppercase usage are considered relevant
- Comments containing excessive emojis combined with moderate similarity are considered relevant
- Comments that do not meet these criteria are labeled as not relevant

## Results

The analysis shows that approximately 90 percent of the comments are not semantically similar to the video titles.
This indicates that most YouTube comments do not directly reflect the context of the video titles.

## Future Improvements

Possible future enhancements include incorporating video transcripts, applying semantic embedding models such as Word2Vec or BERT, and improving contextual understanding of user comments.
