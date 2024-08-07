# Teachers’ Classroom Dress Assessment Dataset (TCDADataset)

## About the dataset：
![image](https://github.com/aaauthors/TCDADataset/blob/main/TDAM/fig/TCDA.png)

Figure 1: An overview of the TCDA dataset. (a) shows the annotation information of the TCDA
dataset, (b) shows the viewpoint position of the camera in the classroom during the recording
process, and (c) shows examples of different perspectives.
The TCDA dataset contains how teachers dress in their daily classrooms，with a total of 11,879 image samples, covering different subjects, classrooms and diverse teaching environments. The details are shown in Figure 1.

  **As shown in Figure 1(a)**, we have defined a series of clothing attributes to capture the characteristics of teacher clothing more comprehensively. Positive attribute represents the clothing attribute that the teacher recommends in the daily classroom. Negative attribute represents the
clothing attribute that the teacher does not recommend in the daily classroom. Other attribute
represents the sample that does not participate in the teacher's dress assessment, and the absent
attribute represents the attribute that the character is missing. Finally, we conduct a comprehensive
evaluation of the teacher's attire based on the positive attributes and negative attributes to form the
final score. 

  In order to enhance the robustness of the dataset, we try to simulate the shooting angles in the
collected classroom teaching videos, i.e., directly behind the classroom, 45° behind the left of the
classroom, and 45° behind the right of the classroom,**as shown in Figure 1(b)**. Considering the
limitations of the scene, the teacher's body is often partially obscured by the lectern or the
teacher's interaction with the students, etc. Therefore, **as shown in Figure 1(c)**, we select the
teacher's viewpoint information from four directions, i.e., forward (F), backward (B), left (L), and
right (R).

## About the TDAM model：
### Requirement

Python >= 3.7

Pytorch >= 1.7.0
 
### Dataset Preparation

**1.TCDA dataset**
If the article is accepted for publication, we will upload the TCDA dataset. Then, prepare the dataset to have following structure:
TCDA
data/
dataset_all.pkl

**2.Training & Evaluation**

To train and evaluate the TDAM model on TCDA base on resnet50:

` python train.py --cfg ./config/pedes_baseline/TCDA.yaml `

If you use the TAQA dataset, please cite this paper:A Teacher Classroom Dress Assessment Method Based on a New Assessment Dataset
