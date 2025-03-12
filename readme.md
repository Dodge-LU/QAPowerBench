# A Multi-Type Structured QA Benchmark Dataset for Power Industry

## Overview

This repository contains a Chinese-language benchmark dataset for structured question-answering (QA) tasks, specifically focused on the power industry. The dataset is derived from 484 authoritative documents related to the electric power sector and is designed to help evaluate AI models, particularly Large Language Models (LLMs), in the context of knowledge comprehension and reasoning within this domain.

The dataset is structured in JSONL format, making it suitable for efficient batch processing and dynamic scalability. It includes 93,988 structured questions categorized across various professional fields, question types, difficulty levels, and standard sources.

## Dataset Details

- **Total Number of Questions**: 93,988
- **Data Format**: JSONL (ISO/IEC 21778 compliant)
- **Source**: Publicly available Chinese power industry standards
- **Categories**: 
  - **Standard Sources**: GB, DB, DL/T (National, Local, and Power Industry Standards)
  - **Professional Fields**: Primary Substation, Secondary Substation, Transmission Line, Civil Engineering, and more
  - **Question Types**: Fill-in-the-blank, Calculation, Case Analysis, Multiple Choice, True/False, Comprehension
  - **Difficulty Levels**: L1 (easy), L2 (moderate), L3 (difficult)

### Key Features

- **Multi-type QA**: Questions include multiple question types, such as fill-in-the-blank, multiple-choice, case analysis, and more.
- **Structured Format**: Data is structured in JSONL format, making it easy to parse, process, and expand.
- **Difficulty Labeling**: Each question is labeled with one of three difficulty levels based on model validation.
- **Real-world Relevance**: Questions are derived from real-world power industry standards and documents.

## Dataset Structure

Each entry in the dataset contains the following fields:

- **id**: Unique identifier (e.g., 016 1063 010)
- **doc**: Source document name
- **standard**: Standard source of the document (e.g., GB, DB, DL/T)
- **field**: Professional field of the document (e.g., Primary Substation, Transmission Line)
- **type**: Question type (e.g., fill-in-the-blank, multiple-choice)
- **difficulty**: Difficulty level (L1, L2, L3)
- **question**: The question stem, sensitive to the question type (e.g., with options, formulas)
- **answer**: Answer format, sensitive to question type (e.g., single character for multiple-choice)
- **analysis**: Explanation for question types like fill-in-the-blank, calculation, and case analysis
- **knowledge_points**: Associated knowledge points (e.g., ["Principle of Differential Protection", "Characteristics of Magnetizing Inrush Current"])
