# 补充合成测试 | Supplemental Synthetic Evaluation

DeepSeek生成10个主题；ChatGPT协助改写咨询与评分标准，作者审核。
DeepSeek generated ten topics; ChatGPT assisted with enquiries and rubrics, reviewed by the author.

部分主题与开发题重叠，不属于完全独立情境或真实用户验证。文本、预期及系统在运行前冻结；评分不用于调优本次冻结版本。
Some themes overlap development cases; this is not fully independent scenario or real-user validation. Inputs, expectations and the system are frozen before execution. Scores are not used to tune that frozen version.

L1检查运行、标签、合同与状态；L2人工核对回答与证据。helpful另外评价实质帮助。未复核项保持None，不产生全案例L2成绩。
L1 checks execution, labels, contracts and status. L2 reviews responses against evidence. Helpfulness is separate. Unreviewed entries remain None, and overall L2 is withheld until completion.

本批10题：9条三类标签、1条信息不足、1条紧急题、4条gold来源题。T02/T08/T10预期资料不足。小样本不证明总体可靠性或全面安全。
This batch has ten cases: nine three-category labels, one clarification case, one urgent case and four gold-source questions. T02/T08/T10 lack complete evidence by design. Small samples do not establish overall reliability or comprehensive safety.

files: frozen.json, cases.json, records.json, batch.json, human_l2.json, metrics.json, metrics.csv, failures.json, price.json.
回归与补充成绩分别报告，不合并为30题准确率。
Regression and supplemental scores are reported separately, not pooled as 30-case accuracy.
