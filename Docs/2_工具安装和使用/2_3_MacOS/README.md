## 1. Anaconda的安装与使用    
### 1.1 下载Anaconda     
在[官网](https://www.anaconda.com/distribution/)选择“MacOS”，并选择与所需python相对应的Anaconda版本进行下载

### 1.2 安装Anaconda 
步骤一：安装      
打开下载的安装包（以.pkl为后缀），根据引导完成安装，在安装过程中可以修改安装路径，具体如下图所示：
<div align=center><img width="600" height="400" src="./anaconda1.png"/></div>          
【注意】默认安装在MacOS当前用户主目录下     
步骤二：设置环境变量   
在命令行中执行下述命令

```cmd
# 将anaconda的bin目录加入PATH
# 根据安装路径的不同，修改”/Users/anaconda3/bin“
echo 'export PATH="/Users/anaconda3/bin:$PATH"' >> ~/.bash_profile
# 更新bash_profile以立即生效
source ~/.bash_profile
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
> MacOS 版本 = 10.11/10.12/10.13/10.14 (64 bit)     

【注意】目前MacOS环境仅支持CPU版PaddlePaddle

在命令行中执行下述命令
```cmd
# 进入创建好的Anaconda环境
source activate mypaddle
# （选择1）安装CPU版本PaddlePaddle
pip install -U paddlepaddle
# （选择2）安装指定版本PaddlePaddle
pip install -U paddlepaddle==[版本号]
```

安装成功后，打开python命令行，使用以下代码进行测试：
```python
import paddle.fluid as fluid
fluid.install_check.run_check()
# 若出现Your Paddle Fluid is installed successfully!字样则表示安装成功
```

## 3. 标注工具LabelMe的安装和使用
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
