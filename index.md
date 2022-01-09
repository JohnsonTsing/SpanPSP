---
layout: default
---

# Abstract

The accuracy of prosodic structure prediction is crucial to the naturalness of synthesized speech in Mandarin text-to-speech system, but now is limited by widely-used sequence-to-sequence framework and error accumulation from previous word segmentation results. In this paper, we propose a span-based Mandarin prosodic structure prediction model to obtain an optimal prosodic structure tree, which can be converted to corresponding prosodic label sequence. Instead of the prerequisite for word segmentation, rich linguistic features are provided by Chinese character-level BERT and sent to encoder with self-attention architecture. On top of this, span representation and label scoring are used to describe all possible prosodic structure trees, of which each tree has its corresponding score. To find the optimal tree with the highest score for a given sentence, a bottom-up CKYstyle algorithm is further used. The proposed method can predict prosodic labels of different levels at the same time and accomplish the process directly from Chinese characters in an end-to-end manner. Experiment results on two real-world datasets demonstrate the excellent performance of our span-based method over all sequenceto-sequence baseline approaches.

# Subjective Evaluation

|         |    Method     | Chinese text | Audio |
|:--|:---------|:---------------------------------------|:------|
| 1 | Baseline | 中国是禁止涉外婚介的，不信你可以上网查查。|<audio controls><source src="./wavs/Baseline/b01.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 中国是禁止涉外婚介的，不信你可以上网查查。 |<audio controls><source src="./wavs/Proposed/p01.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 2 | Baseline | 其次，玉米食用油尤其是玉米胚芽油正越来越多的推向市场。|<audio controls><source src="./wavs/Baseline/b02.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 其次，玉米食用油尤其是玉米胚芽油正越来越多的推向市场。 |<audio controls><source src="./wavs/Proposed/p02.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/thuhcsi/SpanPSP/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
