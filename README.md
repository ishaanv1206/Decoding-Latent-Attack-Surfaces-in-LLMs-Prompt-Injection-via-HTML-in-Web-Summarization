# Decoding Latent Attack Surfaces in LLMs: Prompt Injection via HTML in Web Summarization

## Overview

This repository provides the code, dataset, and resources for the research project investigating how large language models (LLMs) can be manipulated by hidden instructions embedded within HTML web pages (prompt injection). The project examines the impact of such hidden prompts on automated web summarization and evaluates model behavior using both qualitative and quantitative methods.

## What’s Inside

- **280 HTML webpages:** 140 clean (normal), 140 with various HTML-based prompt injection attacks. (Not all HTML pages in HTML folder were used during evaluation, only pages with hidden tags were kept)
- **Python scripts:** For generating pages, extracting content, summarizing via LLMs, and evaluating summary changes.
- **Data and results:** Includes sample LLM summaries before/after attacks, evaluation metrics, and summary output files.

## Directory Structure

clean/
images/
injected/
evaluation.py
file_generation.py
gemma.csv
llama.csv
metadata.csv


## Project Workflow

1. **Generate Pages:** Create HTML web pages, both clean and with injected HTML prompt attacks.
2. **Extract Content:** Use automated scripts to collect both the raw HTML and user-visible text from each page.
3. **Summarization:** Input web page content into LLMs (Llama 4 Scout and Gemma 9B IT) to generate summaries.
4. **Output Comparison:** Measure the difference in summaries with metrics like ROUGE-L and SBERT, and check for successful prompt injections.
5. **Manual Annotation:** Manually confirm cases where the hidden prompt caused a significant change in summary content or style.

## Key Findings

- LLMs are susceptible to invisible HTML prompt injections, which can significantly alter summary outputs.
- Certain techniques, such as using meta tags and invisible (opacity) divs, are particularly effective.
- Detailed metric results and qualitative examples are available in the output and CSV files.

## License

This work is licensed under the [CC0 1.0 Universal (CC0 1.0) Public Domain Dedication]
