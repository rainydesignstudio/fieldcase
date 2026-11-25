# fieldcase分发材料索引

路径基准：本INDEX所在目录；独立T从T:distribution进入fieldcase/。共享T无该分类时，由实际已登记的D:distribution入口读取，不新建上级公共分类。
材料版本：0.1.0.0；配套材料源自 `fieldcase-zh-dt-04`；材料语言：`zh-CN`。这里记录的是配套材料来源；整包批次和验证范围分别取同一固定资源根的随包 README §1 和 §5。

本包核心12份，K／R／M及模块材料10份，共22份源文件。D规范统一放本区docs/spec，K按知识库需求采用；同号不代表与旧K／T核心或rule-*入口兼容。精确来源、语言及保存范围须核实，不能用版本号代替固定内容。

## 1. 使用边界

先读adoption，再按用户选择读取原件。材料就位不表示采用或启动；所选工作文件按完整准入方案安装到本区D或实际资料层，更新INDEX／B、必要配套及精确来源。

K／R／M是可选资料层，不写进config.modules。三模块可以在D／T基础安装方法；知识获取的正式产出须有准入K目标，原始件单独获取可按授权存T。不自带业务库、外部工具或未提供Skills，不随安装运行网络、通信、Goal或heartbeat。

## 2. 固定材料

| # | 标识 | 名称 | 类别 | 入口 | 体积 | 取用方式 |
|---|---|---|---|---|---|---|
| 1 | <a id="adoption"></a>adoption | 层与模块采用配套 | 说明 | [配套](ADOPTION.md) | 25970 B | 可整读，核D／T核心、资料层、模块及升级边界 |
| 2 | <a id="knowledge-governance"></a>knowledge-governance | K治理原件 | 模板 | [K治理](layers/knowledge/AGENTS.md) | 4846 B | 本区自建K实际采用后生效；共享库沿原治理 |
| 3 | <a id="knowledge-index"></a>knowledge-index | K索引原件 | 模板 | [K索引](layers/knowledge/INDEX.md) | 1788 B | 仅自建K使用，不把本区管理规范复制到K |
| 4 | <a id="r-index"></a>r-index | R索引原件 | 模板 | [R索引](layers/references/INDEX.md) | 2532 B | 选择R后采用，不含参考业务内容 |
| 5 | <a id="m-governance"></a>m-governance | M治理原件 | 模板 | [M治理](layers/materials/AGENTS.md) | 2865 B | 选择M后采用，权限取实际治理 |
| 6 | <a id="m-index"></a>m-index | M索引原件 | 模板 | [M索引](layers/materials/INDEX.md) | 1610 B | 采用或定制后核本层治理B |
| 7 | <a id="cache-spec"></a>cache-spec | 知识获取方法原件 | 模板 | [获取规范](modules/knowledge-acquisition/docs/spec/cache-spec.md) | 7132 B | 与adoption§3配套，工作目标为本区D/spec |
| 8 | <a id="contract-spec"></a>contract-spec | 契约方法原件 | 模板 | [契约规范](modules/cross-workspace/docs/spec/contract-spec.md) | 5722 B | 与adoption§4配套，工作目标为本区D/spec |
| 9 | <a id="contract-index"></a>contract-index | 空契约索引原件 | 模板 | [契约索引](modules/cross-workspace/temp/contract/INDEX.md) | 595 B | 有权自建T才采用；共享T不覆盖，现行只读活跃段 |

本表登记原件及实际B，不是实例安装状态表；工作规范只有实际安装并登记D条目后才按D:标识使用。资料层标识只有实际根入口登记后才解析。

## 3. 选择与依赖

| 选择标识 | 用途 | 安装前置／运行依赖 | 配套 |
|---|---|---|---|
| knowledge | K知识库 | 根＋D＋T；选择自建、共享或导入K | adoption§2；knowledge-governance／knowledge-index |
| references | R参考与证据 | 根＋D＋T；选择R | adoption§2；r-index |
| materials | M生产材料 | 根＋D＋T；选择M | adoption§2；m-governance／m-index |
| knowledge-acquisition | 获取、转换、索引及可选verify | D／T可装方法，正式产出先定K目标 | adoption§3；cache-spec |
| cross-workspace | 契约、联络及推送 | D／T及实际合法契约入口；通信能力和授权另核 | adoption§4；contract-spec／contract-index |
| unattended | 无人值守、连续迭代及可另启熔断复活 | D／T；宿主能力、范围及完成条件实际核对 | adoption§5；无新增常驻文件 |

模块来源只在完整配套及必要核验完成后写config.modules。继承上位模式不等于本区模块安装，未安装不影响已适用上位规则。项目内Skills尚未提供，不把全模块解释为存在封装。

## 4. 维护与清理

更新先核固定身份、兼容、依赖、全部配套和B，不从浮动分支拼装。D引用、可选K及恢复点简化不借旧实测通过，正式分发仍需对应验证和来源核实。

未采用、停用、卸载及清理分别办理，不因删除config条目或取得新版而删除旧原件、唯一证据、恢复依据或现行规则。缺材料按D:agent-guide处理，不捏造来源。

本索引仅管理本组入口及兼容，不授予安装、获取、发送、提交或发布权限。复核触发：来源、批次、路径、选项、配套或兼容变化。
