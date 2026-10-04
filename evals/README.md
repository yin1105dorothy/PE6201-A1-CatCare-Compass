# 评测设计 | Evaluation Design

results/: 20条回归／整合案例（14+6），5条gold资料题，3条紧急题。用于验证既有流程和修复，不是独立真实用户验证。
results/: 20 regression/integration cases (14+6), five gold-source questions and three urgent cases. They verify the existing workflow and fixes, not independent real-user performance.

supplemental/: 在存在结果时保存10条运行前冻结的补充合成题。部分主题与开发题重叠；9条三类标签、1条信息不足、1条紧急题、4条gold资料题。
supplemental/: When available, stores ten pre-frozen supplemental synthetic cases. Some topics overlap development cases. There are nine three-category labels, one clarification case, one urgent case and four gold questions.

L1检查运行、字段、预期与引用合同；L2人工核对事实与证据，合法编号不等于事实正确。None表示未复核。评分须绑定实际run_id。两组分别计分，不池化准确率。风险召回与误转介及失败率配对报告。
L1 checks execution, fields, expectations and citation contracts. L2 reviews facts against evidence; valid IDs do not guarantee correctness. None means unreviewed. Reviews require the matching run_id. Scores are separate and not pooled. Recall is paired with false referrals and failure rate.
