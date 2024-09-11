---
title: "[[EVD]] - LDA modeling showed that overall political bias varied significantly across subreddits . - [[@kaneCommunitiesWeChoose2018]]"
url: https://roamresearch.com/#/app/dg-social-media-polarization/page/S3Jz8Rq0j
author: Joel Chan
date: Tue Jul 18 2023 03:18:00 GMT-0400 (Eastern Daylight Time)
---

- ## Summary of Result (with supporting snippets)
    - pg. 5
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fdg-social-media-polarization%2FSk6x7kbDe1.42.37.png?alt=media&token=4dc0fa42-fc0a-4f31-b30a-e5c87a97bb95) (Figure 4)
- ## Summary of Methods (with supporting snippets)
    - pgs. 2-3
    - **Data pipeline**
        - May 2015: Reddit
            - 3,385 most active subreddits (>500 comments/month)
            - selected comments passing a score-threshold (_s_ > 5)
                - remove comments < 10 characters long
            - final dataset: 5 million comments
                - Fig. 1 shows an example comment
                    - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fdg-social-media-polarization%2FauxO4hCmUE.35.14.png?alt=media&token=c1658cc9-bd0b-4321-bfa2-d09569b5566d)
            - Political vocab corpora
                - 2016 US presidential debates
                    - 400 lines est. per party
                - May 2015 dataset
                    - various political subreddits: Liberal, Progressive, Socialism, Conservative
    - **Measure of political bias**
        - Political bias = Liberal bias index - Conservative bias index
            - liberal = pos. score
            - conservative = neg. score
- ---
- [[ACL Recontextualizing Claims and Evidence Shared Task]] meta
    - Status:: #resultGrounded
    - Annotator::
    - ResultGrounding:: [[figure]]

###### Discourse Context

- **Supports::** [[[[CLM]] - LDA modeling is an accurate and useful way to capture bias on social media sites relative to clustering.]]
