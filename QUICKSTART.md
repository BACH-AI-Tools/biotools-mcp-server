# Biotools MCP Server - 快速开始指南

## 🚀 使用 npx 快速启动（推荐）

### 配置方法

在 Cursor / Cherry Studio 的 MCP 配置文件中添加：

```json
{
  "mcpServers": {
    "biotools": {
      "command": "npx",
      "args": ["-y", "biotools-mcp-server"]
    }
  }
}
```

### 说明

- 无需手动安装依赖
- `npx` 会自动从 npm 下载并运行最新版本
- `-y` 参数跳过确认提示，实现无人值守启动

---

## 📦 从 npm 安装

如果你想全局安装：

```bash
npm install -g biotools-mcp-server
```

安装后可直接使用：

```bash
biotools-mcp
```

---

## 🧬 可用工具（37 个）

### 📚 文献研究工具（3 个）

- `search_pubmed` - 搜索 PubMed 科学文献
- `get_publication_details` - 获取特定出版物的详细信息
- `get_publication_abstract` - 提取出版物摘要

### 🧬 蛋白质分析工具（3 个）

- `search_uniprot` - 搜索 UniProt 蛋白质数据库
- `get_protein_entry` - 获取蛋白质详细信息
- `get_protein_sequence` - 获取蛋白质序列

### 🧬 核苷酸序列分析工具（4 个）

- `get_nucleotide_sequence` - 获取核苷酸序列
- `compare_annotations` - 比较基因组注释
- `find_intron_exons` - 检测内含子-外显子边界
- `align_promoters` - 比对启动子区域

### 🧪 增强蛋白质分析工具（3 个）

- `get_cross_references` - 获取跨数据库引用
- `analyze_ptms` - 分析翻译后修饰
- `get_pathway_data` - 获取通路信息

### 🧬 DNA 分析工具（4 个）

- `analyze_gc_content` - 分析 GC 含量
- `find_restriction_sites` - 查找限制性酶切位点
- `predict_orfs` - 预测开放阅读框
- `assemble_fragments` - 组装 DNA 片段

### 🧬 蛋白质序列工具（3 个）

- `predict_protein_properties` - 预测蛋白质性质
- `predict_transmembrane_regions` - 预测跨膜区域
- `scan_protein_motifs` - 扫描蛋白质基序

### 🔍 序列相似性工具（5 个）

- `blast_search` - BLAST 搜索
- `psi_blast_search` - PSI-BLAST 搜索
- `align_sequences_global` - 全局序列比对
- `align_sequences_local` - 局部序列比对
- `generate_dotplot` - 生成点阵图

### 🧬 多序列比对工具（4 个）

- `multiple_sequence_alignment` - 多序列比对
- `highlight_conserved_regions` - 高亮保守区域
- `generate_sequence_logo` - 生成序列 logo
- `export_alignment` - 导出比对结果

### 🏗️ 结构与 RNA 工具（4 个）

- `get_protein_structure` - 获取蛋白质结构
- `analyze_secondary_structure` - 分析二级结构
- `predict_rna_secondary_structure` - 预测 RNA 二级结构
- `scan_rna_motifs` - 扫描 RNA 基序

### 🌳 系统发育工具（2 个）

- `build_phylogenetic_tree` - 构建系统发育树
- `compare_phylogenetic_trees` - 比较系统发育树

### 📊 文档工具（2 个）

- `log_analysis_parameters` - 记录分析参数
- `generate_resource_map` - 生成资源地图

---

## 📝 版本信息

- **当前版本**: 1.0.0
- **npm 地址**: https://www.npmjs.com/package/biotools-mcp-server
- **源码地址**: https://github.com/biotools-mcp/biotools-mcp-server

---

## 💡 使用示例

```javascript
// 搜索 BRCA1 相关文献
{
  "tool": "search_pubmed",
  "arguments": {
    "term": "BRCA1 mutations breast cancer",
    "max_results": 10
  }
}

// 获取蛋白质详细信息
{
  "tool": "get_protein_entry",
  "arguments": {
    "accession": "P38398"  // BRCA1 蛋白
  }
}

// 分析 DNA 序列 GC 含量
{
  "tool": "analyze_gc_content",
  "arguments": {
    "sequence": "ATCGATCGATCGATCG"
  }
}
```
