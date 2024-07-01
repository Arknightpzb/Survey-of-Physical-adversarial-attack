# Survey-of-Physical-adversarial-attack

## 基于补丁形态的物理对抗样本
基于干扰性补丁的物理对抗攻击指通过将**具备对抗干扰性纹理的贴纸或补丁粘贴在平面或具备较小弧度的曲面上，从而对模型产生干扰效果**的对抗攻击方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2016-CCS | 【AdvEyeglass】Accessorize to a crime: Real and stealthy attacks on state-of-the-art face recognition | [paper](https://dl.acm.org/doi/10.1145/2976749.2978392) | 面向人脸识别开发对抗眼镜| | TV,NPS(**首次**)| |
| 2019-CVPR | 【AdvPatch】Fooling automated surveillance cameras: adversarial patches to attack person detection | [论文](https://openaccess.thecvf.com/content_CVPRW_2019/papers/CV-COPS/Thys_Fooling_Automated_Surveillance_Cameras_Adversarial_Patches_to_Attack_Person_Detection_CVPRW_2019_paper.pdf)| 面向行人检测针对YOLOv2开发对抗补丁 | | EOT; TV,NPS | |

## 基于3D实体形态的物理对抗样本
基于3D实体形态的物理对抗攻击指通过将**通过改变目标物体的外型、纹理或放置具备干扰性的实体，从而在任意视角下均可对模型产生干扰效果**的对抗攻击方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2022-CVPR | 【AdvTexture】Adversarial Texture for Fooling Person Detectors in the Physical World | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_Adversarial_Texture_for_Fooling_Person_Detectors_in_the_Physical_World_CVPR_2022_paper.pdf)| 面向行人检测开发可穿戴对抗样本 | (TC-EGA)利用FCN的平移不变性构建了产生扩展性纹理的生成器，并使用Toroidal Cropping(TC)辅助训练输入至生成器的隐变量，使得纹理产生拓扑结构 | EOT,TPS; TV | |





