# 舆情事理图谱工具
## V1:简化版
### 核心功能模块
* **LLM 交互与文本处理**：
* `call_llm`: 封装了对 DeepSeek API 的调用，支持自定义 System/User Prompt 和参数（如 Temperature）。
* `chunk_text`: 将长文本按固定长度（默认 1200 字符）进行分块，以规避大模型单次输入的上下文长度限制。
* **信息提取与清洗**：
* `extract_from_chunk`: 结合预设的 Prompt，从单个文本块中识别出包含 `cause`（原因）、`relationship_type`（关系类型）和 `effect`（结果）的 JSON 数组。
* `extract_json`: 利用正则表达式从 LLM 返回的文本中过滤掉冗余描述，精准提取 JSON 格式数据。
* **知识标准化**：
* `standardize_entities`: 针对初步提取的三元组进行“二次加工”。它再次调用 LLM 来合并同义词、统一实体表达（例如将“AI”和“人工智能”统一），提高知识图谱的质量。

## V2
### 
## V3
### 
## V4
### 
