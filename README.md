# CSMACD

## Description
The Chinese Social Media Autism Children Dataset (CSMACD) is a multimodal dataset collecting facial images and videos of autistic and typical-developing children from mainstream Chinese social media platforms. It aims to support research on autism early screening tools, behavioral pattern analysis, and facial feature recognition, and offers high-quality data for researchers in psychology, medicine, and AI. The dataset strictly follows privacy protection standards to ensure legality and compliance.<br><br>

## Data Sources
Platform Selection：Bilibili, Douyin, Quick Worker, Watermelon video, Tencent Video, and Youku Video；<br>
Reasons：These platforms have a large user base and wide content coverage, with numerous children-related videos, which can effectively reflect real world behavioral characteristics.<br><br>

## Search Keywords
#### Related to Autistic Children
Chinese Keywords：ASD, autism, autistic, spectrum, autism spectrum, autism spectrum disorder, Asperger's, Biwa, Star Baby, children from the stars, special children；<br>
English Abbreviation：ASD（Autism Spectrum Disorder）；<br>

#### Related to Typically-Developing Children
Human child，Young human boy，Slicked-back hairstyle boy，No-bangs boy；<br><br>
 **_Note_** ：Keyword selection is based on literature review and platform common tags, with some data obtained via recommendation algorithms (e.g., homepage recommendations).<br><br>

## Child Inclusion Criteria
#### General Conditions
1. Age Range: 6 months-15 years. Accounts with early childhood images (e.g., 5-6 months) are included even if the current age exceeds the limit；<br>
2. Twin/Trplet Handling: Treat twins or triplets as one entity；<br>
3. Single-Platform Deduplication: For multiple accounts of the same child on one platform, only include the main account (most videos, highest quality)；<br>
4. Cross-Platform Deduplication: For multi-platform accounts of the same child, select the most complete-data platform account；<br>
5. Child Gender Labeling: Infer from multiple video content dimensions<br>
    * Observable Features: Child's hairstyle, clothing, voice characteristics (if voiced)；<br>
    * Contextual Information: Video title tags (e.g., "Boy's Rehabilitation Diary"), poster's descriptive text；<br>
    * for infants, also refer to caregiver's terms (e.g., "son","daughter").<br>

#### Autistic Children 
1. User profile or video content clearly states diagnosis (e.g., "diagnosed with autism", "ASD diagnosis certificate")；<br>
2. Profile explicitly states the child has autism, or account content includes medical diagnosis proof or ongoing rehabilitation records (text/video format); exclude accounts without clear diagnosis evidence.<br>

#### Typically-Developing Children
1. Account has no disease statement, and video content doesn't involve special medical or intervention training.<br><br>

## Child Video Selection Criteria
#### Quantity
1-3 videos per child (prioritizing high-quality segments).<br>

#### Duration
10 seconds-3 minutes. Can be longer considering platform characteristics.<br>

#### Exclusion Rules
1. Promotional/advertising videos (e.g., organizational promotion, fundraising)；<br>
2. Multi-person videos (autism group should avoid other children on camera)；<br>
3. Content with strong filters/beauty effects.<br>

#### Quality Requirements
1. Resolution ≥ 720p. Low-resolution videos (< 720p) must have clear facial images；<br>
2. Child's face unobstructed, close-up, neutral expression or small movements, for easy facial feature extractio；<br>
3. Early childhood (e.g., 6 months-3 years) videos preferred；<br>

 **_Note_** ：Some social platforms support photo-and-text format content besides videos. We include this in video selection, using the same criteria.<br><br>
 
## Facial Image Cropping Standards
#### Quantity
Only 1 optimal facial image per child.<br>
#### Technical Requirements
1. Full face (including ears), no shadows/obstructions；<br>
2. Facial yaw ≤ 40° (OpenFace tool's optimal recognition range)；<br>
3. Neutral expression preferred, avoid exaggerated actions (e.g., laughing, crying), maintain original facial structure.<br><br>

## Video Formats
Bilibili, Douyin, Quick Worker, Watermelon Video: MP4 format；<br>
Tencent Video: QLV forma；<br>
Youku Video: KUX format.<br><br>

## Dataset Features
#### 1. Autism Children
|                  | Number of children | Number of videos | Male | Female |
|------------------|--------------------|------------------|------|--------|
| Bilibili         | 18                 | 50               | 13   | 5      |
| Douyin           | 42                 | 124              | 29   | 13     |
| Quick Worker     | 45                 | 130              | 35   | 10     |
| Tencent Video    | 20                 | 20               | 16   | 4      |
| Watermelon Video | 54                 | 146              | 44   | 10     |
| Youku Video      | 3                  | 5                | 3    | 0      |
| All              | 182                | 475              | 140  | 42     |

#### 2. Typically-Developing Children
|                  | Number of children | Number of videos | Male | Female |
|------------------|--------------------|------------------|------|--------|
| Bilibili         | 1                  | 1                |      | 1      |
| Douyin           | 180                | 187              | 139  | 41     |
| Quick Worker     | 1                  | 1                | 1    |        |
| Tencent Video    |                    |                  |      |        |
| Watermelon Video |                    |                  |      |        |
| Youku Video      |                    |                  |      |        |
| All              | 182                | 189              | 140  | 42     |

## Data Privacy
 **Children's Video** ：Only video data links are provided.<br>
 **Facial Images** ：Only data after standard facial alignment and feature extraction using OpenFace 2.0 are provided.<br><br>

## Dataset Structure and Usage
#### Facial Image Naming Rule
Example：2-1-3-4<br>
First Digit: Platform Number (1 = Bilibili, 2 = Douyin, 3 = Quick Worker, 4 = Tencent Video, 5 = Watermelon Video, 6 = Youku Video, 7 = Rednote)；<br>
Second Digit: User Sequence Number within Platform；<br>
Third Digit Z: Video Sequence Number of the User；<br>
Fourth Digit W: Facial Image Sequence Number within the Video.<br>

#### Application Scenarios
Behavioral Analysis: Analyze autistic children's social interaction patterns by combining video timestamps.<br>
AI Model Training: Train classification models using facial features (e.g., AU action units) extracted by OpenFace.<br>
Cross-modal Research: Link facial features with voice and limb movement data.<br>

## Version and Citation
 **Version Number** ：V1.0 (2025-3-11)<br>
 **Citation Format** ：<br>
 **Dynamic Update** ：Set up a sustained data - collection mechanism. Monthly crawl for newly - added ASD/TD children's content that meets the criteria, and release incremental updates via version control (e.g., CSMACD - v1.0, v1.1).<br>

## Contact and Feedback
Maintenance Team: Xi Lab (Email: my.zhou1@siat.ac.cn).<br>
Issue Feedback: Submit via GitHub/Gitee repository or email.<br>
