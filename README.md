> 本版本为ipynb版本，可以直接运行

1. 安装notedown

```bash
# 1.安装 notedown
pip install notedown
# 2.markdown -> ipynb
notedown input.md > output.ipynb
# 3.ipynb -> markdown
# 3.1 去除输出
notedown input.ipynb --to markdown --strip > output.md
# 3.2 保留输出
notedown input.ipynb --to markdown > output_with_outputs.md
```
