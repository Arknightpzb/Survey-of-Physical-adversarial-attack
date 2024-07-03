# Survey-of-Physical-adversarial-attack

## 基于补丁形态的物理对抗样本
基于干扰性补丁的物理对抗攻击指通过将**具备对抗干扰性纹理的贴纸或补丁粘贴在平面或具备较小弧度的曲面上，从而对模型产生干扰效果**的对抗攻击方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2016-CCS | 【AdvEyeglass】Accessorize to a crime: Real and stealthy attacks on state-of-the-art face recognition | [论文](https://dl.acm.org/doi/10.1145/2976749.2978392) | 面向人脸识别开发对抗眼镜| | ; TV(**首次**),NPS(**首次**)| |
| 2017-NeurIPS | 【AdvPatch】Adversarial patch | [论文](https://arxiv.org/pdf/1712.09665.pdf) | **首次**面向分类任务设计了通用物理对抗补丁 |  | EOT | |
| 2019-TOPS | 【AdvEyeglass2】A general framework for adversarial examples with objectives | [论文](https://dl.acm.org/doi/10.1145/3317611)| 面向人脸识别开发对抗眼镜 | 使用了GAN方法生成眼镜纹理：训练能够生成对抗性纹理的生成器，并基于该生成器产生的对抗性纹理制作眼镜实施攻击。 | | |
| 2019-CVPR | 【AdvPatch】Fooling automated surveillance cameras: adversarial patches to attack person detection | [论文](https://openaccess.thecvf.com/content_CVPRW_2019/papers/CV-COPS/Thys_Fooling_Automated_Surveillance_Cameras_Adversarial_Patches_to_Attack_Person_Detection_CVPRW_2019_paper.pdf)| 面向行人检测针对YOLOv2开发对抗补丁 | | EOT; TV,NPS | |
| 2019-ICCV | 【AdvPattern】advPattern: physical-world attacks on deep person re-identification via adversarially transformable patterns | [论文](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_advPattern_Physical-World_Attacks_on_Deep_Person_Re-Identification_via_Adversarially_Transformable_ICCV_2019_paper.pdf)|  **首次**面向行人re-ID（再识别）系统的补丁对抗攻击 | | EOT; TV,NPS  | |
| 2019-SIBIRCON | 【ArcFaceAttack】On adversarial patches: real-world attack on arcface-100 face recognition system | [paper](https://ieeexplore.ieee.org/document/8958134)| 面向人脸识别系统的补丁对抗攻击 | Projective transformation(简单使用了基于网格校正的投影变换模拟补丁在非平面上的布置形态); TV |
| 2020-ECCV, 2021-TIP | 【Bias-based Attack】Bias-based universal adversarial patch attack for automatic check-out | [论文ECCV版](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123580392.pdf), [论文TIP版](https://ieeexplore.ieee.org/document/9632406) | 针对自动购物检测系统的通用对抗补丁 |  | 利用风格迁移损失融合难样本的纹理，并结合视觉注意力机制产生干扰性纹理先验。 并使用数据流形简化训练； EOT | |
| 2020-ICPR | 【AdvHat】Advhat: Real-world adversarial attack on arcface face id system | [paper](https://www.computer.org/csdl/proceedings-article/icpr/2021/09412236/1tmhLeqyrHq)| 面向人脸识别的对抗性帽子（贴）| | 使用抛物线型变换(parabolic transformation)模拟平面弯曲过程，从而更好模拟补丁粘贴在帽子上的形态; TV |
| 2021-CVPR | 【TAP】Improving transferability of adversarial patches on face recognition with generative models | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Xiao_Improving_Transferability_of_Adversarial_Patches_on_Face_Recognition_With_Generative_CVPR_2021_paper.pdf) | 面向人脸识别的补丁对抗攻击| 基于在人脸生成任务上预训练的GAN，将输入向量投影成为补丁，并通过优化调整输入向量的值来使补丁具备对抗效果。|  在优化过程中使用了 momentum iterative method(MIM)和TIDIM方法提升可迁移性; EOT | |
| 2022-TIFS | 【TnTAttack】TnT Attacks! Universal Naturalistic Adversarial Patches Against Deep Neural Network Systems | [paper](https://ieeexplore.ieee.org/document/9856683)\|[Project](https://TnTattacks.github.io/) | 面向自然图像分类的视觉和谐补丁| 使用了GAN-based方法，通过GAN模型的生成网络将输入向量映射成为具有常见物品形态的视觉和谐补丁，并通过调整输入向量的值来使得补丁具备对抗干扰性能| | |

## 基于3D实体形态的物理对抗攻击
基于3D实体形态的物理对抗攻击指通过将**通过改变目标物体的外型、纹理或放置具备干扰性的实体，从而在任意视角下均可对模型产生干扰效果**的对抗攻击方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2022-CVPR | 【AdvTexture】Adversarial Texture for Fooling Person Detectors in the Physical World | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_Adversarial_Texture_for_Fooling_Person_Detectors_in_the_Physical_World_CVPR_2022_paper.pdf)| 面向行人检测开发可穿戴对抗样本 | (TC-EGA)利用FCN的平移不变性构建了产生扩展性纹理的生成器，并使用Toroidal Cropping(TC)辅助训练输入至生成器的隐变量，使得纹理产生拓扑结构 | EOT,TPS; TV | |

## 无接触的物理对抗攻击
无接触的物理对抗攻击指**通过在场景中投射具备干扰性的阴影区域或改变光照条件等非直接接触干扰手段，使得模型在该场景下产生错误的决策**的对抗攻击方法
与放置人工设计的对抗对象的物理攻击相比，无接触的攻击避免了对物理实体的修改，并且可以通过改变投影模式进行瞬态和动态的攻击。
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2020-NeurIPS | 【ViewFool】ViewFool: Evaluating the Robustness of Visual Recognition to Adversarial Viewpoints | [论文](https://openreview.net/forum?id=X0m9q0IcsmX)| 面向分类的视角变换对抗攻击 | 利用充分训练的NeRF表征3D场景，通过优化调整相机位姿寻找到能使分类模型产生错误预测结果的对抗性视角 | | |
| 2021-CVPR | 【OPAD】Optical adversarial attack | [论文](https://openaccess.thecvf.com/content/ICCV2021W/AROW/papers/Gnanasambandam_Optical_Adversarial_Attack_ICCVW_2021_paper.pdf)| 面向自然图像分类的无接触结构光对抗攻击 | 该方法建立投影仪-摄像机模型，并将其引入到对抗攻击生成中，校正了投影仪辐射响应的非线性和场景光谱响应的空间变化特性，实现利用结构光照明来改变目标物体的外观产生对抗效果。| | |
| 2021-CVPR | 【LEDAttack】Invisible perturbations: Physical adversarial examples exploiting the rolling shutter effect | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Sayles_Invisible_Perturbations_Physical_Adversarial_Examples_Exploiting_the_Rolling_Shutter_Effect_CVPR_2021_paper.pdf)\|[code](https://github.com/EarlMadSec/invis-perturbations) | 面向自然图像分类的无接触LED投影攻击 | 利用商品相机中的辐射卷帘快门效应，提出基于LED投影的对抗攻击，使得经过卷帘快门相机拍摄的图像上出现的具备干扰性的条纹图案。 | EOT | |
| 2021-CVPR | 【AdvLB】Adversarial laser beam: Effective physical-world attack to dnns in a blink | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Duan_Adversarial_Laser_Beam_Effective_Physical-World_Attack_to_DNNs_in_a_CVPR_2021_paper.pdf)| 面向自然图像分类的无接触光照对抗攻击 | 基于对激光束的参数化建模，将激光束投射到自然图像中，并利用启发式搜索方法寻找最具备对抗干扰性能的激光束参数 | | EOT | |
| 2022-IEEE VR | 【SPAA】SPAA: Stealthy Projector-based Adversarial Attacks on Deep Image Classifiers | [论文](https://ieeexplore.ieee.org/document/9756739) | 面向自然图像分类的投影攻击 | 设计了PCNet用于模拟投影仪投影图像到场景中并被相机拍摄成像过程，基于充分训练的PCNet通过将对抗性噪声投影到目标物体所在场景实现对分类面向的干扰 | 本质上属于D2P的应用 | |
| 2022-CVPR | 【ShadowAttack】Shadows can be dangerous: Stealthy and effective physical-world adversarial attack by natural phenomenon | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhong_Shadows_Can_Be_Dangerous_Stealthy_and_Effective_Physical-World_Adversarial_Attack_CVPR_2022_paper.pdf)| 面向自然图像的阴影对抗攻击 | 通过对自然条件下的阴影进行参数化建模，将阴影投射在目标物体表面产生对抗干扰效果，通过PSO启发式寻优进行优化 | EOT | |
## 其他
主要收录一些做数字域对抗攻击的论文，但是提出了一些新的可用于物理域的鲁棒性增强方法
| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2019-AAAI | 【D2P】Connecting the digital and physical world: Improving the robustness of adversarial attacks | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/3926)| 设计了Digital-to-physical Transformation(D2P)方法，使用conditional Generative Adversarial Network用于模拟真实应用场景的拍摄条件，从而使得对抗样本能够在 与实际应用场景更贴近的物理仿真图像上进行训练 | | EOT, D2P(**首次**)| |





