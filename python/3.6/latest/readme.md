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

