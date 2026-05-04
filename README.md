# Geekster_Synthetic_Chart_Table_QA_Dataset
Synthetic chart/table reasoning dataset for VLM training on reading, comparing, and reasoning over structured visuals.

# Synthetic Chart/Table QA Dataset

## What this includes

- Ready-to-train synthetic dataset files.
- Multi-format exports for VLM training workflows.
- Metadata/statistics for quick validation and analysis.

## Data schema overview

- `qa.jsonl`: one QA supervision pair per line (`sample_id`, `image`, `question`, `answer`, `question_type`).
- `samples.jsonl`: one source sample per line with rendering metadata and OCR text labels.
- `llava_conversations.json`: chat-style conversion for instruction fine-tuning.
- `qa.parquet` / `samples.parquet`: analytics-friendly tabular copies.

## Task coverage

Lookup, comparison, count, sum, average, median, and difference reasoning over styled tables, bar charts, and line charts.

## Included files

- `data/images/`
- `data/qa.jsonl`
- `data/samples.jsonl`
- `data/llava_conversations.json`
- `data/qa.parquet`
- `data/samples.parquet`
- `data/stats.json`

## Quick usage

1. Use `images/` as visual inputs.
2. Use `llava_conversations.json` for LLaVA-style chat fine-tuning.
3. Use `qa.jsonl` for direct QA supervision.
4. Use parquet files for filtering and analytics pipelines.

## Sample image-text pairs (showcase)

### Sample 1
- **Image:** `images/chartqa_000000.jpg`
- **Metadata:** render_type: `table` | style: `borderless` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** more by Category

### Sample 2
- **Image:** `images/chartqa_000001.jpg`
- **Metadata:** render_type: `line_chart` | style: `plain` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** great by Category

### Sample 3
- **Image:** `images/chartqa_000002.jpg`
- **Metadata:** render_type: `table` | style: `compact` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** against by Category

### Sample 4
- **Image:** `images/chartqa_000003.jpg`
- **Metadata:** render_type: `bar_chart` | style: `classic` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** from by Category

### Sample 5
- **Image:** `images/chartqa_000004.jpg`
- **Metadata:** render_type: `table` | style: `classic` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** might by Category

### Sample 6
- **Image:** `images/chartqa_000005.jpg`
- **Metadata:** render_type: `bar_chart` | style: `wide` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** Enterprise by Category

### Sample 7
- **Image:** `images/chartqa_000006.jpg`
- **Metadata:** render_type: `bar_chart` | style: `minimal` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** after by Category

### Sample 8
- **Image:** `images/chartqa_000007.jpg`
- **Metadata:** render_type: `bar_chart` | style: `wide` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** good by Category

### Sample 9
- **Image:** `images/chartqa_000008.jpg`
- **Metadata:** render_type: `table` | style: `compact` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** long by Category

### Sample 10
- **Image:** `images/chartqa_000009.jpg`
- **Metadata:** render_type: `bar_chart` | style: `wide` | question_type: `extract_title`
- **Question:** What is the chart title?
- **Answer:** Expenses by Category

## Dataset stats

```json
{
  "num_samples": 10000,
  "render_types": {
    "bar_chart": 4059,
    "table": 3511,
    "line_chart": 2430
  },
  "questions": 100000,
  "resource_stats_used": {
    "text_files_found": 28482,
    "text_files_scanned": 1000,
    "text_read_failures": 0,
    "font_files_found": 2,
    "background_files_found": 118287,
    "labels": 499,
    "metrics": 110,
    "max_files": 1000
  },
  "resources_available": {
    "labels": 499,
    "metrics": 110,
    "fonts": 2,
    "backgrounds": 118287
  }
}
```

##To acquire the full dataset, please visit the following link.
[https://datageekready.gumroad.com/l/SyntheticChart-TableOCR-QADataset](https://datageekready.gumroad.com/l/SyntheticChart-TableOCR-QADataset)

