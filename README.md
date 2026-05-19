# claude-cli

Claude CLI 配置管理工具。

## 安装

```bash
go build -o claude-cli .
```

## 使用方法

### 切换提供商配置

```bash
./claude-cli config <provider>
```

将 `~/.claude-cli/<provider>/*` 中的配置文件复制到 `~/.claude/`。

### 示例

```bash
# 创建 minimax 配置目录
mkdir -p ~/.claude-cli/minimax

# 将当前 Claude 配置保存为 minimax 配置
cp ~/.claude/settings.json ~/.claude-cli/minimax/settings.json

# 切换到 minimax 配置
./claude-cli config minimax
```

## 目录结构

```
~/.claude-cli/
└── minimax/
    └── settings.json  -> 复制到 ~/.claude/settings.json
```