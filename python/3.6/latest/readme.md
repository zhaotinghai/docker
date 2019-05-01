用法1：交互运行
```shell
docker rm -f python
docker run -it \
--name=python \
-v /usr/share/zoneinfo/Asia/Shanghai:/etc/localtime \
-v /data/notebook:/data/notebook \
--privileged=true \
-p 8888:8888 \
zhaotinghai/python \
jupyter notebook \
--no-browser \
--ip="*" \
--notebook-dir=/data/notebook/ \
--port=8888
```

用法2：常驻运行
```shell
docker rm -f python
docker run -d \
--name=python \
-v /usr/share/zoneinfo/Asia/Shanghai:/etc/localtime \
-v /data/notebook:/data/notebook \
--restart=always \
--privileged=true \
-p 8888:8888 \
zhaotinghai/python \
jupyter notebook \
--no-browser \
--ip="*" \
--notebook-dir=/data/notebook/ \
--port=8888
```

nbextensions 在网页上一般开启下面三个选项，代码提示，选择高亮，吧啦吧啦
Hinterland | Table Of Contens (2) | Highlight selected word

```shell

pip install pymongo apscheduler pystan fbprophet jupyter_contrib_nbextensions

# Hinterland | Table Of Contens (2) | Highlight selected word
jupyter contrib nbextension install --user

jupyter notebook --generate-config
# vi /root/.jupyter/jupyter_notebook_config.py
# c.NotebookApp.ip = '*'
# c.NotebookApp.allow_remote_access = True
# c.NotebookApp.allow_root = True
# sed -i "s/#c.NotebookApp.port = 8888/c.NotebookApp.port = 8888/g" /root/.jupyter/jupyter_notebook_config.py

# set jupyter notebook password
# jupyter notebook password



docker rm -f python
docker run -d \
-v /data:/data \
-v /usr/share/zoneinfo/Asia/Shanghai:/etc/localtime \
--name=python \
--restart=always \
--privileged=true \
--net=host \
zhaotinghai/python \
sleep 2100000000
docker exec -ti python bash




```

