# Third-party dataset material

The CC BY 4.0 grant in [LICENSE](LICENSE) covers original MIR contributions only. It does not replace upstream licenses or grant rights in third-party content.

## Dataset files

This notice applies to the dataset distributed in:

- `data/train_chronological_df.csv`
- `data/dev_chronological_df.csv`
- `data/test_chronological_df.csv`
- `data/augmented_train_chronological.csv`

These files combine MIR contributions with source-derived material. In particular, `citation_text`, `citing_paper_abstracts`, and `cited_paper_abstracts` contain paper text. Upstream annotations and material incorporated into other fields also retain applicable upstream terms; this is not an exhaustive field-level license classification. A file or column must not be treated as entirely CC BY 4.0 merely because it appears in this repository.

## MultiCite

MIR extends MultiCite by Anne Lauscher, Brandon Ko, Bailey Kuehl, Sophie Johnson, Arman Cohan, David Jurgens, and Kyle Lo.

- Source: https://github.com/allenai/multicite
- Paper: https://aclanthology.org/2022.naacl-main.137/
- Upstream license statement: https://github.com/allenai/multicite#license
- License: Creative Commons Attribution-NonCommercial 2.0 Generic (CC BY-NC 2.0), https://creativecommons.org/licenses/by-nc/2.0/

MultiCite states that it is derived from S2ORC and is released under CC BY-NC 2.0. That license continues to apply to MultiCite-derived material in MIR. MIR repurposes MultiCite for methodology inspiration retrieval and augments its training data, as described in the README and MIR paper. The CC BY 4.0 grant for original MIR contributions does not remove the upstream noncommercial restriction.

## arXiv and other paper content

Text sourced from individual papers remains subject to the applicable source licenses and permissions. Availability on arXiv does not establish a uniform reuse license.

- arXiv licensing information: https://info.arxiv.org/help/license/index.html
- Source identifiers are included in dataset fields such as `actual_ids` and `cited_paper_id`.

The distributed CSV files do not include a complete per-record license manifest. This notice does not certify that every record has the same reuse permissions or that a separately reusable, unrestricted subset has been established. Consult the source paper terms for the material being reused.

## Attribution

Retain applicable source attribution and license notices. The README provides citations for MIR and MultiCite; those citations do not replace compliance with their applicable license terms.
