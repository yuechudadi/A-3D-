shensx-animal-animator-core/
├──.github/
│   └── workflows/
│       └── ai-validation.yml      # GitHub Actions 自动化测试与持续集成配置
├── assets/
│   ├── logos/                     # 项目徽标与架构图表
│   └── demo_clips/                # 《狼王梦》生成的最终成果 GIF 动图展示
├── configs/
│   ├── agent_roles.yaml           # OpenClaw 子代理角色与权限配置文件
│   └── mimo_api_config.json       # Xiaomi MiMo-V2.5 API 密钥与端点设置
├── data/
│   ├── source_texts/              # 沈石溪小说原始脱敏文本片段
│   └── character_dna/             # 动物角色一致性基准参考图库 (CREF)
├── src/
│   ├── agents/
│   │   ├── director_agent.py      # MiMo-V2.5-Pro 长文本规划器逻辑核心
│   │   ├── asset_manager.py       # Kling 3.0 / MidJourney 图像 API 封装修饰器
│   │   ├── audio_sync_vasa.py     # JoyVASA 音频面部同步框架接入点
│   │   └── multimodal_validator.py# 基于多模态模型的视觉质量检测关卡
│   ├── tools/
│   │   ├── ffmpeg_assembler.py    # 自动化视频片段拼接与剪辑脚手架
│   │   └── prompt_compiler.py     # 文本到分镜指令的结构化编译工具
│   └── orchestrator/
│       └── openclaw_gateway.py    # OpenClaw 核心事件总线与生命周期管理器
├── tests/                         # 针对各 Agent 交接数据契约的单元测试
├──.env.example                   # 环境配置模板，说明需填入 MIMO_API_KEY
├── requirements.txt               # 运行环境依赖库声明
└── README.md                      # 核心项目展示文档
# 一键启动
# git clone https://github.com/yuechudadi/shensx-animal-animator-core.git
# cd shensx-animal-animator-core
# pip install -r requirements.txt
# python src/orchestrator/openclaw_gateway.py --book "data/source_texts/wolf_king_dream.txt"
