# 研究与工程更新索引｜2026年10月

编者：SHENGDONG WU｜整理：2026-10-30  
© 2026 SHENGDONG WU，保留所有权利。

本目录保存公开资料的原创工程摘要，不改变主手册的施工标准。所有结论均有日期和产品边界；原始链接可能更新，实施前复核。按主题归并重复内容，不把草案、产品计划或案例当作通用验收标准。

## 阅读顺序

1. [2026-10-30详细版](2026-10-30.md)：光模块遥测、Minerva ORR、Cumulus状态一致性、SUE-T。
2. 下方为10月9、16、23日三期的去重摘要和原始链接，便于查阅。
3. 正式施工、清洁、芯序、损耗预算及回环流程仍以项目批准文件和准确型号文档为准。

## 2026-10-09｜从物理链路扩展到DPU/NVLink控制面

| 资料 | 资料日期/状态 | 工程价值与重点 |
|---|---|---|
| [NVIDIA Infra Controller v2.2](https://docs.nvidia.com/infra-controller/documentation/release-notes/2026/10/2) | 2026-10-02，软件发布 | 健康历史、DPU初始化与NVLink域运维；换线前留存重启/初始化时间线。仅适用于使用NICo的部署。 |
| [Dell iDRAC10 1.30.60.50](https://www.dell.com/support/manuals/en-us/poweredge-xe9712i/idrac10_1.30.xx_ug/firmware-version-1306050?guid=guid-e15cd156-7055-4ce4-99c8-feb235321db1&lang=en-us) | 2026-09-28/30文档更新，产品实现 | 读取准确服务器/网卡/固件及Dedicated/Shared模式；不将支持能力套用所有Grace平台。 |
| [IEEE P802.3dj D3.2 final comments](https://www.ieee802.org/3/dj/comments/D3p2/8023dj_D3p2_comments_final_clause.pdf) | 2026-09-15，草案意见处理 | R2-110等涉及LOS恢复；R2-199预算提案被拒绝，不能据此放宽验收。 |
| [DOCA GPUNetIO技术分析](https://developer.nvidia.com/blog/how-doca-gpunetio-unifies-gpu-initiated-networking-across-the-nvidia-software-stack/) | 2026-10-06，厂商分析 | GPU—PCIe—NIC路径；物理/FEC正常后继续看RDMA、队列和软件。重点架构图和数据路径。 |

English: Separate physical faults from DPU initialization, NVLink-domain control, and GPU-to-NIC software paths. Draft proposals are not approved optical budgets.

## 2026-10-16｜从能亮到误码和负载验收

| 资料 | 资料日期/状态 | 工程价值与重点 |
|---|---|---|
| [Fluke LinkWare PC release notes](https://www.flukenetworks.com/knowledge-base/release-notes-linkware-pc) | 2026年10月，Build 14；未注明日 | Windows 11 USB驱动与Versiv版本配套；先备份测试记录，再核查驱动。 |
| [EXFO HyperBlazer](https://www.exfo.com/en/products/field-network-testing/ethernet-testing/hyperblazer-series/) | 2026-10-13产品发布，技术页无独立修订日 | 光模块快速筛查与SN追溯；不能代替长时间BER或业务验收。 |
| [Keysight FITS-16CH数据表](https://www.keysight.com.cn/cn/zh/assets/3126-1801/data-sheets/Keysight-Functional-Interconnect-Test-Solutions-16CH.pdf) | 2026-10-14产品发布，数据表修订日未独立核实 | 实验室逐通道BER/FEC验证；电通道数不等于MPO芯数或逻辑口数。 |
| [GPU-Initiated Communication: Dissecting Down to the Bone](https://arxiv.org/html/2610.01380v1) | 2026-10-01，预印本 | 对比平台、时钟、队列和背景流量；结果限定于论文测试条件，不作验收门限。 |

English: Distinguish module screening, sustained BER/FEC testing, and workload validation. Record test duration, load, software, and platform.

## 2026-10-23｜管理面隔离、草案状态和多平面部署

| 资料 | 资料日期/状态 | 工程价值与重点 |
|---|---|---|
| [Dell iDRAC Direct KB 000130077](https://www.dell.com/support/kbdoc/en-us/000130077/poweredge-how-to-use-the-idrac-direct-feature) | 2026-10-16，Version 19 | 按代际检查USB-C Direct与LED；本地直连可帮助隔离管理网问题，不能证明业务链路正常。 |
| [IEEE P802.3dj Clause 12 report](https://www.ieee802.org/email/stds-802-lmsc/msg01281.html) | 2026-10-15，草案流程 | 97%批准、第三次recirculation结束、准备提交RevCom；不是正式发布标准。 |
| [Network Operator 26.7 release notes](https://docs.nvidia.com/networking/display/kubernetes2670/release-notes.html)与[Spectrum-X profile](https://docs.nvidia.com/networking/display/kubernetes2670/k8s-launch-kit/profiles/spectrum-x.html) | 2026-10-07，产品实现 | RA2.3、ConnectX-8多平面、Data Direct；核对device ID/profile、GPU-NIC affinity与DRA支持边界。 |
| [OCP Remote Optical Transceiver Messaging R0.9](https://www.opencompute.org/documents/transparent-remote-optical-transceiver-messaging-with-epps-design-specification/) | 2026-10-08，初始规范 | DSP间透明消息、lock、ePPS和RTT；与10月30日软件遥测规范互补，不是同一文件。 |
| [NVIDIA/Cisco USFP公告](https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-and-Cisco-Introduce-New-Pluggable-Optics-Form-Factor-to-Scale-AI-Factories/default.aspx) | 2026-10-12，产业计划 | “OSFP-sized”不等于OSFP兼容。仅作技术方向观察，不作为当前备件/接线依据。 |

English: Keep management access, Ethernet data paths, and NVLink control separate. Confirm hardware-specific multipane support. Planned form factors and standards-ballot milestones do not change field wiring rules.

## 后续维护规则

- 每期记录来源日期、核查日期、标准/草案/产品实现/工程推断。
- 相同资料只有实质变化才重复推荐，并写明版本差异。
- 发布日不明或仅网页抓取时间变化，不宣称“本周新发布”。
- 不转载第三方全文、图表或内部项目资料。
- 英文摘要与中文适用边界保持一致。
- 本索引为历史快照，不保证链接目标此后未改动。
