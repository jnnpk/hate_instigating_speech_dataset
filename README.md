# Hate Instigating Speech Dataset

## Overview
The Hate Instigating Speech Dataset is a collection of comments and replies from YouTube news channels, including CNN and Fox News in English and JTBC and TV Chosun in Korean. The dataset aims to provide a comprehensive resource for studying hate speech and its instigation in online discussions. It includes both raw data from the original sources and cleansed data that removes HTML tags and entities. The dataset is organized at both the comment and reply levels to analyze the impact of comments on subsequent replies. 

## Data Structure
The dataset comprises two main components:

### Hate Instigating Comments
- `commentID`: Unique identifier for each comment.
- `comment_text`: The text of the comment.
- `hate_instigation_level`: A measure of the comment's potential to incite hate speech.
- `hatespeech_or_not`: Indicates whether the comment contains hate speech or not.

### Hate Replies
- `replyID`: Unique identifier for each reply.
- `reply_text`: The text of the reply.
- `hatespeech_or_not`: Indicates whether the reply contains hate speech or not.

## Data Collection
The dataset was collected from major news media companies' YouTube channels in the United States and South Korea. Specifically, the channels included were CNN, Fox News, JTBC, and TV Chosun. Data was gathered using the YouTube Data API, covering videos posted between January 2022 and April 2022. In total, the dataset includes 4,165 comments and 11,310 replies from 210 videos, with the breakdown as follows:
- CNN: 46 videos, 935 comments, 2,499 replies
- Fox News: 44 videos, 980 comments, 2,592 replies
- JTBC: 45 videos, 1,018 comments, 3,496 replies
- TV Chosun: 75 videos, 1,232 comments, 2,723 replies

## Annotation Process
The primary objective of this dataset is to label comments as hate instigating speech or not. The annotation process involved two key steps:

1. **Labeling Replies:** Replies associated with each comment were labeled as either hate speech or non-hate speech. 

2. **Measuring Hate Speech Instigation:** The level of hate speech instigation at the comment level was determined by examining the ratio of hate replies to the total number of replies.

## Hate Speech Definitions

- **Hate Speech:** Speech that deliberately targets a specific group or individual for condemnation. This includes but is not limited to sexism, homophobia, and hate towards certain political groups. Additionally, aggressive speech without a specific target also falls under this category.

- **Non-Hate Speech:** Speech that does not fall under the above categories. Criticism and sarcasm are examples of non-hate speech.

## Contributors
The main contributors of the work are:

- Kyuhan Lee
- Hyoungjun Park
- Hosung Shim
- Jangsun Park
- Hyerin Kim
