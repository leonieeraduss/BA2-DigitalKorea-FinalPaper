# Political Orientation and Linguistic Patterns in South Korean News Tweets

This corpus-based study investigates whether political orientation can be detected through linguistic patterns in South Korean newspaper tweets. A corpus of 2,745 tweets from left- and right-leaning newspapers published between July and August of 2017 is analyzed using computational text analysis in Orange Data Mining.

The analysis focuses on whether differences in language use between ideological groups are strong enough to create distinguishable linguistic patterns.

## Research Question

Can linguistic patterns reveal political orientation in South Korean newspaper tweets?

## Headline Finding

The results show that political orientation is only mildly reflected in differences in language use. While some variation in topic emphasis exists between left- and right-leaning outlets, the overall vocabulary is overlapping a lot, and both groups participate in the same political discourse. Distinctive terms are mainly topic-based rather than ideological, and no clear ideological clustering is observed.

## Methods Overview

The analysis is conducted in Orange Data Mining using the following pipeline:

File → Corpus → Python Script (Kiwi tokenization) → Corpus → Preprocess Text (custom stopwords) → Select Columns → Bag of Words (TF-IDF)  
→ Select Rows (left) → Word Clouds → Data Table  
→ Select Rows (right) → Word Clouds → Data Table  
→ Rank  
→ t-SNE

## How to Reproduce

1. Open Orange Data Mining (version specified in `requirements.md`)
2. Load the dataset using the File widget
3. Run the workflow provided in `analysis/Final Workflow.ows`
4. Ensure the custom stopword list is included in preprocessing
5. Generate figures in Orange:
   - Word clouds
   - Rank results
   - t-SNE visualization
6. Export figures
