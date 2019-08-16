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