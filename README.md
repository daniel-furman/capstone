# CalibraGPT: The Search for (Mis)Information in Large Language Models

[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/daniel-furman/Capstone/blob/main/LICENSE) 
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/) 
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black) 

This is the repo for the UC Berkeley CalibraGPT project, which aims to assess how large language models handle matters of veracity and store facts across different languages. The repo contains the following:

1. The [**72.3k+ English data**][data] employed for the fact completion benchmark, **20+ more languages to come**
2. A [**notebook demo**][notebook_cka_demo] for running lightweight contrastive knowledge assessment (i.e., factual completion probing)
3. The [**code**][benchmark_cka_code] for running the full fact completion benchmark in a given language with a [compatible](https://github.com/daniel-furman/Capstone#model-families-tested) model

## Data Release

Cite calinet [[1][bib]], memit [[2][bib]], and t-rex [[3][bib]].

## Selected benchmark results

**English** results:

| Model           | Fact completion benchmark (% correct) |
|------------------|---------------------------------------------|
| `llama-33b`     | 88.29 (+/- 0.23)   |
| `llama-13b`     | 86.44 (+/- 0.25)   | 
| `llama-7b`      | 85.68 (+/- 0.25)    | 
| `flan-t5-xl`    | 81.06 (+/- 0.25)   | 
| `flan-t5-large` | 77.89 (+/- 0.30)   | 
| `roberta-large` | 75.53 (+/- 0.31)   | 
| `flan-t5-base`  | 73.78 (+/- 0.32)    | 
| `Random guessing` | 50   | 

Add info on the CalibraGPT benchmark ... For reference, random guessing would score a 50%.

* The uncertainty estimates in the CalibraGPT results were calculated using bootstrap resampling (10,000 random samples with replacement, 95% confidence level).  

**Multilingual** results (coming)

## Model families tested

| Model family | Release date | Model type | Organization |
|--------------|--------------|------------|--------------|
| `BERT`       | Oct 2018     | Masked LM  | Google       |
| `GPT2`       | Feb 2019     | Causal LM  | OpenAI       |
| `RoBERTa`    | Nov 2019     | Masked LM  | Meta AI      |
| `T5`     `    | Jul 2020     | Seq2Seq    | Google       |
| `GPT-J`      | Aug 2021     | Causal LM  | EleutherAI   |
| `GPT-Neo`    | Apr 2022     | Causal LM  | EleutherAI   |
| `OPT`        | May 2022     | Causal LM  | Meta AI      |
| `Flan-t5`    | Dec 2022     | Seq2Seq    | Google       |
| `Pythia`     | Feb 2023     | Causal LM  | EleutherAI   |
| `LLaMa`      | Feb 2023     | Causal LM  | Meta AI      |
| `Flan-ul2`   | Mar 2023     | Seq2Seq    | Google       |

## Models Release

## Setup instructions

* For running a notebook in Google Colab, see .ipynb files in ```./notebooks/```
* For running locally, follow the steps below from the root dir

```
pip install -r requirements.txt
cd src/cka_scripts
python run_cka.py configs.tests.bert_v0
```

## Authors
All grad students below contributed equally.

* Shreshta Bhat <bhat_shreshta@berkeley.edu>
* Daniel Furman <daniel_furman@berkeley.edu>
* Tim Schott <timschott@berkeley.edu>

## Advisor

* David Bamman <dbamman@berkeley.edu>

## Citation

Please cite the repo if you use the data or code in this repo.

```
@misc{calibragpt,
  author = {Shreshta Bhat and Daniel Furman and Tim Schott},
  title = {CalibraGPT: The Search for (Mis)Information in Large Language Models},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/daniel-furman/Capstone}},
}
```

## Bibliography 

1. Qingxiu Dong, Damai Dai, Yifan Song, Jingjing Xu, Zhifang Sui, and Lei Li."Calibrating Factual Knowledge in Pretrained Language Models". In Findings of the Association for Computational Linguistics: EMNLP 2022. [arXiv:2210.03329][cka] (2022).
2. Kevin Meng, Arnab Sen Sharma, Alex Andonian, Yonatan Belinkov, and David Bau. "Mass Editing Memory in a Transformer." arXiv preprint [arXiv:2210.07229][memit] (2022).
3. Hady ElSahar, Pavlos Vougiouklis, Arslen Remaci, Christophe Gravier, Jonathon S. Hare, Frédérique Laforest and Elena Paslaru Bontas Simperl. “T-REx: A Large Scale Alignment of Natural Language with Knowledge Base Triples.” International Conference on Language Resources and Evaluation. [Link][trex] (2018).

[notebook_cka_demo]: https://colab.research.google.com/github/daniel-furman/Capstone/blob/main/notebooks/cka_run_main_demo.ipynb
[data]: https://github.com/daniel-furman/Capstone/tree/main/data/calibragpt_full_input_information.json
[cka]: https://arxiv.org/abs/2210.03329
[memit]: https://arxiv.org/abs/2210.07229
[mmlu]: https://paperswithcode.com/sota/multi-task-language-understanding-on-mmlu
[mmlu_paper]: https://arxiv.org/abs/2009.03300
[bib]: https://github.com/daniel-furman/Capstone#bibliography
[trex]: http://aclanthology.lst.uni-saarland.de/L18-1544.pdf
[benchmark_cka_code]: https://github.com/daniel-furman/Capstone/blob/main/src/cka_scripts/run_cka_full_benchmark.py
