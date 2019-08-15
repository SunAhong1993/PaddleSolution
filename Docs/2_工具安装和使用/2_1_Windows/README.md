## 1. Anaconda的安装与使用    
### 1.1 下载Anaconda     
在[官网](https://www.anaconda.com/distribution/)选择“Windows”，并选择与所需python相对应的Anaconda版本进行下载（PaddlePaddle要求安装的Anaconda版本为64-bit）

### 1.2 安装Anaconda 
打开下载的安装包（以.exe为后缀），根据引导完成安装，在安装过程中可以修改安装路径，具体如下图所示：
<div align=center><img width="580" height="400" src="./anaconda1.png"/></div>                  
【注意】默认安装在Windows当前用户主目录下           

### 1.3 使用Anaconda  

- 点击Windows系统左下角的Windows图标，打开：所有程序->Anaconda3/2（64-bit）->Anaconda Prompt      
- 在命令行中执行下述命令
```cmd
# 创建一个名为mypaddle的环境，指定python版本是3.5
conda create -n mypaddle python=3.5
# 创建好后，使用activate进入环境
conda activate mypaddle
python --version
# 若上述命令行出现Anaconda字样，则表示安装成功
# 退出环境
conda deactivate
```

## 2. 安装PaddlePaddle
环境依赖：
> python2 >= 2.7.15 或者 python3 >= 3.5.1 (64 bit)         
> pip >= 9.0.1 (64 bit)    
> Windows 版本 = 7/8/10企业版/10专业版 (64 bit)             
> 【注意】 如若您的机器有NVIDIA® GPU，对于CUDA和CUDNN的安装，可参考NVIDIA官方文档了解
> [CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/)和
> [CUDNN](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/)的安装流程和配置方法                
> 【注意】目前在Windows环境暂不支持NCCL，分布式等相关功能；默认提供的安装包需要计算机支持AVX指令集和MKL，如果您的环境不支持，请在[这里](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/beginners_guide/install/Tables.html/#ciwhls-release)下载openblas版本的安装包          
> 在命令行中执行下述命令
```cmd
# 进入创建好的Anaconda环境
conda activate mypaddle
# （选择1）安装CPU版本PaddlePaddle
pip install -U paddlepaddle
# （选择2）安装GPU版本PaddlePaddle
pip install -U paddlepaddle-gpu
# （选择3）安装指定版本PaddlePaddle
pip install -U paddlepaddle-gpu==[版本号]
pip install -U paddlepaddle==[版本号]
```
【注意】版本号可参考[这里](https://pypi.org/project/paddlepaddle-gpu/#history)       

安装成功后，打开python命令行，使用以下代码进行测试：
```python
import paddle.fluid as fluid
fluid.install_check.run_check()
# 若出现Your Paddle Fluid is installed successfully!字样则表示安装成功
```

## 3. 标注工具LabelMe的安装和使用
### 3.1 安装LabelMe
在命令行中执行下述命令
```cmd
# 进入创建好的Anaconda环境
conda activate mypaddle
# （选择一）python版本为2.x
conda install pyqt
# （选择二）python版本为3.x
pip install pyqt5
# 安装LabelMe
pip install labelme
```
### 3.2 使用LabelMe
在命令行中执行下述命令，则会出现标注工具
```cmd
# 进入创建好的Anaconda环境
source activate mypaddle
# 开启LabelMe
```
LabelMe标注工具界面主要如下图所示：       
<div align=center><img width="800" height="450" src="./labelme1.png"/></div>             
LabelMe默认标注多边形，可在图像中右键选择标注其他类型的框，如下图所示：          
<div align=center><img width="800" height="450" src="./labelme2.png"/></div>  
