# 城市更新资料契约

全部楼宇、机构、居民群体、设备、交易及事件均为本地合成，不对应新闻所涉真实主体，不声称新闻中发生这些业务问题。seed.json及各同名Parquet保留完全相同的原始值；actions.json是尚未应用的后续资料。inventory.json仅记录物理大小、摘要及行数，不是业务结论。原始量纲、空值和时区按下文解释。

sensors给member/unit/direction/reference_id/resolution；readings是不规则观测，state=ok/missing/saturated，饱和仅给limit边界。reference_checks给基点相对控制点测量及误差。instruments给更换区间/重叠，不给接续系数。environment为独立气象，vibrations为施工窗口；members给邻接与重要性，非危险判决。review_schedule是预定报告日，windows分正常研究与隔离诊断。inspection_actions给可澄清的参考/仪器/构件集合及停工成本，actions补基点复测原值。统一单位或分开解释，无真实建筑鉴定。

readings的value和limit均采用对应sensor.unit；direction定义结构报告正方向。R0用于水准位移而R1是倾角参考架，reference_checks.displacement_mm只描述参考点平移，不能直接从mrad倾角相减；角度共同参考支持不足时应保留限制。reference_checks.at为测量时点，actions给可用于后续复核的生效范围，未确认范围不默认全期。
