<img width="2154" height="1347" alt="image" src="https://github.com/user-attachments/assets/b84495f4-2776-4735-aec3-f206e886dfd9" />

# 项目结构
```plaintext
├── app/
│   ├── __init__.py
│   ├── config.py            # 配置管理（API Key、模型参数）
│   ├── prompts.py           # 软件测试专家系统提示词
│   ├── document_loader.py   # 多格式文档加载器
│   ├── rag_engine.py        # RAG核心引擎
│   └── main.py              # FastAPI Web服务
├── static/
│   ├── index.html           # Web界面
│   ├── style.css            # 样式
│   └── app.js               # 前端交互逻辑
├── data/chroma_db/          # 向量数据库存储
├── uploads/                 # 上传临时目录
├── .env                     # 环境变量配置
├── requirements.txt
└── run.py                   # 启动脚本
```

# 核心功能
1. 系统提示词 - 内置软件测试领域专家角色，涵盖测试方法论、自动化框架、性能测试、安全测试、测试管理等专业知识
2. 文档支持 - 支持 PDF、Word、Markdown、TXT、CSV 格式文档上传和索引
3. RAG引擎 - 基于LangChain文档切分 + ChromaDB向量存储 + 通义千问Embedding/LLM
4. Web界面 - 左侧知识库管理 + 右侧对话式问答，支持流式输出和来源引用
