## 1. 安装PaddlePaddle
环境依赖：
> python2 >= 2.7.15 或者 python3 >= 3.5.1 (64 bit)         
> pip >= 9.0.1 (64 bit)    
> Windows 版本 = 7/8/10企业版/10专业版 (64 bit)             
> 【注意】 如若您的机器有NVIDIA® GPU，对于CUDA和CUDNN的安装，可参考NVIDIA官方文档了解
> [CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/)和
> [CUDNN](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/)的安装流程和配置方法                
> 【注意】目前在Windows环境暂不支持NCCL，分布式等相关功能；默认提供的安装包需要计算机支持AVX指令集和MKL，如果您的环境不支持，请在[PaddlePaddle官网](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/beginners_guide/install/Tables.html/#ciwhls-release)下载openblas版本的安装包          
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
【注意】版本号可参考[PaddlePaddle官网](https://pypi.org/project/paddlepaddle-gpu/#history)       

安装成功后，打开python命令行，使用以下代码进行测试：
```python
import paddle.fluid as fluid
fluid.install_check.run_check()
# 若出现Your Paddle Fluid is installed successfully!字样则表示安装成功
```
