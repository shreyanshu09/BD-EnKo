<div align="center">
    
# Unveiling the Power of Integration: Block Diagram Summarization through Local-Global Fusion

[![Conference](https://img.shields.io/badge/ACL-2024-blue)](#how-to-cite)
[![Demo](https://img.shields.io/badge/Demo-Gradio-brightgreen)](#demo)

Official Implementation of BD-EnKo Dataset and Generator

</div>

## Introduction

**BD-EnKo** dataset provides a diverse and high-quality benchmark dataset in English and Korean for block diagram understanding. This dataset is created using our innovative data collection methodology, ensuring flexibility and scalability to support a wide range of applications in both languages.

<img width="946" alt="image" src="misc/overview.png">

The official implementation of the BlockNet model is available in this [GitHub](https://github.com/shreyanshu09/BlockNet) repository.

## Datasets

![image](misc/)

The links to the datasets are here:

- [`BD-EnKo`](https://huggingface.co/datasets/shreyanshu09/BD-EnKo): 83,394 samples.
- [`Complete Dataset`](https://huggingface.co/datasets/shreyanshu09/Block_Diagram): 84,925 samples.

## Dataset Format

This dataset follows the given structure:

```bash
> tree dataset_name
dataset_name
├── test
│   ├── metadata.jsonl
│   ├── {image_path0}
│   ├── {image_path1}
│             .
│             .
├── train
│   ├── metadata.jsonl
│   ├── {image_path0}
│   ├── {image_path1}
│             .
│             .
└── validation
    ├── metadata.jsonl
    ├── {image_path0}
    ├── {image_path1}
              .
              .

> cat dataset_name/test/metadata.jsonl
{"file_name": {image_path0}, "ground_truth": "{\"gt_parse\": {\"c2t\": \"{ground_truth_parse}\"}}"}
{"file_name": {image_path1}, "ground_truth": "{\"gt_parse\": {\"c2t\": \"{ground_truth_parse}\"}}"}
     .
     .
```

- The structure of `metadata.jsonl` file is in [JSON Lines text format](https://jsonlines.org), i.e., `.jsonl`. Each line consists of
  - `file_name` : relative path to the image file.
  - `ground_truth` : string format (json dumped), the dictionary contains `gt_parse`.




