# Measuring Multilingual Encyclopedic Knowledge Representation in Foundation Language Models

[![License](https://img.shields.io/badge/License-Apache_2.0-green.svg)](https://github.com/daniel-furman/Capstone/blob/main/LICENSE) 
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/) 
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black) 

This is the repository for [Measuring Multilingual Encyclopedic Knowledge Representation in Foundation Language Models](https://bit.ly/ischool-berkeley-capstone). It contains several research artifacts including:

1. The [**code**][cka_run_main] for running the fact-completion benchmark with a compatible language model
2. The [**data**][hf_data] used for the fact-completion benchmark, which contains 20 languages
3. A [**demo**][cka_lightweight_demo] for fact-completion language models via contrastive knowledge assessment

## Test Leaderboard

To add a new model to the leaderboard, please reach out to us or submit a pull request.

| Model            | Authors      | English        |
|------------------|--------------|:--------------:|
| [`llama-30b`](https://arxiv.org/abs/2302.13971) | Touvron et al., 2023 | 89.40 +/- 0.38 |
| [`flan-t5-xxl`](https://arxiv.org/abs/2210.11416) | Chung et al., 2022 | |
| [`gpt-neox-20b`](https://arxiv.org/abs/2204.06745) | Black et al., 2022 | |
| [`gpt-j-6b`](https://github.com/kingoflolz/mesh-transformer-jax/#gpt-j-6b) | Wang et al., 2021 | |
| [`bloom-7b1`](https://arxiv.org/abs/2211.05100) | Scao et al., 2022 | 76.16 +/- 0.51 |
| [`gpt2-xl`](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) | Radford et al., 2018 | 73.76 +/- 0.54 |
| [`xlm-roberta-large`](https://arxiv.org/abs/1911.02116) | Conneau et al., 2019 | 61.55 +/- 0.59 |
| `Random guessing` | N/A | 50   | 

## Data Release

Cite calinet [[1][bib]], memit [[2][bib]], and t-rex [[3][bib]] papers.

## Authors

* Daniel Furman <daniel_furman@berkeley.edu>
* Tim Schott <timschott@berkeley.edu>
* Shreshta Bhat <bhat_shreshta@berkeley.edu>

## Advisor

* David Bamman <dbamman@berkeley.edu>

## Citation

Please cite this repository as follows if you use its data or code:

```
@misc{Measuring_Multilingual_Encyclopedic_Knowledge_2023,
  author = {Daniel Furman and Tim Schott and Shreshta Bhat},
  title = {Measuring Multilingual Encyclopedic Knowledge Representation in Foundation Language Models},
  year = {2023}
  publisher = {GitHub},
  howpublished = {\url{https://github.com/daniel-furman/Capstone}},
}
```

## Bibliography 

[1] Dong, Qingxiu, Damai Dai, Yifan Song, Jingjing Xu, Zhifang Sui, and Lei Li. "Calibrating Factual Knowledge in Pretrained Language Models". In Findings of the Association for Computational Linguistics: EMNLP 2022. [arXiv:2210.03329][cka] (2022).

[2] Meng, Kevin, Arnab Sen Sharma, Alex Andonian, Yonatan Belinkov, and David Bau. "Mass Editing Memory in a Transformer." arXiv preprint [arXiv:2210.07229][memit] (2022).

[3] ElSahar, Hady, Pavlos Vougiouklis, Arslen Remaci, Christophe Gravier, Jonathon S. Hare, Frédérique Laforest and Elena Paslaru Bontas Simperl. “T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples.” International Conference on Language Resources and Evaluation. [Link][trex] (2018).


[bib]: https://github.com/daniel-furman/Capstone#bibliography
[hf_data]: https://huggingface.co/datasets/CalibraGPT/Fact-Completion
[cka]: https://arxiv.org/abs/2210.03329
[memit]: https://arxiv.org/abs/2210.07229
[mmlu]: https://paperswithcode.com/sota/multi-task-language-understanding-on-mmlu
[mmlu_paper]: https://arxiv.org/abs/2009.03300
[trex]: http://aclanthology.lst.uni-saarland.de/L18-1544.pdf
[cka_lightweight_demo]: https://github.com/daniel-furman/Capstone/blob/main/notebooks/fact_completion_notebooks/fact-completion-lightweight-demo.ipynb
[cka_run_main]: https://github.com/daniel-furman/Capstone/blob/main/notebooks/fact_completion_notebooks/fact-completion-full-benchmark.ipynb
