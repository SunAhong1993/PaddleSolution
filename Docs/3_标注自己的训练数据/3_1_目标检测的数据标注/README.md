## 1. 使用LabelMe标注自己的数据

***步骤一 准备工作***   
- 对收集的图像划分为训练、验证（非必须）、测试三个部分的数据集，分别存放于对应的文件夹中      
- 创建与图像文件夹相对应的文件夹，用于存储标注的json文件
- 点击”Open Dir“按钮，选择需要标注的图像所在的文件夹打开，则”File List“对话框中会显示所有图像所对应的绝对路径      

***步骤二 标注***           
- 打开矩形框标注工具，具体如下图所示     
<div align=center><img width="800" height="450" src="./pics/detection1.png"/></div>   

- 使用拖拉的方式对目标物体进行标识，并在弹出的对话框中写明对应label（当label已存在时点击即可），具体如下图所示：

<div align=center><img width="800" height="450" src="./pics/detection2.gif"/></div>        

当框标注错误时，可点击右侧的“Edit Polygons”再点击标注框，通过拖拉进行修改，也可再点击“Delete Polygon”进行删除。

- 当所使用的模型是类似Mask R-CNN这类模型时，标注也需要语义分割信息；所以需要在标注过矩形框的基础上，点击右侧的“Create Polygons”以打点的方式圈出目标的轮廓，具体如下提所示：


- 点击右侧”Save“，将标注结果保存到步骤一中创建的文件夹中

