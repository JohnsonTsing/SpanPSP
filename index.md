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
| 3 | Baseline | 一般认为，确定耶路撒冷的地位是解决巴以冲突的核心问题。|<audio controls><source src="./wavs/Baseline/b03.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 一般认为，确定耶路撒冷的地位是解决巴以冲突的核心问题。 |<audio controls><source src="./wavs/Proposed/p03.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 4 | Baseline | 但愿他的忏悔是真诚的。|<audio controls><source src="./wavs/Baseline/b04.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 但愿他的忏悔是真诚的。 |<audio controls><source src="./wavs/Proposed/p04.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 5 | Baseline | 宁愿做一朵篱下的野花，不愿做一朵受恩惠的蔷薇。|<audio controls><source src="./wavs/Baseline/b05.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 宁愿做一朵篱下的野花，不愿做一朵受恩惠的蔷薇。 |<audio controls><source src="./wavs/Proposed/p05.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 6 | Baseline | 叙利亚总统阿萨德与黎巴嫩总统苏莱曼的会谈也令人瞩目。|<audio controls><source src="./wavs/Baseline/b06.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 叙利亚总统阿萨德与黎巴嫩总统苏莱曼的会谈也令人瞩目。 |<audio controls><source src="./wavs/Proposed/p06.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 7 | Baseline | 下了一个星期的雨了，每天待家里哪也去不了。|<audio controls><source src="./wavs/Baseline/b07.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 下了一个星期的雨了，每天待家里哪也去不了。 |<audio controls><source src="./wavs/Proposed/p07.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 8 | Baseline | 喜爱与收藏这些娃娃的人主要以女性居多。|<audio controls><source src="./wavs/Baseline/b08.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 喜爱与收藏这些娃娃的人主要以女性居多。 |<audio controls><source src="./wavs/Proposed/p08.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 9 | Baseline | 这些员工要参与产品测试，并及时提供反馈。|<audio controls><source src="./wavs/Baseline/b09.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 这些员工要参与产品测试，并及时提供反馈。 |<audio controls><source src="./wavs/Proposed/p09.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 10 | Baseline | 走近才发现，大桥已垮塌。|<audio controls><source src="./wavs/Baseline/b10.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|   | Proposed | 走近才发现，大桥已垮塌。 |<audio controls><source src="./wavs/Proposed/p10.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 11 | Baseline | 如今那些所谓当红女星，成千上万，哪一个拥有这样酷的眼神。|<audio controls><source src="./wavs/Baseline/b11.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 如今那些所谓当红女星，成千上万，哪一个拥有这样酷的眼神。 |<audio controls><source src="./wavs/Proposed/p11.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 12 | Baseline | 倘若一个人出名正出得半红不紫，那他是断不会淡薄的。|<audio controls><source src="./wavs/Baseline/b12.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 倘若一个人出名正出得半红不紫，那他是断不会淡薄的。 |<audio controls><source src="./wavs/Proposed/p12.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 13 | Baseline | 经突审，犯罪嫌疑人刘迎儿交代了犯罪事实和主要犯罪动机。|<audio controls><source src="./wavs/Baseline/b13.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 经突审，犯罪嫌疑人刘迎儿交代了犯罪事实和主要犯罪动机。 |<audio controls><source src="./wavs/Proposed/p13.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 14 | Baseline | 根据质地我们可以看到分若干个品种。|<audio controls><source src="./wavs/Baseline/b14.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 根据质地我们可以看到分若干个品种。 |<audio controls><source src="./wavs/Proposed/p14.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 15 | Baseline | 随着英文名越来越火，帮人取英文名这一行当也成了香馍馍。|<audio controls><source src="./wavs/Baseline/b15.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 随着英文名越来越火，帮人取英文名这一行当也成了香馍馍。 |<audio controls><source src="./wavs/Proposed/p15.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 16 | Baseline | 考试期间，首尔的宾馆旅店爆满，连桑拿中心也生意兴隆。|<audio controls><source src="./wavs/Baseline/b16.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 考试期间，首尔的宾馆旅店爆满，连桑拿中心也生意兴隆。 |<audio controls><source src="./wavs/Proposed/p16.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 17 | Baseline | 我相信小孩子也不希望妈妈每天都在家对他啰嗦吧。|<audio controls><source src="./wavs/Baseline/b17.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 我相信小孩子也不希望妈妈每天都在家对他啰嗦吧。 |<audio controls><source src="./wavs/Proposed/p17.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 18 | Baseline | 我会武术谁也挡不住呀。|<audio controls><source src="./wavs/Baseline/b18.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 我会武术谁也挡不住呀。 |<audio controls><source src="./wavs/Proposed/p18.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 19 | Baseline | 狐狸说：猴子，凭你这点小小的本事，你这笨蛋还想做兽中之王吗？|<audio controls><source src="./wavs/Baseline/b19.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 狐狸说：猴子，凭你这点小小的本事，你这笨蛋还想做兽中之王吗？ |<audio controls><source src="./wavs/Proposed/p19.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
|   |    |   |
| 20 | Baseline | 莫欺少年穷，要有信心哦！|<audio controls><source src="./wavs/Baseline/b20.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
|    | Proposed | 莫欺少年穷，要有信心哦！ |<audio controls><source src="./wavs/Proposed/p20.wav" type="audio/wav">Your browser does not support the audio element.</audio>   |
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
