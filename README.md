# LexVeritas

LexVeritas 是一个基于区块链的可验证法律知识库 RAG 系统,通过 Merkle Tree 和智能合约确保检索内容的真实性和可追溯性。

## 项目结构

本项目采用 Git 子模块管理多个组件:

- **lex-veritas-backend**: Go 后端服务 (Gin + Eino)
- **lex-veritas-blockchain**: 智能合约层 (Hardhat + Solidity)
- **lex-veritas-frontend**: 前端界面
- **lex-veritas-ingestion**: 数据处理管道 (Python)

## 快速开始

### 克隆项目

```bash
# 克隆主项目及所有子模块
git clone --recursive <repository-url>

# 或者先克隆主项目,再初始化子模块
git clone <repository-url>
cd LexVeritas
git submodule update --init --recursive
```

### 更新子模块

```bash
# 更新所有子模块到最新版本
git submodule update --remote --merge

# 或者拉取时自动更新子模块
git pull --recurse-submodules
```

### 在子模块中工作

```bash
# 进入子模块目录
cd lex-veritas-backend

# 在子模块中进行正常的 Git 操作
git checkout -b feature/new-feature
git add .
git commit -m "Add new feature"
git push origin feature/new-feature

# 返回主项目并提交子模块引用的更新
cd ..
git add lex-veritas-backend
git commit -m "Update backend submodule"
git push
```

## 本地开发

使用 Docker Compose 启动所有服务:

```bash
docker-compose up -d
```

详细的开发指南请参考各子模块的 README 文件。

## 文档

- [项目搭建指南](docs/project_setup_guide.md)
- [目录结构说明](docs/directory_structure.md)

## 技术栈

- **后端**: Go, Gin, Eino
- **区块链**: Solidity, Hardhat, Polygon
- **向量数据库**: Milvus
- **前端**: React
- **数据处理**: Python

## License

(待补充)
