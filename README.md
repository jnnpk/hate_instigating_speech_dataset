# Hate Instigating Speech Dataset

## Overview
The Hate Instigating Speech Dataset is a collection of comments and replies from YouTube news channels, including CNN and Fox News in English and JTBC and TV Chosun in Korean. The dataset aims to provide a comprehensive resource for studying hate speech and its instigation in online discussions. It includes both raw data from the original sources and cleansed data that removes HTML entities. The dataset is organized at both the comment and reply levels to analyze the impact of comments on subsequent replies. 

## Paper
[Paper](https://aclanthology.org/2023.findings-emnlp.412.pdf)

## Data Structure
The dataset comprises two main components:

### Hate Instigating Comments
- `commentID`: Unique identifier for each comment.
- `comment_text`: The text of the comment.
- `hate_instigation_level`: A measure of the comment's potential to incite hate speech(0~1).
- `hatespeech_or_not`: Indicates whether the comment contains hate speech(1) or not(0).

### Hate Replies
- `replyID`: Unique identifier for each reply.
- `reply_text`: The text of the reply.
- `hatespeech_or_not`: Indicates whether the reply contains hate speech(1) or not(0).

## Data Collection

Data was gathered using the YouTube Data API, covering videos posted between January 2022 and April 2022. In total, the dataset includes 4,165 comments and 11,310 replies from 210 videos, with the breakdown as follows:

### English

- CNN: 46 videos, 935 comments, 2,499 replies
- Fox News: 44 videos, 980 comments, 2,592 replies

### Korean

- JTBC: 45 videos, 1,018 comments, 3,496 replies
- TV Chosun: 75 videos, 1,232 comments, 2,723 replies

## Annotation Process
The primary objective of this dataset is to label comments as hate instigating speech or not. Specifically, by examining the level of hatred presented in the replies to a comment, we can identify the level of hate instigation associated with that comment. The annotation process involved two key steps:

1. **Labeling Replies:** Replies associated with each comment were labeled as either hate speech or non-hate speech by three annotators through majority voting.

2. **Measuring Hate Speech Instigation:** The level of hate speech instigation at the comment level can be determined by examining the ratio of hate replies to the total number of replies. Nevertheless, the approach to defining hate speech instigation may vary. Rather than assigning a continuous ratio of hate speech instigation levels to comments, they can alternatively be categorized into binary labels based on a specific threshold.

## Hate Speech Definitions

**Hate Speech:** Speech that deliberately targets a specific group or individual for condemnation. This includes but is not limited to sexism, homophobia, and hate towards certain political groups. Additionally, aggressive speech without a specific target also falls under this category.

  Examples:
- Explicit hatred towards a particular group: *"INDIA + CHINA = DISGUSTING RAT EATING 3RD WORLD COUNTRIES!"*
- Hate towards a political group: *"Biden Is the biggest Disaster in American History 😫"*
- Sexism: *"She is a woman; it's hard for women to understand things like this."*
- General aggression: *"YouTube comments are such a cesspit."*

**Non-Hate Speech:** Speech that does not fall under the above categories. Criticism and sarcasm are examples of non-hate speech.

  Examples:
- Sarcasm: *"Wow, what a surprise, American."*
- Criticism: *"I'm part Russian and absolutely disappointed in this whole war!"*

The definitions and examples are based on prior literature (Assimakopoulos et al., 2020; Mulki et al., 2019; Pavlopoulos et al., 2017; Davidson et al., 2017; Mathur et al., 2018; Sigurbergsson and Derczynski, 2019).

## Contributors
The primary contributors for this project can be found in the Information Systems(IS) at Korea University:

- Kyuhan Lee
- Hyoungjun Park
- Ho sung Shim
- Jangsun Park
- Hyerin Kim
