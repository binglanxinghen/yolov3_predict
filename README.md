# yolov3_predict

该代码是部署的代码，可以任意拷贝到任何机器，只需要对应机器有安装git，git clone 这个仓库即可，运行代码需要额外的python包，需要pip install如下： 
先创建虚拟环境，安装Anaconda,输入./Anaconda3-5.2.0-Linux-x86_64.sh,接着source ~/.bashrc,然后conda create -n py3.6 python==3.6.  
1.opencv-python  
2.tensorflow==1.14.0    
3.pillow  ==6.2.1  
4.flask ==0.12.2   
5.flask_paginate ==0.5.3   
6.flask_sqlalchemy  
7.python-docx
8.easydict  ==1.9  
9.Werkzeug ==0.12.2  
其中如果涉及到动态库未安装，在例如libSM.so.6,centos机器可以yum whatprovides libSM.so.6，然后用yum install安装，例如yum install libSM-1.2.2-2.el7.x86_64 --setopt=protected_multilib=false，如果ubuntu系统，有类似动态库未安装，先apt-get update，然后提供一个命令，一键安装所有库，apt-get install -y libsm6 libxext6 libxrender-dev libglib2.0-0

本地代码改完如果需要上传到github上，需要检查一下第一条规则，不要把checkpoint里面的目录上次到github，因为模型太大了。
不熟悉git 命令需要去学，或者linux的vim编辑命令不熟，需要学习。  
简单介绍一下git的流程。git分为本地仓库，暂存仓，远程仓库。  
1.本地仓就是当前我们编辑代码的环境，当我们把git clone xxx 到某台电脑时候，那台电脑就是本地仓。  
2.当我们改完代码时候，可以使用git diff 或者git diff HEAD，皆可以显示刚才更改了那些地方。  
3.当我们本地全部代码编辑完，可以使用git add XXX，把文件提交到暂存仓(一键提交所有的改动是git add -A)，这时候如果add 错了文件，可以用git reset HEAD xxx把这个文件从暂存仓删除(也可以全部一键从暂存仓删除，git reset HEAD .，注意HEAD后面有个点)。  
4.提交到暂存仓后可以git status看一下刚才提交了哪些文件，检测一下时候提交了模型！！！，不要提交模型。  
5.使用git commit，是讲暂存仓库提交到本地仓，这时候会进入到vim模式让你编辑这次代码改动的log，比如这次做了一个新功能，那么这个信息记录到log里面，保存退出即可，:wq（vim的保存退出）。  
6.最后提交到远程仓库，git push -u origin master。  
8.把github账号密码一填即可。  

