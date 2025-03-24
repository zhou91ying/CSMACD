补充数据来源说明 | Supplementary Data Sources—— Flickr-Faces-HQ (FFHQ)

为增强数据集的类别平衡性与多样性，本项目在构建过程中整合了来自 Flickr-Faces-HQ (FFHQ) 的儿童面部数据。以下为FFHQ数据的关键信息：

To enhance the category balance and diversity of the dataset, this project incorporates facial data of children from the Flickr-Faces-HQ (FFHQ) dataset. Key details about FFHQ are provided below:

FFHQ数据说明 | FFHQ Data Description
数据来源 | Source
FFHQ是由NVIDIA发布的公开人脸数据集，包含70,000张高质量（1024×1024分辨率）人像图片，覆盖广泛年龄、种族和背景特征。
FFHQ is a public face dataset released by NVIDIA, containing 70,000 high-quality (1024×1024 resolution) portrait images with diverse age, ethnicity, and background characteristics.

FFHQ Link：https://github.com/NVlabs/ffhq-dataset

子集筛选 | Subset Selection
为匹配CSMACD数据集的亚洲儿童特征，从FFHQ的亚洲子集中手动筛选出与CSMACD年龄范围（0-15岁）一致的182个儿童样本，其中男性140个，女性42个，样本的性别由人工进行判别，判断依据为儿童的发型、服饰等外在呈现，排除性别指征不明确的样本。
To align with the demographic characteristics of Asian children in the CSMACD dataset, 182 child samples within the age range of 0-15 years were manually selected from the Asian subset of FFHQ, comprising 140 males and 42 females. The gender annotation was performed manually based on external phenotypic features such as hairstyle, clothing, and other visual indicators, with samples exhibiting ambiguous gender characteristics excluded from the final selection.

用途与限制 | Purpose & Limitations
用途：作为“正常发育儿童（TD）”的补充对照组，与CSMACD自有社交媒体数据的ASD数据形成平衡对比。
Purpose: Serve as a supplementary control group for "Typically Developing (TD)" children, balancing comparisons with CSMACD's social media-sourced data.

限制：FFHQ数据为实验室环境下的标准人像，可能与真实社交媒体场景存在分布差异。
Limitations: FFHQ images are standardized studio portraits, which may differ in distribution from real-world social media scenarios.

伦理与许可 | Ethics & License
FFHQ遵循Creative Commons BY-NC-SA 4.0协议，本项目中仅使用其符合研究目的的儿童子集。
FFHQ is licensed under Creative Commons BY-NC-SA 4.0. Only a child subset relevant to research objectives is used in this project.

FFHQ原始数据未包含个人身份信息，本项目已进一步移除其元数据以确保隐私合规，仅提供经过openface处理过的面部图像数据。
The original FFHQ dataset contains no personally identifiable information To ensure privacy compliance, this project has further removed all metadata and exclusively provides facial image data preprocessed with OpenFace, which extracts anonymized facial features while discarding non-facial regions and background information.
