# Unity-RL-Playground-X2Ultra
Full-pipeline RL training and deployment for X2Ultra robot, powered by Unity-RL-Playground.

# setup
git clone https://github.com/loongOpen/Unity-RL-Playground.git, 

随后完成其主页安装仿真环境和训练环境安装流程，注意UnityEditor最好选择Unity2022.3.62f3，复制此链接下载https://unity.com/releases/editor/whats-new/2022.3.62f3

# X2Ultra

参考其sdk手册于https://x2-aimdk.agibot.com/en/latest/index.html

调试前关闭X2Ultra自带运控，ssh agi@10.0.1.40 password:1, aima em stop-app mc , x2Ultra会一直执行最后一次收到的command

注意，由于许可限制，本存储库中不包含 X2Ultra 的 URDF 和网格文件，假如你从工作人员那获取到URDF，将它按照Unity-RL-Playground导入，换掉Scene中名为"FakeX2Ultra"这个GameObject，在导入的机器人上装载相同脚本即可。

# 使用

Unity打开需要预先加载ROS环境

source /opt/ros/humble/setup.bash

export ROS_DOMAIN_ID=0

然后于该终端打开Unity
