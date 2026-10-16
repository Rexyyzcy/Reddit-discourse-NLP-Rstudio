# Reddit Discourse Analysis in R: Sentiment, Topics & Engagement

An exploratory text-analysis project from UCL's postgraduate **Applied Data Science module (SECU0057, 2024)**. I collected Reddit discussions about the Palestine–Israel conflict, cleaned and analysed the text in R, and wrote up the work as an 11-page, two-column research-style report (84 marks).

**At a glance:** 1,638 threads and 137,683 comments collected from 30 March to 30 April 2024; an end-to-end workflow covering collection, preprocessing, descriptive text analysis, sentiment scoring, LDA topic modelling, and regression on engagement.

| Start here | What it shows |
| --- | --- |
| [Final report](report/reddit-discourse-analysis-redacted.pdf) | Research question, methods, visualisations, findings, and limitations. |
| [R analysis notebook](analysis/Data-Science-Project-Code.Rmd) | Historical code for Reddit collection and text analysis. |
| [Selected tutorial exercises](tutorials/) | Three small R Markdown homework files from the same course, with my author line removed. |

## Methods and skills

- **Data collection:** used `RedditExtractoR` to collect thread metadata and comments from relevant subreddits and keyword searches.
- **Data preparation and NLP:** cleaned text, tokenised comments, and compared type–token ratio and Flesch–Kincaid readability across sources using R tools including `quanteda`.
- **Analysis:** applied a sentiment lexicon, trained a four-topic LDA model, and fitted a linear regression to explore associations with upvotes.
- **Communication:** wrote and typeset the two-column report in LaTeX using Overleaf, with figures and a discussion of limitations.

The report found differences in sentiment and themes across the sampled communities. Its regression explained only about **0.35%** of variation in upvotes, and the stance labels were exploratory rules derived from topics and sentiment rather than a validated classifier. These limits matter when interpreting the findings.

## Data and reproducibility

The raw comment archive is **not published here**. It includes usernames and the original text of 137,683 comments about a sensitive issue. The notebook records the historical collection steps, but reproducing them requires collecting data through currently permitted Reddit access methods and supplying the relevant sentiment lexicon. Its R chunks were saved with `eval = FALSE`, and I have not rerun the archived workflow for this publication.

The Week 2 exercise copy has its old Genius API credentials redacted. To use that API section, supply your own token through the `GENIUS_ACCESS_TOKEN` environment variable.

The report preserves the submitted analysis and layout. A former view-only link to a separate code archive was removed from its first page; no results were changed. The original source files on my computer were not modified. This repository is a portfolio archive, not a representative measure of public opinion or a current statement about the conflict.
