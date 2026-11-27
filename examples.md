# 疑难规则参考（v4 原文摘录）

3. 分块规则
- 按语义和逻辑关系分块，不按句数等分。段落短就一块，长就多块，以读得顺为准。
- 语义紧连的两句可合为一块（块内用两个意群），不同语义的内容绝不塞进同一块。
- 块内再分意群（.eh），意群之间用 .dv 细线。
- 多分句必须按分句顺序排列：连词（whereas / while / but / and）归入后一分句的开头，不得孤立放在块末。
- 框内二级单元一律按原文线性顺序排列，不为「好看」调换。
- 分框的排列顺序服务于成分归类，允许与原文词序不同；但同一分句内部的先后必须忠于原文。
4. 两级结构
4.1 一级＝外框，代表成分大类
display:inline-block; vertical-align:top; border:1px solid <大类主色>;
border-radius:10px; padding:8px 10px 4px; margin:0 10px 14px 0;
框顶实心徽章：background:<主色>; color:#fff; border-radius:4px; padding:1px 7px; font-size:11.5px; font-weight:500;
- 一张卡只放一个成分大类，绝不合并（「主语＋谓语」合并是「粗」的根源）。
- 并列／从属连词归入它所连接的成分框内。
- 句首连接副词（However / Furthermore / Specifically / Nevertheless / Consequently）可独立标注，但不强制每次新建一级框。
4.2 二级＝框内最小单元
display:inline-block; vertical-align:top; padding:0 7px 2px 0;
margin:0 8px 8px 0; border-right:0.5px dashed <次要边框色>;
最后一个单元去右边框（.nob）。单元内自上而下三行：
1. 成分标签 12px / 500，按角色配色
2. 英文原片 15px（secondary）
3. 中文 15px（primary）
二级单元本身不加背景色。
4.3 拆分粒度：语义完整优先
- 默认按完整短语或可理解的语法成分拆分；只有该词确实构成理解难点才进一步展开。
- a significant improvement 作为一个名词短语，不必拆成冠词＋定语＋中心词。
- 冠词、介词、助动词不一律独立成卡；拆开会让读者在碎片间来回拼的，就是拆过头。
- 并列成分逐个拆卡并编号 ①②③；从句单独成框。
- 长成语块（如 in the application domain of interest）保持整体，不按介词切碎。

5. 成分标签与配色
5.1 标签格式：成分名（细类／引导词）
大类
细标签示例
主语
主语（名词短语）／主语（从句）／形式主语 it／真正主语（不定式）
谓语
谓语动词（及物／不及物／短语动词／时态）／谓语（系动词 is）
表语
表语（名词短语／形容词短语）／表语从句（because）
宾语
宾语（名词短语）／宾语从句／介词宾语（中心词）／宾语（并列②）
补语
宾语补足语／主语补足语
定语
定语（前置·复合定语）／定语（过去分词）／定语（后置介词短语）／定语从句（which 修饰 X）
状语
状语（方式／原因／目的／范围／时间／结果／让步／比较／依据／身份）
其他
同位语（缩写／命名）／插入语（such as 举例）／连词（and·并列谓语）／引导词（that）／并列项①／序号标记
标签必须准确。句子就是陈述，就标「陈述」或干脆不标功能词，不为凑格式强行定为「结论」或「推论」。

6. 特殊标注
6.1 定语从句
- 先行词单元：border-left:2.5px solid #BA7517; padding-left:5px;，标签后加徽章 先行词①。
- 从句框：border:2px dashed #BA7517;，徽章写 定语从句 ①，框内首行小字 ↑ 修饰先行词① X（中文）。
- 先行词按实际语法判断，不机械取最近名词；先行词也可能位于从句内部。
- 关系代词省略：标 关系代词省略，必要时说明其宾语作用，不一律标「缺宾语」。
- 嵌套从句（从句套从句）在框内作为一个单元标注，不另立外框。
6.2 非限制性定语从句
先判指代对象：
- 修饰名词 → 照定语处理，加先行词徽章，不得强行断句。
- 确实指代整个主句 → 不加先行词徽章；框顶写 ↑ 无名词先行词：which 指代整个主句（……）；中文断句用「这」承接。
6.3 重点标注（2026-11-27 定稿）
- 对照区：英文行与中文行标同一处，background:#FAEEDA; border-radius:2px; padding:0 2px; color:#B45309; font-weight:500;
- 成品译文必须同步上色：<span class="key">，color:#B45309; font-weight:500;，与对照区落在同一批内容上。
- 对象：① 术语／方法名／型号 ② 关键数字 ③ 结论强度词（significantly／substantially／consistently 等）。
- 范围要窄：只覆盖真正值得注意的 token。整短语全涂等于没有重点。
正确：SAM-leveraged、masked image pretraining、ViT-H、substantially
错误：把 a SAM-leveraged masked image pretraining framework 整段涂底。
- 图例末项写作「■ 重点」。
6.4 本文自提方法
作者自己提出的方法／模块的单元加 border-left:2px solid #EF9F27; padding-left:6px;（橙条），并在图例末尾加「▌本文自提方法」。
他人工作（被引方法、数据集、基线）一律不加。
橙条与同位语紫可以叠加：紫说明语法身份，橙条说明这是本文方法，信息不同，拥挤时减徽章不删信息。
6.5 引用标注
[2]、[13, 21] 原样保留，不单独成框：作上标角标挂在对应单元中文行末尾（11px / tertiary / vertical-align:super）；成品译文按原样写。作句子成分的文献编号（如 [68] suggests ...）正常作主语单元。
6.6 原文瑕疵
- 明确的排版断字／粘连可以还原（thatmixing → that mixing、ViTH → ViT-H），并在页脚注明。
- 笔误、语法不一致、缺冠词、以连字符代破折号、内容截断：按正确含义理解与翻译，不改动原词，页脚简短标注。
- 不擅自补全缺失内容，不暗改作者论述。
7. 译法规则（判断型，不设绝对命令）
7.1 结构处理
- 后置定语、分词结构：按长度、修饰范围与中文习惯处理，可以前移，也可以拆句，不一律前移。
- 英文名词化：可适当动词化，但保留必要的学术概念与术语（feature extraction 仍是「特征提取」）。
7.2 辅助词先判功能，再给含义
语法形式需要识别，但不固定绑定一个汉语词；没有自然对应时直接说明其语法作用，不硬译。
- has potential 的 has 是「具有」，不是「已」。
- 完成时 have/has 不一定都要译「已」。
- 被动不一定都用「被」：it is shown that → 「研究表明」；inspired by → 「受……启发」。
- may 可表可能性，也可表许可；must 可表推断，也可表义务。
- 已废止的机械映射：be→被／is→是／can→能够／have→已。
- 禁止用 — 作中文占位符（此条仍有效）。
7.3 不定式与介词
- 不定式 to：与动词合并展示，按实际功能说明目的、补足或修饰，不能一律译「以」。
- 介词 to：与不定式区分；from A to B、transmitted to ... 有对应（到／向）时独立成卡。
- with：判明是「手段（通过）」「伴随（与……一起）」「配置（采用……）」还是「对象（与……配合）」，不统一翻译。
- for：判明是「目的」「用途」「场合」（如 for fine-tuning SAM 常为场合）还是「受益对象」。
7.4 强度与语气
- 保留原文的强弱层次，不互相顶替：
demonstrate ＞ show；outperforms ＞ performs well；consistently ＞ usually ＞ often。
- 保守措辞照译：provide evidence that（弱于 demonstrate）、suggests、decent（不错的）、suboptimal（不够理想）、an initial investigation（初步探索）、shed light on（揭示）。
- significant／substantially：先判是「幅度大」还是「统计显著」，学术写作中多数表幅度。
- nontrivial → 「并非易事」；desirable → 「可取的」；comprehensive → 「系统的／全面的」。
7.5 中文行允许不组成通顺中文
对照区按英文顺序展示各片段的局部含义，顶部成品用自然中文。
但不能为了贴词序写出错误含义——准确性优先于词序对应。
7.6 术语首现
给「中文（缩写）」，后文统一用缩写。方法缩写与网络名称保留原名，但完整方法名仍可准确翻译（Reconstruction of Channel Correlation (RCC) → 通道相关性重建（RCC））。
段末原文无句号（截断）时，译文同样不加句号。
