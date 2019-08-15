## 1. Anaconda的安装与使用    

### 1.1 下载Anaconda         
Ubuntu图形界面下：在[官网](https://www.anaconda.com/distribution/)选择“Linux”，并选择与所需python相对应的Anaconda版本进行下载             
Ubuntu命令行界面下：使用”wget“进行下载
```cmd
# Anaconda2
wget https://repo.anaconda.com/archive/Anaconda2-2019.07-Linux-x86_64.sh --no-check-certificate
# Anaconda3
wget https://repo.anaconda.com/archive/Anaconda3-2019.07-Linux-x86_64.sh --no-check-certificate
```
### 1.2 安装Anaconda 

***步骤一：安装***       
在Anaconda安装包所在路径执行下述命令行
```cmd
# 运行所下载的Anaconda，例如：
bash ./Anaconda3-2019.07-Linux-x86_64.sh
```
【注意】安装过程中一直回车即可，直至出现设置路径时可对安装路径进行修改，否则默认安装在Ubuntu当前用户主目录下        
***步骤二：设置环境变量***     
在命令行中执行下述命令
```cmd
# 将anaconda的bin目录加入PATH
# 根据安装路径的不同，修改”~/anaconda3/bin“
echo 'export PATH="~/anaconda3/bin:$PATH"' >> ~/.bashrc
# 更新bashrc以立即生效
source ~/.bashrc
```
### 1.3 使用Anaconda         
在命令行中执行下述命令
```cmd
# 创建一个名为mypaddle的环境，指定python版本是3.5
conda create -n mypaddle python=3.5
# 创建好后，使用activate进入环境
source activate mypaddle
python --version
# 若上述命令行出现Anaconda字样，则表示安装成功
# 退出环境
source deactivate
```
## 2. 安装PaddlePaddle
环境依赖：
> python2 >= 2.7.15 或者 python3 >= 3.5.1 (64 bit)         
> pip >= 9.0.1 (64 bit)       
> Ubuntu 版本 (64 bit)    
> ├──Ubuntu 14.04 (GPU 版本支持 CUDA 8/10)         
> ├──Ubuntu 16.04 (GPU 版本支持 CUDA 8/9/10)         
> └──Ubuntu 18.04 (GPU 版本支持 CUDA 10)       
> 【注意】 如若您的机器有NVIDIA® GPU，对于CUDA和CUDNN的安装，可参考NVIDIA官方文档了解
> [CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/)和
> [CUDNN](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/)的安装流程和配置方法


在命令行中执行下述命令
```cmd
# 进入创建好的Anaconda环境
source activate mypaddle
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
source activate mypaddle
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
labelme
```
LabelMe标注工具界面主要如下图所示：       
<div align=center><img width="800" height="450" src="./labelme1.png"/></div>             
LabelMe默认标注多边形，可在图像中右键选择标注其他类型的框，如下图所示：          
<div align=center><img width="800" height="450" src="./labelme2.png"/></div>          
