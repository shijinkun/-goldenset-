# Goldenset 验证 — 材料文献结构化提取

## 提交文件说明

### validation_package.zip
最终验证包，包含：
- gold_cleaned.xlsx — 金标准(16字段,310行)
- extraction_cleaned.json — 提取结果(16字段,1029条)
- final_judgement_rows.xlsx — 逐行审计表(带原文证据)
- FINAL_REPORT.md — 完整报告(含未匹配分析和流程SOP)

### pipeline_outputs.zip
管道中间产物，展示数据流转：
- text_jobs/ — DeepSeek文本提取输入(35个全文job)
- text_raw_deepseek_retry/ — DeepSeek提取原始输出
- image_vl_qwen_context_rerun_direct/ — VLM图像提取输出(507条)
- schema_mapping_.../ — Schema Mapping输入(1151条)和输出
- text_merged_chunked/ — Chunked提取实验产物(749材料系统)
- eval_.../schema_mapping_evaluation.json — 全量评估结果
- final_v13_ph_fixed.json — 最终1029条mapped records

## 结果摘要

| 指标 | 值 |
|------|-----|
| 文献数 | 35篇 |
| 金标准行数 | 310 |
| 提取字段数 | 16 |
| 匹配行数 | 286 (92.3%) |
| 平均字段合规率 | 95.0% |
