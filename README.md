<div align="center">

<h1>Survey-of-Physical-adversarial-attack</h1>

[ [简体中文](README.md) | [English](README-EN.md) ]

![](https://komarev.com/ghpvc/?username=SurveyPhysicsAttack&label=visitors)
![GitHub stars](https://badgen.net/github/stars/Arknightpzb/Survey-of-Physical-adversarial-attack)
[![](https://img.shields.io/badge/license-MIT-green)](#License)

</div>

## Contributing

本仓库主要关注与目前的**物理对抗攻击方法**，并按攻击形态将当前方法分为**对抗补丁(Patch)，3D实体，无接触投影**三大类

欢迎大家积极补充，请随时发送Pull Request~

## 目录
+ [基于补丁形态的物理对抗样本](#基于补丁形态的物理对抗样本)
+ [基于3D实体形态的物理对抗攻击](#基于3D实体形态的物理对抗攻击)
+ [无接触的物理对抗攻击](#无接触的物理对抗攻击)
+ [其他](#其他)


## 基于补丁形态的物理对抗样本
基于干扰性补丁的物理对抗攻击指通过将**具备对抗干扰性纹理的贴纸或补丁粘贴在平面或具备较小弧度的曲面上，从而对模型产生干扰效果**的对抗攻击方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2016-CCS | 【AdvEyeglass】Accessorize to a crime: Real and stealthy attacks on state-of-the-art face recognition | [论文](https://dl.acm.org/doi/10.1145/2976749.2978392) | 面向人脸识别开发对抗眼镜| | ; TV(**首次**),NPS(**首次**)| |
| 2017-NeurIPS | 【AdvPatch】Adversarial patch | [论文](https://arxiv.org/pdf/1712.09665.pdf) | **首次**面向分类任务设计了通用物理对抗补丁 |  | EOT | |
| 2018-CVPR | 【RP2】Robust physical-world attacks on deep learning visual classification | [论文](https://openaccess.thecvf.com/content_cvpr_2018/papers/Eykholt_Robust_Physical-World_Attacks_CVPR_2018_paper.pdf)| 面向自然图像（交通场景）分类的补丁对抗攻击 | | （设计思路）从实验中观察到掩膜的位置对攻击的有效性有影响。因此，本文从分类的角度假设物体具有强、弱物理特征，并定位掩码对弱区域进行攻击。**首次**提出RP2，首先使用L1范数约束辅助对抗扰动优化，随后以扰动存在的位置构建Mask掩膜，再对掩膜内的扰动使用L2范数约束优化，实现对抗扰动的鲁棒性提升,NPS |
| 2018-USENIX-W | 【RP2+】Physical adversarial examples for object detectors   | [论文](https://www.usenix.org/system/files/conference/woot18/woot18-paper-eykholt.pdf)| | 将RP2扩展到了目标检测任务上 | RP2,TV,NPS |
| 2018-ECMLPKDD | 【ShapeShifter】Shapeshifter: Robust physical adversarial attack on faster r-cnn object detector | [论文](https://link.springer.com/chapter/10.1007/978-3-030-10925-7_4) | 面向自然图像的对抗攻击（弥散） |  | EOT |
| 2019-TOPS | 【AdvEyeglass2】A general framework for adversarial examples with objectives | [论文](https://dl.acm.org/doi/10.1145/3317611)| 面向人脸识别开发对抗眼镜 | 使用了GAN方法生成眼镜纹理：训练能够生成对抗性纹理的生成器，并基于该生成器产生的对抗性纹理制作眼镜实施攻击。 | | |
| 2019-CVPR | 【AdvPatch】Fooling automated surveillance cameras: adversarial patches to attack person detection | [论文](https://openaccess.thecvf.com/content_CVPRW_2019/papers/CV-COPS/Thys_Fooling_Automated_Surveillance_Cameras_Adversarial_Patches_to_Attack_Person_Detection_CVPRW_2019_paper.pdf)| 面向行人检测针对YOLOv2开发对抗补丁 | | EOT; TV,NPS | |
| 2019-ICCV | 【AdvPattern】advPattern: physical-world attacks on deep person re-identification via adversarially transformable patterns | [论文](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_advPattern_Physical-World_Attacks_on_Deep_Person_Re-Identification_via_Adversarially_Transformable_ICCV_2019_paper.pdf)|  **首次**面向行人re-ID（再识别）系统的补丁对抗攻击 | | EOT; TV,NPS  | |
| 2019-SIBIRCON | 【ArcFaceAttack】On adversarial patches: real-world attack on arcface-100 face recognition system | [论文](https://ieeexplore.ieee.org/document/8958134)| 面向人脸识别系统的补丁对抗攻击 | Projective transformation(简单使用了基于网格校正的投影变换模拟补丁在非平面上的布置形态); TV |
| 2019-AAAI | 【PS_GAN】Perceptual-sensitive gan for generating adversarial patches | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/3893)| 面向自然图像分类的对抗补丁攻击 | 使用了GAN方法产生视觉和谐的对抗补丁，在确定补丁位置时使用了GradCAM注意力图选取网络最关注的部分进行布置，实施对抗干扰。 | ; TV |
| 2019-CCS  | 【NestedAE】Seeing isn't believing: Towards more robust adversarial attack against real world object detectors |[论文](https://dl.acm.org/doi/10.1145/3319535.3354259)| 面向自然图像目标检测的对抗攻击 | | 额外计算特征差异损失函数，辅助对抗样本进行训练。 | |
| 2019-ICCV | 【PATAttack】Physical adversarial textures that fool visual object tracking | [论文](https://openaccess.thecvf.com/content_ICCV_2019/papers/Wiyatno_Physical_Adversarial_Textures_That_Fool_Visual_Object_Tracking_ICCV_2019_paper.pdf) | 面向行人轨迹预测的补丁对抗攻击| | EOT | 使用gazebo搭建仿真环境 |
| 2020-CVPR | 【AdvCam】Adversarial camouflage: Hiding physical-world attacks with natural styles | [论文](https://openaccess.thecvf.com/content_CVPR_2020/papers/Duan_Adversarial_Camouflage_Hiding_Physical-World_Attacks_With_Natural_Styles_CVPR_2020_paper.pdf) | 面向自然图像分类的对抗样本 | | 使用风格迁移损失为目标物体生成环境自适应且具有一定视觉隐蔽性的对抗纹理/图案, EOT; |
| 2020-ECCV | 【Adversarial T-Shirt】Adversarial t-shirt! evading person detectors in a physical world | [论文](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123500647.pdf)| 面向行人检测的补丁对抗攻击 | | EOT,TPS(**首次使用TPS校正模拟衣服褶皱影响**) | |
| 2020-ECCV | 【Invisible Cloak2】Making an invisibility cloak: Real world adversarial attacks on object detectors | [论文](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123490001.pdf) | 面向行人检测的通用对抗性衣服 | 通用对抗样本 | TPS,TV,Ensemble（模型集成） | |
| 2020-ECCV, 2021-TIP | 【Bias-based Attack】Bias-based universal adversarial patch attack for automatic check-out | [论文ECCV版](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123580392.pdf), [论文TIP版](https://ieeexplore.ieee.org/document/9632406) | 针对自动购物检测系统的通用对抗补丁 |  | 利用风格迁移损失融合难样本的纹理，并结合视觉注意力机制产生干扰性纹理先验。 并使用数据流形简化训练； EOT | |
| 2020-ICPR | 【AdvHat】Advhat: Real-world adversarial attack on arcface face id system | [论文](https://www.computer.org/csdl/proceedings-article/icpr/2021/09412236/1tmhLeqyrHq)| 面向人脸识别的对抗性帽子（贴）| | 使用抛物线型变换(parabolic transformation)模拟平面弯曲过程，从而更好模拟补丁粘贴在帽子上的形态; TV |
| 2020-CVPR | 【PhysGAN】Physgan: Generating physical-world-resilient adversarial examples for autonomous driving | [论文](https://openaccess.thecvf.com/content_CVPR_2020/papers/Kong_PhysGAN_Generating_Physical-World-Resilient_Adversarial_Examples_for_Autonomous_Driving_CVPR_2020_paper.pdf) | 面向自动驾驶系统（转角预测）的补丁对抗攻击 | 利用了GAN方法来使得路牌产生对抗干扰效果进而使得自动驾驶系统无法准确预测转角角度 | | |
| 2020-Computers <br/>& Security | 【LPRAttack】Spot evasion attacks: Adversarial examples for license plate recognition systems with convolutional neural networks | [论文](https://www.sciencedirect.com/science/article/pii/S0167404820301000)| 面向车牌识别的补丁对抗攻击 | 使用污泥点作为对抗补丁，通过遗传算法来寻找最具备干扰性的补丁位置，进而实施对抗干扰 | | |
| 2020-AAAI | 【LPRAttack】Beyond digital domain: Fooling deep learning based recognition system in physical world | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/5459) | 面向车牌识别的补丁对抗攻击 | 攻击了SSD | ; TV | |
| 2021-AAAI | 【BulbAttack】Fooling thermal infrared pedestrian detectors in real world using small bulbs | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/16477)| **首个**面向红外行人检测的对抗补丁 | 以小灯泡为发热材料，提出了一种基于高斯单元的对抗板 | EOT,TV | 材料：小灯泡 |
| 2021-AAAI  | 【MTD】Towards Universal Physical Attacks on Single Object Tracking | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/16211) | 面向物体跟踪的补丁对抗攻击| | EOT,TV, 提出最大纹理差异损失Maximum Textural Discrepancy用于干扰模型对目标对象的跟踪 | |
| 2021-MM | 【LAP】Legitimate Adversarial Patches: Evading Human Eyes and Detection Models in the Physical World | [论文](https://dl.acm.org/doi/10.1145/3474085.3475653) | 面向行人检测的补丁对抗攻击 | 将对抗噪声藏在给定的视觉和谐图像（无害图像，或称为具备应用合理性的图像）中 | ; TV,NPS |  |
| 2021-CVPR | 【TAP】Improving transferability of adversarial patches on face recognition with generative models | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Xiao_Improving_Transferability_of_Adversarial_Patches_on_Face_Recognition_With_Generative_CVPR_2021_paper.pdf) | 面向人脸识别的补丁对抗攻击| 基于在人脸生成任务上预训练的GAN，将输入向量投影成为补丁，并通过优化调整输入向量的值来使补丁具备对抗效果。|  在优化过程中使用了 momentum iterative method(MIM)和TIDIM方法提升可迁移性; EOT | |
| 2021-CVPR | 【TranslucentPatch】The translucent patch: A physical and universal attack on object detectors | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Zolfi_The_Translucent_Patch_A_Physical_and_Universal_Attack_on_Object_CVPR_2021_paper.pdf) | 面向自然图像识别的补丁攻击 | 将补丁建模为半透明的薄片，假设攻击者可以接触到成像设备，将薄片粘贴于成像设备上，产生视觉干扰区域，实现通用对抗干扰 | NPS | |
| 2022-TIFS | 【TnTAttack】TnT Attacks! Universal Naturalistic Adversarial Patches Against Deep Neural Network Systems | [论文](https://ieeexplore.ieee.org/document/9856683) | 面向自然图像分类的视觉和谐补丁| 使用了GAN-based方法，通过GAN模型的生成网络将输入向量映射成为具有常见物品形态的视觉和谐补丁，并通过调整输入向量的值来使得补丁具备对抗干扰性能| | |
| 2021-ICCV | 【NaturalisticPatch】Naturalistic physical adversarial patch for object detectors | [论文](https://openaccess.thecvf.com/content/ICCV2021/papers/Hu_Naturalistic_Physical_Adversarial_Patch_for_Object_Detectors_ICCV_2021_paper.pdf) | 面向行人检测的补丁对抗攻击 | 基于隐变量的GAN对抗攻击，GAN在自然图像中进行预训练。 | TV | |
| 2022-TPAMI | 【AdvSticker】Adversarial Sticker: A Stealthy Attack Method in the Physical World | [论文](https://ieeexplore.ieee.org/document/9779913)| 面向人脸识别的对抗贴纸| 设计了基于区域的启发式差分进化算法，寻找给定贴纸的最具备对抗干扰性的位置参数，通过在相应位置粘贴给定贴纸实现对抗攻击。 | 在X-Z平面上bending（翘曲）并在Y-Z平面上rotating（旋转）来模拟贴纸在面部的粘贴情况 | |
| 2022-TPAMI | 【SOPP】Simultaneously Optimizing Perturbations and Positions for Black-box Adversarial Patch Attacks | [论文](https://arxiv.org/abs/2212.12995)| 面向人脸识别的补丁对抗攻击 | 使用强化学习同时优化对抗补丁的纹理和位置，实现了基于查询的黑盒物理对抗攻击 | | | |
| 2022-CVPR | 【QRAttack】Infrared Invisible Clothing: Hiding from Infrared Detectors at Multiple Angles in Real World | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhu_Infrared_Invisible_Clothing_Hiding_From_Infrared_Detectors_at_Multiple_Angles_CVPR_2022_paper.pdf)| 面向行人检测的对抗涂装 | 使用二值化的对抗单元进行堆砌，形成类似二维码的对抗纹理 | EOT, TPS | 使用气凝胶毛毡制作红外对抗涂装 |
| 2022-WACV | 【AerialAttack】Physical adversarial attacks on an aerial imagery object detector | [论文](https://openaccess.thecvf.com/content/WACV2022/papers/Du_Physical_Adversarial_Attacks_on_an_Aerial_Imagery_Object_Detector_WACV_2022_paper.pdf) | **首个**面向遥感场景的物理对抗补丁 | EOT; TV,NPS | |
| 2022-WACV | 【RWAE】Evaluating the robustness of semantic segmentation for autonomous driving against real-world adversarial patch attacks | [论文](https://openaccess.thecvf.com/content/WACV2022/papers/Nesti_Evaluating_the_Robustness_of_Semantic_Segmentation_for_Autonomous_Driving_Against_WACV_2022_paper.pdf) | 面向自然图像分割的对抗补丁 | EOT | 使用了无人驾驶仿真环境CARLA on Unreal Engine |
| 2022-ECCV | 【MDEAttack】Physical attack on monocular depth estimation with optimal adversarial patches | [论文](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136980504.pdf) | 面向自动驾驶深度估计的补丁对抗攻击 | 提出自适应mask生成方法，自适应地调整补丁位置与形状 | EOT; StyleTransfer |  |
| 2023-CVPR | Physically Adversarial Infrared Patches with Learnable Shapes and Locations | [论文]([https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136980504.pdf](https://openaccess.thecvf.com/content/CVPR2023/papers/Wei_Physically_Adversarial_Infrared_Patches_With_Learnable_Shapes_and_Locations_CVPR_2023_paper.pdf)) | 面向自动驾驶深度估计的补丁对抗攻击 | 提出自适应mask生成方法，自适应地调整补丁位置与形状 | EOT; StyleTransfer |  |

## 基于3D实体形态的物理对抗攻击
基于3D实体形态的物理对抗攻击指通过将**通过改变目标物体的外型、纹理或放置具备干扰性的实体，从而在任意视角下均可对模型产生干扰效果**的对抗攻击方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2019-arXiv | 【LiDAR Advobject】Adversarial Objects Against LiDAR-Based Autonomous Driving Systems | [论文](https://arxiv.org/pdf/1907.05418) | （**首个**）面向自动驾驶雷达系统的对抗实体 | 设计了基于点云的对抗性实体生成方法，通过对端到端地优化点云集合，产生对抗性实体 | | 在Baidu Apollo Autonomous Driving platform (V2.0)进行数据域对抗生成，实用MeshLab构建、渲染3D实体 |
| 2019-ICLR | 【CAMOU】CAMOU: Learning A Vehicle Camouflage For Physical Adversarial Attack On Object Detections In The Wild | [论文](https://openreview.net/pdf?id=SJgEl3A5tm)  | 面向车辆目标检测的对抗涂装 | 利用了3D模型和渲染技术，未公开涂装模拟布置的细节 |EOT| 仿真环境使用Unreal |
| 2020-arXiv | 【ER】Physical adversarial attack on vehicle detector in the carla simulator | [论文](https://arxiv.org/pdf/2007.16118.pdf)| 面向车俩检测的对抗涂装| 使用Enlarge（像素放大）和Repeat（方块堆砌）方法产生mosaic-like的迷彩涂装，通过启发式搜索提升对抗干扰性能 | |只在Unreal仿真环境中做了，没做现实世界验证|
| 2020-CVPR | 【UPC】Universal physical camouflage attacks on object detectors | [论文](https://openaccess.thecvf.com/content_CVPR_2020/papers/Huang_Universal_Physical_Camouflage_Attacks_on_Object_Detectors_CVPR_2020_paper.pdf)| 面向行人检测的对抗涂装 | 通用对抗涂装（使用自然图案作为初始值） | EOT | 公开仿真环境平台AttackScenes，可实现多个场景内灯光、视点、位置和角度的自由切换组合 |
| 2021-CVPR | 【DAS】Dual attention suppression attack: Generate adversarial camouflage in physical world | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Wang_Dual_Attention_Suppression_Attack_Generate_Adversarial_Camouflage_in_Physical_World_CVPR_2021_paper.pdf) | 面向车辆目标检测的对抗涂装| 结合可微渲染技术，pixel-wise的优化方法，初始值为自然图案的局部涂装 | TV, 额外设计了Model Attention evasion 和Human Attention evasion(注重边缘信息：Since humans pay more attention to shapes when focusing on objects and making predictions)损失函数，用于增强通用性和视觉和谐度  | 使用了无人驾驶仿真环境CARLA on Unreal Engine |
| 2022-IJCAI | 【CAC】Learning Coated Adversarial Camouflages for Object Detectors | [论文](https://www.ijcai.org/proceedings/2022/0125.pdf) | 面向车辆检测的对抗涂装 | 使用3D渲染实现任意视角对抗 | EOT | 使用Unity仿真环境搭建|
| 2022-AAAI | 【FCA】Fca: Learning a 3d full-coverage vehicle camouflage for multi-view physical adversarial attack | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/20141) | 面向车辆目标检测的对抗涂装| 结合可微渲染技术，pixel-wise的优化方法，全身涂装| TV | 使用了无人驾驶仿真环境CARLA |
| 2022-ECMLPKDD | 【AdvMask】Adversarial Mask: Real-World Adversarial Attack Against Face Recognition Models | [论文](https://2022.ecmlpkdd.org/wp-content/uploads/2022/09/sub_406.pdf)| 面向人脸识别的对抗口罩 | 利用人脸关键点将对抗性纹理布置到口罩佩戴位置，并使用3D人脸重建在人脸图像上布置口罩 | EOT; TV | |
| 2022-CVPR | 【AdvTexture】Adversarial Texture for Fooling Person Detectors in the Physical World | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Hu_Adversarial_Texture_for_Fooling_Person_Detectors_in_the_Physical_World_CVPR_2022_paper.pdf)| 面向行人检测开发可穿戴对抗样本 | (TC-EGA)利用FCN的平移不变性构建了产生扩展性纹理的生成器，并使用Toroidal Cropping(TC)辅助训练输入至生成器的隐变量，使得纹理产生拓扑结构 | EOT,TPS; TV | |
| 2022-CVPR | 【DTA】DTA: Physical Camouflage Attacks using Differentiable Transformation Network | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Suryanto_DTA_Physical_Camouflage_Attacks_Using_Differentiable_Transformation_Network_CVPR_2022_paper.pdf) | 面向车辆检测的对抗涂装 | 使用3D渲染实现任意视角对抗 | 设计了DTN变换网络，实现了将涂装纹理模拟布置到目标车辆表面，同时不改变其在现实世界中的光照轮廓等属性，更好地模拟了特定场景下应用对抗涂装的目标外观, EOT | 使用了无人驾驶仿真环境CARLA on Unreal Engine |
| 2023-ICCV | 【ACTIVE】ACTIVE:Towards Highly Transferable 3D Physical Camouflage for Universal and Robust V ehicle Evasion | [论文](https://openaccess.thecvf.com/content/ICCV2023/papers/Suryanto_ACTIVE_Towards_Highly_Transferable_3D_Physical_Camouflage_for_Universal_and_ICCV_2023_paper.pdf)| 面向车辆目标检测的对抗涂装 | (ACTIVE)利用TPM (Triplanar Mapping)三平面纹理映射技术生成不依赖于特定车辆的纹理（多个车辆可以使用同一纹理） | Random Output Augmentation (ROA)数字域的随机输出增强 | 使用了无人驾驶仿真环境CARLA on Unreal Engine|
| 2024-arXiv | 【RAUCA】RAUCA: A Novel Physical Adversarial Attack on Vehicle Detectors via Robust and Accurate Camouflage Generation | [论文](https://arxiv.org/pdf/2402.15853)| 面向车辆目标检测的对抗涂装 | (RAUCA)利用新的神经渲染组件neural Renderer Plus(NRP)，捕捉渲染中的环境特征，提升不同天气条件下产生的对抗涂装的有效性| | 用CARLA构建了multi-weather数据集|
| 2024-NEURAL NETWORKS | 【AdvIC】Adversarial Infrared Curves: An Attack on Infrared Pedestrian Detectors in the Physical World | [论文](https://arxiv.org/pdf/2312.14217)| 面向行人检测的红外对抗样本 | (AdvIC)利用粒子群算法优化生成Bezier曲线，并在物理领域使用冷补丁实现对抗红外曲线AdvIC | EOT | |
| 2024-CVPR | 【TT3D】Towards Transferable Targeted 3D Adversarial Attack in the Physical World | [论文](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_Towards_Transferable_Targeted_3D_Adversarial_Attack_in_the_Physical_World_CVPR_2024_paper.pdf)| 3D物理对抗 | (TT3D)利用一个名为TT3D的新框架生成可迁移的3D对抗样本，该框架利用NeRF从多视角输入重建3Dmesh，减轻了3D对抗对预先存在的3Dmesh的依赖，扩大了3D攻击的适用范围 | EOT | |
| 2024-CVPR | 【3D2Fool】Physical 3D Adversarial Attacks against Monocular Depth Estimation in Autonomous Driving | [论文](https://XXX)| 面向自动驾驶单目深度估计的对抗涂装 | (3D2Fool)利用texture conversion纹理转换模块以重复的方式将对抗性纹理种子转换为车辆纹理，生成与对象无关的对抗性纹理，通过physical augmentation物理增强模块集成天气变化提升在在各种天气条件下的鲁棒性| EOT, NPS | |

## 无接触的物理对抗攻击
无接触的物理对抗攻击指**通过在场景中投射具备干扰性的阴影区域或改变光照条件等非直接接触干扰手段，使得模型在该场景下产生错误的决策**的对抗攻击方法
与放置人工设计的对抗对象的物理攻击相比，无接触的攻击避免了对物理实体的修改，并且可以通过改变投影模式进行瞬态和动态的攻击。

| 年份-刊物                           | 标题 | 链接 | 论文解决的关键问题           | 建模方法创新点                                                                              | 增强方法与约束条件 | 评估方案增量         |
|---------------------------------| ------------------------------------------------------------ | ------- |---------------------|--------------------------------------------------------------------------------------| ------------------------------------------------------------ |----------------|
| 2020-CVPRW                      | Adversarial Light Projection Attacks on Face Recognition Systems: A Feasibility Study | [论文](https://arxiv.org/pdf/2003.11145)| 面向人脸识别的对抗攻击         | 通过对投影纹理的位置以及颜色进行校正，得到更鲁邦的攻击效果                                                        | |                |
| 2020-NeurIPS                    | 【ViewFool】ViewFool: Evaluating the Robustness of Visual Recognition to Adversarial Viewpoints | [论文](https://openreview.net/forum?id=X0m9q0IcsmX)| 面向分类的视角变换对抗攻击       | 利用充分训练的NeRF表征3D场景，通过优化调整相机位姿寻找到能使分类模型产生错误预测结果的对抗性视角                                  | |                |
| 2021-CVPR                       | 【OPAD】Optical adversarial attack | [论文](https://openaccess.thecvf.com/content/ICCV2021W/AROW/papers/Gnanasambandam_Optical_Adversarial_Attack_ICCVW_2021_paper.pdf)| 面向自然图像分类的无接触结构光对抗攻击 | 该方法建立投影仪-摄像机模型，并将其引入到对抗攻击生成中，校正了投影仪辐射响应的非线性和场景光谱响应的空间变化特性，实现利用结构光照明来改变目标物体的外观产生对抗效果。 | |                |
| 2021-CVPR                       | 【LEDAttack】Invisible perturbations: Physical adversarial examples exploiting the rolling shutter effect | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Sayles_Invisible_Perturbations_Physical_Adversarial_Examples_Exploiting_the_Rolling_Shutter_Effect_CVPR_2021_paper.pdf)| 面向自然图像分类的无接触LED投影攻击 | 利用商品相机中的辐射卷帘快门效应，提出基于LED投影的对抗攻击，使得经过卷帘快门相机拍摄的图像上出现的具备干扰性的条纹图案。                       | EOT |                |
| 2021-CVPR                       | 【AdvLB】Adversarial laser beam: Effective physical-world attack to dnns in a blink | [论文](https://openaccess.thecvf.com/content/CVPR2021/papers/Duan_Adversarial_Laser_Beam_Effective_Physical-World_Attack_to_DNNs_in_a_CVPR_2021_paper.pdf)| 面向自然图像分类的无接触光照对抗攻击  | 基于对激光束的参数化建模，将激光束投射到自然图像中，并利用启发式搜索方法寻找最具备对抗干扰性能的激光束参数                                | | EOT            | |
| 2022-IEEE VR                    | 【SPAA】SPAA: Stealthy Projector-based Adversarial Attacks on Deep Image Classifiers | [论文](https://ieeexplore.ieee.org/document/9756739) | 面向自然图像分类的投影攻击       | 设计了PCNet用于模拟投影仪投影图像到场景中并被相机拍摄成像过程，基于充分训练的PCNet通过将对抗性噪声投影到目标物体所在场景实现对分类面向的干扰          | 本质上属于D2P的应用 |                |
| 2021-USENIX Security            | 【SLAP】SLAP: Improving Physical Adversarial Examples with Short-Lived Adversarial Perturbations | [论文](https://www.usenix.org/system/files/sec21fall-lovisotto.pdf)| 面向自然图像检测的投影对抗攻击     |                                                                                      | EOT; TV,NPS（投影仪版本）|                |
| 2022-CVPR                       | 【ShadowAttack】Shadows can be dangerous: Stealthy and effective physical-world adversarial attack by natural phenomenon | [论文](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhong_Shadows_Can_Be_Dangerous_Stealthy_and_Effective_Physical-World_Adversarial_Attack_CVPR_2022_paper.pdf)| 面向自然图像的阴影对抗攻击       | 通过对自然条件下的阴影进行参数化建模，将阴影投射在目标物体表面产生对抗干扰效果，通过PSO启发式寻优进行优化                               | EOT |                |
| 2022-ACML                       | Adversarial laser spot: Robust and covert physical-world attack to dnns | [论文](https://proceedings.mlr.press/v189/hu23b/hu23b.pdf)| 面向标志牌的对抗攻击          | 利用多束激光点&遗传算法，实现攻击                                                                    | |  |
| 2022-Image and Vision Computing | Adversarial color projection: A projector-based physical-world attack to DNNs | [论文](https://arxiv.org/pdf/2209.09652)| 面向标志牌的对抗攻击          | 投影颜色，模拟霓虹灯之类的，完全覆盖住标志牌                                                               | |  |
| 2023-ICCV                       | Rfla: A stealthy reflected light adversarial attack in the physical world | [论文](https://openaccess.thecvf.com/content/ICCV2023/papers/Wang_RFLA_A_Stealthy_Reflected_Light_Adversarial_Attack_in_the_Physical_ICCV_2023_paper.pdf)| 面向标志牌的对抗攻击          | 利用镜子，几张带颜色的塑料纸，以及一张裁剪的纸，通过粒子种群优化算法，来实现标志牌的攻击                                         | |  |
| 2023-ICCVW                      | Adversarial Examples with Specular Highlights | [论文](https://openaccess.thecvf.com/content/ICCV2023W/AROW/papers/Vats_Adversarial_Examples_with_Specular_Highlights_ICCVW_2023_paper.pdf)| 提了两个imagenet对抗数据集   | 通过高光数据增强，在增强数据中找难样本，构成数据集。没有用到梯度迭代来生成对抗样本。                                           | |  |
| 2024-TBD                        | Imperceptible Physical Attack against Face Recognition Systems via LED Illumination Modulation | [论文](https://ieeexplore.ieee.org/abstract/document/10535230)| 面向人脸识别的对抗攻击         | 通过调制LED的变化频率，利用相机成像特性，实现拍摄图像表面的线性条纹，进而实现攻击                                           | |  |
| 2024-WACV                       | Natural Light Can Also be Dangerous: Traffic Sign Misinterpretation Under Adversarial Natural Light Attacks | [论文](https://openaccess.thecvf.com/content/WACV2024/papers/Hsiao_Natural_Light_Can_Also_Be_Dangerous_Traffic_Sign_Misinterpretation_Under_WACV_2024_paper.pdf)| 面向标志牌的对抗攻击          | 先训一个generator能生成标志牌上的亮光，与真实分布接近，之后再用ZOO灰度攻击方式来打                                      | |  |
| 2024-IOT                        | OptiCloak: Blinding Vision-Based Autonomous Driving Systems Through Adversarial Optical Projection | [论文](https://ieeexplore.ieee.org/abstract/document/10538370)| 面向自动驾驶的对抗攻击         | 考虑投影过程的重影现象、几何变形问题、反射光问题，得到更鲁邦的攻击效果                                                  | | 实际场景无人机投射至车辆后窗 |
| 2024-arxiv                      | Invisible Reflections: Leveraging Infrared Laser Reflections to Target Traffic Sign Perception | [论文](https://arxiv.org/pdf/2401.03582)| 面向标志牌的对抗攻击          | 利用红外激光加热物体表面，实现肉眼不可见的攻击                                                              | |  |
| 2024-CVIU                       | Adversarial Neon Beam: A light-based physical attack to DNNs | [论文](https://arxiv.org/pdf/2204.00853)| 面向标志牌的对抗攻击          | 利用多束范围较大的带颜色的激光，实现攻击效果                                                               | |  |
| 2024-IET-CV                     | Adversarial catoptric light: An effective, stealthy and robust physical‐world attack to DNNs | [论文](https://ietresearch.onlinelibrary.wiley.com/doi/pdfdirect/10.1049/cvi2.12264)| 面向标志牌的对抗攻击          | 相比于shadow attack，该方法利用反光镜来来投射高光，实现攻击效果                                               | |  |

## 其他
主要收录一些做数字域对抗攻击的论文，但是提出了一些新的可用于物理域的鲁棒性增强方法

| 年份-刊物 | 标题 | 链接 | 论文解决的关键问题 | 建模方法创新点 | 增强方法与约束条件 | 评估方案增量 |
| ------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------- |
| 2018-ICML | 【EOT】Synthesizing robust adversarial examples | [论文]([https://ojs.aaai.org/index.php/AAAI/article/view/3926](https://arxiv.org/pdf/1707.07397))| | | EOT(**首次**)(Adding a transformation step into the optimization process of generating adversarial perturbations.)| |
| 2019-AAAI | 【D2P】Connecting the digital and physical world: Improving the robustness of adversarial attacks | [论文](https://ojs.aaai.org/index.php/AAAI/article/view/3926)| 设计了Digital-to-physical Transformation(D2P)方法，使用conditional Generative Adversarial Network用于模拟真实应用场景的拍摄条件，从而使得对抗样本能够在 与实际应用场景更贴近的物理仿真图像上进行训练 | | EOT, D2P(**首次**)| |





