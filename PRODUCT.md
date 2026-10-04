# CatCare Compass 产品说明 | Product Description

用户：缺少系统照护知识的新手成年猫主人。输入自然语言咨询，输出类别、紧急程度、路径、理由、照护回答或补充问题及实际引用来源。
Users: first-time adult cat owners lacking systematic care knowledge. Natural-language inputs produce a category, urgency, route, reason, care response or clarification, and cited sources.

规则→GPT分流与JSON校验→照护／行为路径采用MiniLM与NumPy Top-K→GPT基于资料回答与引用检查；兽医求助、追问及失败分支不生成照护答案。Part 1作为方法比较，不在每次咨询时训练。
Rules → GPT routing and JSON validation → care/behaviour routes use MiniLM and NumPy Top-K → GPT grounded answers and citation checks. Veterinary contact, clarification and failure routes do not generate care answers. Part 1 is comparison evidence, not per-enquiry training.

边界：不诊断、不处方、不代替兽医。局限包括合成小样本、证据覆盖、有限否定／时间规则、中文检索未充分验证、引用不保证蕴含，以及API失败与维护成本。
Boundaries: no diagnosis, prescription or replacement of veterinary care. Limitations include small synthetic samples, evidence coverage, limited negation/time rules, unvalidated Chinese retrieval, citation-entailment gaps, API failure and maintenance cost.


目标 / Targets:
{"three_class_accuracy": 0.867, "gold_all_retrieved": 0.8, "red_flag_recall": 1.0}

回归实测 / Regression measurements:
{"l1": 1.0, "three_class_accuracy": 1.0, "majority_baseline": 0.5625, "route_accuracy": 1.0, "red_flag_recall": 1.0, "urgent_false_referral": 0.0, "any_false_referral": 0.0, "details_accuracy": 1.0, "gold_all_retrieved": 1.0, "gold_document_coverage": 1.0, "gold_all_cited": 1.0, "failure_rate": 0.0, "l2_review_completion": 0.0, "l2_reviewed_pass": null}