## 1. 安装PaddlePaddle
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
【注意】版本号可参考[PaddlePaddle官网](https://pypi.org/project/paddlepaddle-gpu/#history)       

安装成功后，打开python命令行，使用以下代码进行测试：
```python
import paddle.fluid as fluid
fluid.install_check.run_check()
# 若出现Your Paddle Fluid is installed successfully!字样则表示安装成功
```
