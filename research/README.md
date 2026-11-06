# 研究资料区

状态：尚未检索，暂无已核验文献。此文件是交付说明，不是研究成果。

Claude 依照 prompts/claude-literature-search.md 生成：
- scope.md
- search-log.md
- literature.csv
- references.bib
- evidence-notes.md
- comparison.md
- gaps.md

建议 literature.csv 表头：

```csv
id,title,authors,venue,source_type,publication_date,date_type,date_evidence_url,doi,official_url,fulltext_url,accessed_on,access_status,verification_status,recent_window_eligible,relevance
```

CSV 使用 UTF-8，含逗号或换行的字段正确加引号；未知字段明确标注。日期与近期合格状态分开保存，只有核验后才标合格。每个新增文件立即登记到 LOCATIONS.md。
