# BJUT-HCD
This repository provides a dataset of short videos about homogeneous content.
![image](https://github.com/BJUT-AIVBD/HCD/blob/main/Fig1.png)

## Introduction
Specifically designed for homogenization recognition, the self-built BJUT-HCD covers a wide range of video topics with a total of 23 types of homogeneous content, including emotion, news, entertainment, fun, and creative editing categories.

## Download the dataset
The way to download the dataset and the examples of short vides are stored in the "homogeneous_content_dataset".

## Cite this repository
If you use this software in your work, please cite it using the following metadata.
Shuying Zhang, Jing Zhang, Hui Zhang, and Li Zhuo. (2023). HCD by BJUT-AI&VBD [Computer software]. https://github.com/BJUT-AIVBD/HCD

# BJUT-HCD_S

BJUT-HCD_S is a large-scale Chinese semantic textual similarity dataset designed for text semantic understanding in video-related content scenarios. It is constructed for evaluating the ability of models to measure fine-grained semantic similarity between Chinese sentence or paragraph pairs.

## Introduction

With the rapid growth of short-video platforms, textual content associated with videos, such as subtitles, descriptions, comments, and topic summaries, has become increasingly diverse and semantically complex. Many video-related texts are expressed in informal, conversational, or rewritten forms, making semantic similarity estimation more challenging than conventional short-sentence matching.

BJUT-HCD_S contains 5,000 Chinese subtitle-oriented text pairs, including 4,000 training pairs, 500 development pairs, and 500 test pairs. Each sample consists of two Chinese subtitle-style texts at the sentence or paragraph level and a semantic similarity score ranging from 0.0 to 5.0, where 0.0 indicates complete semantic irrelevance and 5.0 indicates highly similar or semantically equivalent meanings.

The dataset contains 5,000 sentence pairs, including 4,000 training pairs, 500 development pairs, and 500 test pairs.

## Dataset Statistics

| Split | Number of pairs |
| ----- | --------------: |
| Train |           4,000 |
| Dev   |             500 |
| Test  |             500 |
| Total |           5,000 |

## Score Definition

The semantic similarity score ranges from 0.0 to 5.0.

| Score range | Description                                            |
| ----------- | ------------------------------------------------------ |
| 0.0         | Completely unrelated semantics                         |
| 1.0         | Weak or indirect semantic relation                     |
| 2.0         | Partially related but with major semantic differences  |
| 3.0         | Moderately related with overlapping topics or meanings |
| 4.0         | Highly related with minor semantic differences         |
| 5.0         | Highly similar or semantically equivalent              |

## Data Format

Each data instance contains two Chinese texts and a semantic similarity score.

Recommended file format:

```csv
id,sentence1,sentence2,score
1,"Chinese text A","Chinese text B",4.2
2,"Chinese text A","Chinese text B",1.0
```

The dataset can also be stored in JSONL format:

```json
{"id": 1, "sentence1": "Chinese text A", "sentence2": "Chinese text B", "score": 4.2}
{"id": 2, "sentence1": "Chinese text A", "sentence2": "Chinese text B", "score": 1.0}
```

## Domain Coverage

BJUT-HCD_S covers diverse video-related textual scenarios, including but not limited to:

* psychology and mental health;
* real estate investment and market analysis;
* pet care and animal health;
* agricultural planting techniques;
* entertainment content, such as dancing, music, and musical instrument learning;
* workplace communication and management.

This cross-domain design enables the dataset to evaluate semantic understanding under different contexts, topics, writing styles, and levels of semantic overlap.

## Text Characteristics

The texts in BJUT-HCD_S are mostly paragraph-level Chinese texts. They include both informal expressions, such as short-video comments, life-sharing texts, and conversational descriptions, and more formal expository texts, such as market analysis and professional knowledge explanations.

Therefore, BJUT-HCD_S reflects the diversity of Chinese video-platform text and provides a challenging benchmark for long-text semantic similarity estimation.

## Example Texts

The following examples illustrate the style and domain coverage of the dataset.

### Real Estate

> 房贷利率又降了！央行最新LPR报价下调，5年期以上LPR降至历史低点，这意味着月供压力将减轻。以贷款100万、30年期为例，每月可少还约150元。但别高兴太早，银行实际执行利率可能因个人信用、地区政策而异。建议近期有购房计划的朋友，多对比几家银行的房贷产品，同时优化自身征信记录，争取更低利率。这波政策红利，你抓住了吗？

### Agriculture

> 阳台种菜最怕啥？虫害啊！尤其是那种小白飞虫，密密麻麻的特别烦人。我最近发现一个土办法，用大蒜水喷叶面，三天喷一次，连续两周，虫子少了一大半！天然无污染，种出来的菜吃着也放心。

### Education

> 今天想和大家深入探讨一个常被忽视但至关重要的英语学习误区：过度依赖语法规则。很多学习者花费大量时间背诵复杂的语法条款，却在实际交流中结结巴巴，这正是因为将语言学习等同于数学公式推导。语言本质上是沟通工具，其核心在于流利表达和意义传递。

## Intended Use

BJUT-HCD_S is suitable for training and evaluating models for:

* Chinese semantic textual similarity estimation;
* sentence and paragraph embedding learning;
* ranking-based sentence generation;
* video content retrieval;
* recommendation systems;
* cross-modal semantic matching;
* fine-grained semantic similarity ranking.

In particular, the dataset is well suited for evaluating sentence embedding models trained with Ranking Sentence Generation or other ranking-oriented supervision strategies.
