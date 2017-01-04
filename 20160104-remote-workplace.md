# 轻松用jupyter打造远程工作环境

很多时候我们需要在服务器(docker)上工作,我觉得python领域，jupyter是个很好的解决方案。

![](https://jupyter.readthedocs.io/en/latest/_static/_images/jupyter.svg)

# 安装jupyter

```
pip install jupyter
```

# 运行jupyter，在你的工作目录

```
jupyter notebook
```

# 桌面环境

在桌面环境，你现在已经打开一个浏览器，并加载了jupyter的编辑器，你可以开心的使用了。

![](https://jupyter.readthedocs.io/en/latest/_images/tryjupyter_file.png)

# 服务器环境

出于安全考虑，你最好使用ssh进行正向代理

```
#服务器环境不打开浏览器，指定端口
jupyter notebook --no-browser --port=8889
#ssh代理,访问本地的8888端口即访问远程主机的8889端口
ssh -N -f -L localhost:8888:localhost:8889 remote_user@remote_host
```

# 结语

现在可以开心的 编辑远程服务器上的文件了，也可以创建notebook进行交互编程。甚至有简单的shell可以交互执行命令。

