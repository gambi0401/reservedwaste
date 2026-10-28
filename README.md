# reservedwaste

**给预留实例的浪费打分并按阈值给出通过与否。**

`reservedwaste` —— 为每一项打分并与阈值比较，明确标出通过、边界与不通过三档

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`reservedwaste.py` 拷走就能用
- 不联网、不写文件

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install gambi0401-reservedwaste
```

装完直接用命令名调用：

```bash
reservedwaste --help
```

也可以不用安装，直接把 `reservedwaste.py` 拷走用——它只依赖标准库。

## 为什么需要它

阈值边界单独成档，不把「刚好压在阈值上」混进通过里

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到 预留实例的浪费 领域的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python reservedwaste.py --file input.txt
python reservedwaste.py --text "示例内容"
python reservedwaste.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 阈值是固定值，不随数据自适应。
- 只判定达标与否，不解释分数来源。

## 跑测试

```bash
python test_reservedwaste.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/gambi0401/reservedwaste>

---

## 关于作者

gambi0401 做预留实例的浪费相关的问题。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://gambi0401.github.io>
- 仓库：<https://github.com/gambi0401/reservedwaste>

## 许可

MIT，见 [LICENSE](LICENSE)。
