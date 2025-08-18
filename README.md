# 🎯 Methodology Inspiration Retrieval

This repository houses the datasets used in our ACL 2025 paper:
**"MIR: Methodology Inspiration Retrieval for Scientific Research Problems"**  🎓

Paper: https://arxiv.org/abs/2506.00249

![MIR Diagram](assets/Diagram.png)

## 🧠 What’s This About?

Our paper explores fundamental questions:

- What’s the best way to retrieve papers on when designing novel scientific hypotheses?
- Are current retrievers trained on semantic similarity enough to inspire new solutions?
- What does it take to retrieve true methodological inspirations?

We **extend the MultiCite Dataset** (Lauscher et al. 2022), originally designed for *citation context intent classification*, and **repurpose this for our retrieval benchmark**. Specifically, we focus citations that provide the most actionable signal towards tracing methodological inspirations in the literature. We extend the original training data by augmenting latest papers from arXiv, up till mid 2024.

Using citation *texts* and citation *intents*, we derive the *Methodology Adjacency Graph (MAG)*, a pruned citation graph, where edges are annotated with citation intents pivotal for the task, viz. ‘methodology’ or ‘non-methodology’. 

Finally we train dense retrievers by sampling triplets from the MAG and fine-tune retrievers by with a joint triplet loss. We find significant gains in recall and mean average precision using these methods.


## 📦 Dataset Overview

The MIR dataset includes:
- 📌 **Research Proposals**: Each proposal consists of a research problem and motivation.
- 📚 **Cited Papers**: Papers cited within the proposals (citing papers), categorized by their methodological citation intent.
- 🧾 **Citation Contexts**: The specific contexts in which the cited papers are referenced.
- 🧭 **Citation Intents**: The intent behind each citation, categorized as methodological or non-methodological.

### 📊 Dataset Splits
The dataset is organized into the following splits:
- **Training Set**: Proposals prior to the year 2019.
- **Development Set**: Proposals from January to June 2019.
- **Test Set**: Proposals after June 2019.
- **Augmented Training Set**: Additional proposals up till mid 2024 to ensure consistent domain representation.

### 🧪Evaluation Settings

The evaluation settings are divided into two distinct methods to (a) avoid temporal overlap introduced by cited papers of proposals in the same test set, and (b) to avoid overlap with cited papers in the training set. We term these **Restricted Corpus** and **Extended Corpus**. **Restricted Corpus** contains all the cited papers in the test set, while **Extended Corpus** dynamically considers cited papers from both the training set and ground-truth citations associated with each test proposal. This tests retriever performance across a more expansive and diverse corpus

## 📄 Citation

If you intend to use this dataset in your work, please consider citing our paper:

```
@inproceedings{garikaparthi-etal-2025-mir,
    title = "{MIR}: Methodology Inspiration Retrieval for Scientific Research Problems",
    author = "Garikaparthi, Aniketh  and
      Patwardhan, Manasi  and
      Kanade, Aditya Sanjiv  and
      Hassan, Aman  and
      Vig, Lovekesh  and
      Cohan, Arman",
    editor = "Che, Wanxiang  and
      Nabende, Joyce  and
      Shutova, Ekaterina  and
      Pilehvar, Mohammad Taher",
    booktitle = "Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.acl-long.1390/",
    doi = "10.18653/v1/2025.acl-long.1390",
    pages = "28614--28659",
    ISBN = "979-8-89176-251-0",
    abstract = "There has been a surge of interest in harnessing the reasoning capabilities of Large Language Models (LLMs) to accelerate scientific discovery. While existing approaches rely on grounding the discovery process within the relevant literature, effectiveness varies significantly with the quality and nature of the retrieved literature. We address the challenge of retrieving prior work whose concepts can inspire solutions for a given research problem, a task we define as Methodology Inspiration Retrieval (MIR). We construct a novel dataset tailored for training and evaluating retrievers on MIR, and establish baselines. To address MIR, we build the Methodology Adjacency Graph (MAG); capturing methodological lineage through citation relationships. We leverage MAG to embed an ``intuitive prior'' into dense retrievers for identifying patterns of methodological inspiration beyond superficial semantic similarity. This achieves significant gains of +5.4 in Recall@3 and +7.8 in Mean Average Precision (mAP) over strong baselines. Further, we adapt LLM-based re-ranking strategies to MIR, yielding additional improvements of +4.5 in Recall@3 and +4.8 in mAP. Through extensive ablation studies and qualitative analyses, we exhibit the promise of MIR in enhancing automated scientific discovery and outline avenues for advancing inspiration-driven retrieval."
}
```
And the original MultiCite paper:
```
@inproceedings{lauscher-etal-2022-multicite,
    title = "{M}ulti{C}ite: Modeling realistic citations requires moving beyond the single-sentence single-label setting",
    author = "Lauscher, Anne  and
      Ko, Brandon  and
      Kuehl, Bailey  and
      Johnson, Sophie  and
      Cohan, Arman  and
      Jurgens, David  and
      Lo, Kyle",
    editor = "Carpuat, Marine  and
      de Marneffe, Marie-Catherine  and
      Meza Ruiz, Ivan Vladimir",
    booktitle = "Proceedings of the 2022 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies",
    month = jul,
    year = "2022",
    address = "Seattle, United States",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.naacl-main.137/",
    doi = "10.18653/v1/2022.naacl-main.137",
    pages = "1875--1889"
}
```

## 📬 Contact

For any questions or further information, please get in touch with aniketh.g@tcs.com

