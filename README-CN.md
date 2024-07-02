# Survey-of-Physical-adversarial-attack

## 基于补丁形态的物理对抗样本
基于干扰性补丁的物理对抗攻击指通过将**具备对抗干扰性纹理的贴纸或补丁粘贴在平面或具备较小弧度的曲面上，从而对模型产生干扰效果**的对抗攻击方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2016-CCS | 【AdvEyeglass】Accessorize to a crime: Real and stealthy attacks on state-of-the-art face recognition | [论文](https://dl.acm.org/doi/10.1145/2976749.2978392) | 面向人脸识别开发对抗眼镜| | ; TV,NPS(**首次**)| |
| 2017-NeurIPS | 【AdvPatch】Adversarial patch | [论文](https://arxiv.org/pdf/1712.09665.pdf) | **首次**面向分类任务设计了通用物理对抗补丁 |  | EOT | |

| 2019-CVPR | 【AdvPatch】Fooling automated surveillance cameras: adversarial patches to attack person detection | [论文](https://openaccess.thecvf.com/content_CVPRW_2019/papers/CV-COPS/Thys_Fooling_Automated_Surveillance_Cameras_Adversarial_Patches_to_Attack_Person_Detection_CVPRW_2019_paper.pdf)| 面向行人检测针对YOLOv2开发对抗补丁 | | EOT; TV,NPS | |
| 2020-ECCV, 2021-TIP | 【Bias-based Attack】Bias-based universal adversarial patch attack for automatic check-out | [论文ECCV版](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123580392.pdf), [论文TIP版](https://ieeexplore.ieee.org/document/9632406) | 针对自动购物检测系统的通用对抗补丁 |  | 利用风格迁移损失融合难样本的纹理，并结合视觉注意力机制产生干扰性纹理先验。 并使用数据流形简化训练； EOT | |
| 2022-TIFS | 【TnTAttack】TnT Attacks! Universal Naturalistic Adversarial Patches Against Deep Neural Network Systems | [paper](https://ieeexplore.ieee.org/document/9856683)\|[Project](https://TnTattacks.github.io/) | 面向自然图像分类的视觉和谐补丁| 使用了GAN-based方法，通过GAN模型的生成网络将输入向量映射成为具有常见物品形态的视觉和谐补丁，并通过调整输入向量的值来使得补丁具备对抗干扰性能| | |

## 基于3D实体形态的物理对抗攻击
基于3D实体形态的物理对抗攻击指通过将**通过改变目标物体的外型、纹理或放置具备干扰性的实体，从而在任意视角下均可对模型产生干扰效果**的对抗攻击方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2022-CVPR | 【AdvTexture】Adversarial Texture for Fooling Person Detectors in the Physical World | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_Adversarial_Texture_for_Fooling_Person_Detectors_in_the_Physical_World_CVPR_2022_paper.pdf)| 面向行人检测开发可穿戴对抗样本 | (TC-EGA)利用FCN的平移不变性构建了产生扩展性纹理的生成器，并使用Toroidal Cropping(TC)辅助训练输入至生成器的隐变量，使得纹理产生拓扑结构 | EOT,TPS; TV | |

## 无接触的物理对抗攻击
无接触的物理对抗攻击指**通过在场景中投射具备干扰性的阴影区域或改变光照条件等非直接接触干扰手段，使得模型在该场景下产生错误的决策**的对抗攻击方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
## 其他
主要收录一些做数字域对抗攻击的论文，但是提出了一些新的可用于物理域的鲁棒性增强方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2019-AAAI | 【D2P】Connecting the digital and physical world: Improving the robustness of adversarial attacks | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/3926)| 设计了Digital-to-physical Transformation(D2P)方法，使用conditional Generative Adversarial Network用于模拟真实应用场景的拍摄条件，从而使得对抗样本能够在 与实际应用场景更贴近的物理仿真图像上进行训练 | | EOT, D2P(**首次**)| |





