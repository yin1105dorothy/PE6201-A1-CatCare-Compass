# CatCare Compass 提交与复现说明 | Submission and Reproduction

入口 / Entry: CatCare\_Compass\_10\_04.ipynb  (Google Colab)

1–7：依赖、API配置、知识库、检索、分流、回答和系统入口。
1–7: dependencies, API configuration, knowledge, retrieval, routing, answers and system entry point.

8：单条演示（RUN\_DEMO）；9：20条回归批次（RUN\_EVAL）；10：绑定当前run\_id的人工评分；11：回归指标。
8: single demo (RUN\_DEMO); 9: twenty-case regression batch (RUN\_EVAL); 10: human review explicitly bound to its run\_id; 11: regression metrics.

11A-A/B：定义与冻结10条补充题及系统；C：真实运行（RUN\_SUPPLEMENTAL）；D/E：输出与人工评分；F：补充指标和独立ZIP。12：统一证据ZIP。
11A-A/B: define and freeze ten supplemental cases and the system; C: execution (RUN\_SUPPLEMENTAL); D/E: output and review; F: supplemental metrics and standalone ZIP. 12: combined evidence ZIP.

API key采用环境变量、Colab Secret或隐藏输入；不包含在包中。不要求先运行其他Notebook。生成模型通过OpenRouter调用；模型／网络可能影响复现，实际环境版本另保存。
The API key uses environment variables, Colab Secrets or hidden input and is not included in the archive. Other notebooks need not be run first. Generation uses OpenRouter. Provider and network changes can affect reproduction; actual package versions are recorded.

目录 / Contents:

* data/: knowledge and source metadata / 知识及来源
* evals/: fixed regression cases and gold sources / 固定回归题及正确来源
* results/: executed regression records, batch, metrics and reviews / 实际回归结果
* supplemental/: supplemental evidence when run / 已运行补充证据
* prompts.json, config.json, manifest.json, environment\_versions.json

两组结果分别报告；README与manifest列出实际批次。未运行不报告成绩，未完成人工复核不报告全案例L2。history不作为当前成绩。双语版本需要新的实际运行与复核。
Results are reported separately. README and manifest identify actual batches. Unrun cases have no scores; incomplete review has no overall L2. Historical reviews are not current scores. The bilingual version requires its own execution and review.

成本是按记录日期单价及实际Token估算的模型费用，不包括开发、维护与托管。小样本不能证明全面安全。
Cost estimates use dated prices and actual tokens and exclude development, maintenance and hosting. Small samples do not establish comprehensive safety.

此ZIP不自动包含Notebook源文件、Part 1比较、最终报告或视频；这些作为独立提交材料。
This ZIP does not automatically include notebook source, Part 1 comparison, final report or video; these are separate submission items.



实际批次 / Included batches

* Regression: 29bbe174a29045f0972af040c9cdf1e8 (20 cases)
* Supplemental: 已包含 / Included: edfd78dcb4de4353b02830b15467ed3f
* Regression review binding: False

