# cq-editor 虚拟环境搭建方法

问题：README 中提供的方法可以正确构建环境，但运行的时候提示
DLL load failed while import OCP
原因：猜测是 conda-forge/cadquery channel 上最新的 cadquery-merge 和 ocp7.5 的包存在问题, 没有经过测试

临时解决方案：不适用最新的 cadquery 和 ocp, 适用 cadquery2.1、ocp7.4 和 py3.8

```
# 克隆cq-editor代码
git clone https://github.com/CadQuery/CQ-editor.git
# conda env create -f cqgui_env.yml -n cqgui
# 创建虚拟环境(python3.8+ocp7.4+cadquery2.1)
conda env create -f cqgui_env_py38_ocp74_cq21.yml -n cqgui_py38_ocp74_cq21
# 激活环境
conda activate cqgui_py38_ocp74_cq21
# 运行cq-editor中的run.py
python run.py
```
