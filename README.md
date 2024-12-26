# Methodology Inspiration Retrieval (MIR) Dataset

The Methodology Inspiration Retrieval (MIR) dataset is designed to support research in retrieving methodological inspirations from academic papers. This dataset is constructed using the MultiCite dataset, which provides citation contexts with intent labels, and is augmented with additional data to ensure comprehensive and diverse representation of research subdomains.

## Dataset Overview

The MIR dataset includes:
- **Research Proposals**: Each proposal consists of a research problem and the motivation behind it.
- **Cited Papers**: Papers cited within the proposals, categorized by their methodological intent.
- **Citation Contexts**: The specific contexts in which the cited papers are referenced.
- **Citation Intents**: The intent behind each citation, categorized as methodological or non-methodological.

## Dataset Structure

The dataset is organized into several splits:
- **Training Set**: Proposals prior to the year 2019.
- **Development Set**: Proposals from January to June 2019.
- **Test Set**: Proposals after June 2019.
- **Augmented Training Set**: Additional proposals to ensure consistent domain representation.

## Usage

The dataset can be used for:
- Training and evaluating retrieval models for methodological inspirations.
- Studying the impact of citation intents on research methodologies.
- Analyzing the evolution of research subdomains over time.

## Citation

If you use this dataset in your research, please cite the original MultiCite dataset and any relevant publications that describe the construction and augmentation of the MIR dataset.

## Contact

For any questions or further information, please contact the dataset maintainers.

