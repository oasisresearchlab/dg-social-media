---
title: "[[EVD]] - An SVM classifier trained on vocabulary from 40 model-estimated topics over subreddits was able to predict subreddits' political bias with 85% accuracy. - [[@kaneCommunitiesWeChoose2018]]"
url: https://roamresearch.com/#/app/dg-social-media-polarization/page/sikUtfWyf
author: Jay Patel
date: Thu Aug 17 2023 01:07:38 GMT-0400 (Eastern Daylight Time)
---

- Tags: #complete
- ## Summary of Results (with supporting snippets)
    - pg. 6, Table 3
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fdg-social-media-polarization%2F11lPvqQtFc.png?alt=media&token=38bd21fb-111f-4626-b409-e584d180a38c)
- ## Summary of Methods (with supporting snippets)
    - **Settings**: Reddit virtual community (p. 3, para 1)
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fdg-social-media-polarization%2FXzeC6mm3XY.png?alt=media&token=49d2a9f4-66ba-402f-b530-6029603cc5b9)
    - **Participants**: 3,385 active subreddit forums (p. 3, para 1)
    - **Measures**:
        - Subreddit texts, political corpora with Democrat and Republican phrases (p. 3-4, Section III)
        - Bias calculated using bigrams/trigrams correlations (p. 4, para 5)
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fdg-social-media-polarization%2FP_w0pNTeav.png?alt=media&token=25beb4b9-87de-455b-b1c8-80689210e5e3)
    - **Design**:
        - IV: Subreddit topic
        - DV: Subreddit political bias
    - **Sample size**:
        - 5 million Reddit comments
        - 3,385 subreddit forums
    - **Analytic techniques:**
        - Latent Dirichlet Allocation (LDA) used to model topics and group subreddits (p. 4, Section IV.A)
        - Political bias calculated using bigrams and trigrams compared to external political corpora (p. 4, Section IV.B)
            - Jaccard correlation between vocabulary of subreddit and "known" conservative or liberal
            - these external political corporal/datasets of bias are not described!
        - Classifier trained on LDA topics to predict subreddit bias (p. 5, Section IV.C)
        - **Details**
            - The authors used several analytic techniques to investigate the relationship between non-political group topics and political bias in Reddit communities.
            - First, they utilized a topic modeling technique called **Latent Dirichlet Allocation (LDA) to discover underlying topics across a large collection of Reddit comments. LDA is a probabilistic technique that identifies groups of words that tend to co-occur in documents**. By analyzing patterns of word co-occurrence, it determines a set number of topics that describe the collection. Each topic consists of the most probable words related to that topic. The researchers **used LDA to model 80 topics from all the subreddit documents**. They manually reviewed the top words in each topic to assign topic labels like "Sports" or "Music." This allowed them to group the thousands of subreddits into topics.
            - After using LDA to categorize the subreddits into topics, the researchers **calculated a political bias score for each individual subreddit**.
                - To do this, they compared the text of each subreddit to two external corpora containing known politically biased vocabulary. One corpus contained Republican and Democratic phrases from presidential speeches, and the other contained texts from partisan subreddits. They extracted frequent bigrams (two-word phrases) and trigrams (three-word phrases) from these political corpora to represent biased political language. For example, "climate change" occurred frequently among Democratic phrases while "religious freedom" was common in the Republican corpus.
            - To **quantify the bias of a subreddit, they calculated the overlap between the subreddit's bigrams/trigrams and those of each political corpus using a similarity metric called the Jaccard coefficient**.
                - This measures the number of bigrams/trigrams in common between two documents divided by the total number of unique bigrams/trigrams in both. The resulting scores were normalized to a 0-1 scale. By comparing a subreddit's language to each political corpus, they obtained separate liberal and conservative bias scores.
            - Then they **subtracted the conservative score from the liberal score to determine an overall bias score for each subreddit**, with positive scores indicating liberal bias and negative indicating conservative bias.
            - After calculating individual subreddit bias, they reported average bias scores for all subreddits within each LDA topic. This allowed them to examine relationships between topics and bias. Finally, to further analyze these relationships, they **trained a classifier using the LDA topics to predict subreddit political bias based on the vocabulary of a topic**. They tested different classifiers, finding SVM performed best with 85.2% accuracy, significantly above chance. This provided additional evidence of correlations between topics and biased language.
            - In summary, the authors leveraged LDA topic modeling to categorize subreddits and extract topics, calculated political bias scores for subreddits through comparisons with partisan phrase corpora, analyzed bias by topic, and trained a classifier on topics to predict bias. **The combination of techniques provided both qualitative and quantitative insights into how non-political topics relate to political biases in Reddit communities**
- ---
- [[ACL Recontextualizing Claims and Evidence Shared Task]] meta
    - Status:: #resultGrounded
    - Annotator::
    - ResultGrounding:: [[table]]

###### Discourse Context

- **Supports::** [[[[CLM]] - Topics in online communities are systematically politicized in their language.]]
