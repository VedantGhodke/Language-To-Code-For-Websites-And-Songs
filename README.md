# Language Models For Conversion To Websites And Songs

Recent work has demonstrated substantial gains on many NLP tasks and benchmarks by pre-training on a large corpus of text followed by fine-tuning on a specific task. While typically task-agnostic in architecture, this method still requires task-specific fine-tuning datasets of thousands or tens of thousands of examples. By contrast, humans can generally perform a new language task from only a few examples or from simple instructions – something which current NLP systems still largely struggle to do. Here we show that scaling up language models greatly improves task-agnostic, few-shot performance, sometimes even reaching competitiveness with prior state-of-the-art fine-tuning approaches. Specifically, we train this code, an autoregressive language model with 175 billion parameters, 10x more than any previous non-sparse language model, and test its performance in the few-shot setting.


For all tasks, this code is applied without any gradient updates or fine-tuning, with tasks and few-shot demonstrations specified purely via text interaction with the model. The code achieves strong performance on many NLP datasets, including translation, question-answering, and cloze tasks, as well as several tasks that require on-the-fly reasoning or domain adaptation, such as unscrambling words, using a novel word in a sentence, or performing 3-digit arithmetic. At the same time, we also identify some datasets where this code's few-shot learning still struggles, as well as some datasets where the code faces methodological issues related to training on large web corpora. Finally, we find that the code can generate samples of news articles which human evaluators have difficulty distinguishing from articles written by humans. We discuss broader societal impacts of this finding and of this code in general.

## Contents

- [175b_samples.jsonl](175b_samples.jsonl) - Unconditional, unfiltered 2048 token samples from this code with p=.85, t=1.&#12288;


**CONTENT WARNING:** This code was trained on arbitrary data from the web, so may contain offensive content and language.
- [data](data) - Synthetic datasets for word scramble and arithmetic tasks described in the paper.
- [dataset_statistics](dataset_statistics) - Statistics for all languages included in the training dataset mix.
- [overlap_frequency.md](overlap_frequency.md) - Samples of 13-gram overlaps between our training data and benchmarks, selected by frequency in the training set.


