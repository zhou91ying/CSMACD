# CSMACD

## 介绍
中国社交媒体自闭症儿童数据集（Chinese Social Media Autism Children Dataset, CSMACD）是一个专门收集中国主流社交媒体平台上自闭症儿童与正常儿童面部图像及视频的多模态数据集。该数据集旨在支持自闭症早期筛查工具开发、行为模式分析、面部特征识别等研究，同时为心理学、医学及人工智能领域的科研人员提供高质量数据资源。数据集遵循严格的隐私保护规范，确保合法合规。<br><br>

## 数据源
平台选择：哔哩哔哩、抖音、快手、西瓜视频、腾讯视频、优酷视频；<br>
选择理由：上述平台用户基数大、内容覆盖广，且包含大量儿童相关视频，能够充分反映真实场景下的行为特征。<br><br>

## 检索关键词
#### 自闭症儿童相关
中文关键词：自闭，自闭症，孤独症，谱系，自闭症谱系，自闭症谱系障碍，阿斯伯格，毕娃，星宝，来自星星、星星的孩子，来自星星的孩子，特殊孩子；<br>
英文缩写：ASD（Autism Spectrum Disorder）；<br>

#### 正常儿童相关
人类幼崽，人类幼崽男孩，背头男孩，无刘海男孩；<br><br>
 **_补充说明_** ：关键词选择基于文献调研及平台常见标签，部分数据通过推荐算法获取（如首页推送）。<br><br>

## 儿童纳入标准
#### 通用条件
1. 年龄范围：6个月-15岁。若账号包含儿童幼年影像（如5-6个月），即使当前年龄超限，仍纳入数据；<br>
2. 多胞胎处理：双胞胎或三胞胎视为同一个体；<br>
3. 单平台去重：同一平台同一儿童的多个账号仅纳入主账号（发布视频最多、质量最优的账号）；<br>
4. 跨平台去重：同一儿童的多平台账号仅保留数据最完整的平台账号；<br>
5. 儿童性别标注——基于视频内容多维度推断<br>
    * 显性特征：儿童发型、服饰、声纹特征（若有语音）；<br>
    * 上下文信息：视频标题标签（如“男孩康复日记”）、发布者描述性文案；<br>
    * 对婴幼儿案例，额外参考抚养者称呼（如“儿子”“女儿”等代词）。<br>

#### 自闭症儿童
1. 用户简介或视频内容明确提及确诊信息（如“确诊自闭症”、“ASD诊断证明”）；<br>
2. 账号简介明确声明儿童确诊自闭症，或者账号内容包含医疗诊断证明或持续康复训练记录（以文字/视频形式呈现）；排除未提供明确诊断依据的账号。<br>

#### 正常儿童
1. 账号无任何疾病声明，且视频内容未涉及特殊医疗或干预训练。<br><br>

## 儿童视频选择标准
#### 数量
每位儿童选取1-3个视频（优先高质量片段）。<br>

#### 时长
10秒-3分钟，但考虑到不同平台的特点，视频时长也可以酌情增加。<br>

#### 排除规则
1. 宣传片、广告类视频（如机构推广、募捐视频）；<br>
2. 多人同框视频（自闭症组尽量避免其他儿童入镜）；<br>
3. 含强烈滤镜/美颜特效的内容。<br>

#### 质量要求
1. 分辨率≥720p，低分辨率视频（<720p）需包含清晰面部图像；<br>
2. 录制到儿童无遮挡正脸，儿童面部距离镜头较近，表情中性或动作幅度小，便于面部特征提取；<br>
3. 优先选取儿童幼年时期（如6个月-3岁）视频；<br>

 **_注_** ：由于某些社交平台除视频之外也支持发布图文格式内容，在选择视频时我们也将这部分内容包括在内，选取标准与视频相同。<br><br>
 
## 面部图像截取标准
#### 数量
每位儿童仅保留1张最优面部图像；<br>
#### 技术要求：
1. 完整脸部区域（含耳朵），无阴影或遮挡物；<br>
2. 面部偏转角度≤40°（基于OpenFace工具的最佳识别范围）；<br>
3. 中性表情优先，避免夸张动作（如大笑、哭泣），保持原本的脸部结构。<br><br>

## 视频格式
哔哩哔哩、抖音、快手、西瓜视频：MP4格式；<br>
腾讯视频：QLV格式；<br>
优酷视频：KUX格式。<br><br>

## 数据集特征
#### 1. 自闭症
|                  | 儿童数量            | 视频数量         | 男   | 女      |
|------------------|--------------------|------------------|------|--------|
| 哔哩哔哩          | 18                 | 50               | 13   | 5      |
| 抖音              | 42                 | 124              | 29   | 13     |
| 快手              | 45                 | 130              | 35   | 10     |
| 腾讯视频          | 20                 | 20               | 16   | 4      |
| 西瓜视频          | 54                 | 146              | 44   | 10     |
| 优酷视频          | 3                  | 5                | 3    | 0      |
| 总              | 182                | 475              | 140  | 42     |

#### 2. 发育正常儿童
|      | 儿童数量 | 视频数量 | 男   | 女  |
|------|------|------|-----|----|
| 哔哩哔哩 | 1    | 1   |   | 1  |
| 抖音   | 180   | 187  | 139  | 41 |
| 快手   | 1   | 1  | 1  |  |
| 腾讯视频 |    |    |   |   |
| 西瓜视频 |    |   |   |  |
| 优酷视频 |     |    |    |   |
| 总    | 182  | 189  | 140 | 42 |

## 数据隐私
 **儿童视频** ：仅提供视频数据的链接；<br>
 **面部图像** ：仅提供使用OpenFace 2.0进行标准化面部对齐和特征提取之后的数据。<br><br>

## 数据集结构与使用
#### 面部图像命名规则
示例：2-1-3-4<br>
第一位：平台编号（1=哔哩哔哩，2=抖音，3=快手，4=腾讯视频，5=西瓜视频，6=优酷视频，7=小红书）；<br>
第二位：平台内用户序号；<br>
第三位：该用户的视频序号；<br>
第四位：视频内面部图像序号。<br>

#### 应用场景
行为分析：结合视频时间戳分析自闭症儿童社交互动模式。<br>
AI模型训练：利用OpenFace提取的面部特征（如AU动作单元）训练分类模型。<br>
跨模态研究：关联面部特征与语音、肢体动作数据。<br>

## 版本与引用
 **版本号** ：V1.0 (2025-3-11)<br>
 **引用格式** ：<br>
 **动态更新** ：建立持续性数据采集机制，每月爬取新增符合标准的ASD/TD儿童内容，并通过版本控制（如CSMACD-v1.0, v1.1）发布增量更新。<br>

## 联系与反馈
维护团队：Xi lab实验室（邮箱：my.zhou1@siat.ac.cn）<br>
问题反馈：GitHub/Gitee仓库提交Issue或邮件联系。<br>
