
docker run -ti --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix

docker run -d -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v /data:/data --net=host --privileged=true --name=tf14 tensorflow/tensorflow sleep 2100000000

curl -O cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css
//cdn.bootcss.com/require.js/2.3.3/require.min.js
Torch7 


docker run -d --name gpu -p 80:5000 -v /data/digits/data:/data --privileged=true --device /dev/nvidia-uvm:/dev/nvidia-uvm --device /dev/nvidia0:/dev/nvidia0 --device /dev/nvidiactl:/dev/nvidiactl nvidia/digits
docker run -d --name gpu1 -p 81:5000 -v /data/digits/data:/data --privileged=true nvidia/digits

nvidia-docker run --rm nvidia/cuda nvidia-smi

nvidia-docker run -d -v /data/digits/data:/data -v /data/digits/data/jobs:/jobs -p 80:5000 -p 6006:6006 nvidia/digits

nvidia-docker run -v /data:/data/ -p 5000:5000 nvidia/digits:latest

nvidia-docker run -d -v /data/digits/data:/data -v /data/digits/data/jobs:/jobs -p 80:5000 -p 6006:6006 nvidia/digits

nvidia-docker restart -v /data/digits/data:/data -p 80:5000 -p 6006:6006 nvidia/digits

nvidia-docker restart -v /data/digits/data:/data -p 80:5000 -p 6006:6006 nvidia/digits

export http_proxy="http://USERNAME:PASSWORD@<proxyserver>:<proxyport>"

export http_proxy="http://139.219.234.169:6666"
export https_proxy="http://139.219.234.169:6666"

{"success":true,"data":{"access_token":"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VybmFtZSI6ImFkbWluIiwiZXhwaXJlc19hdCI6MTUxMTM1NzA1ODAyM30.bBMfbhWqmy-J-jFObTc0yevdY5ETdRew_80Fv9Jqz7E","expires_in":7200}}


docker run -d -v /data/dataset:/data/dataset --net host --name nfs --privileged cpuguy83/nfs-server /data/dataset
docker run -d -v /data/dataset:/data/dataset -p 111:111/udp -p 2049:2049/tcp --name nfs --privileged cpuguy83/nfs-server /data/dataset

docker run -d -v /data/nfs:/data/nfs --name nfs-client --privileged --link nfs:nfs cpuguy83/nfs-client /data/nfs:/data/nfs


mkdir /tmp/model-data
curl -o '/tmp/model-data/inception-v3-2016-03-01.tar.gz' 'http://download.tensorflow.org/models/image/imagenet/inception-v3-2016-03-01.tar.gz'
cd /tmp/model-data
tar xzf inception-v3-2016-03-01.tar.gz


docker network create app-tier --driver bridge


docker run -d --name tensorflow-serving \
    --volume /tmp/model-data:/bitnami/model-data \
    --network app-tier \
    bitnami/tensorflow-serving:latest

docker run -d --name tensorflow-serving \
    --volume /tmp/model-data:/bitnami/model-data \
    -p 9000:9000 \
    bitnami/tensorflow-serving:latest


docker run -d --name tensorflow-serving \
    --volume /tmp/model-data:/bitnami/model-data \
    --network host \
    --privileged \
    bitnami/tensorflow-serving:latest

docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --network app-tier \
    bitnami/tensorflow-inception:latest inception_client --server=tensorflow-serving:9000 --image=/bitnami/model-data/00611.jpg


iptables -t nat -A PREROUTING -p tcp -d 172.28.9.212 --dport 27017 -j DNAT --to-destination 172.28.9.214:27017

docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --network app-tier \
    bitnami/tensorflow-inception:latest inception_client --server=tensorflow-serving:9000 --image=/bitnami/model-data/00611.jpg

docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --network host \
    --privileged \
    bitnami/tensorflow-inception:latest inception_client --server=172.28.9.212:9000 --image=/bitnami/model-data/00611.jpg

docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --network host \
    --privileged \
    bitnami/tensorflow-inception:latest inception_client --server=127.0.0.1:9000 --image=/bitnami/model-data/00611.jpg




docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --link tensorflow-serving:tfs \
    bitnami/tensorflow-inception:latest inception_client --server=tfs:9000 --image=path/to/image.jpg

docker run -it --rm \
    --volume /tmp/model-data:/bitnami/model-data \
    --link tensorflow-serving:tfs \
    bitnami/tensorflow-inception:latest inception_client --server=172.28.9.210:9000 --image=/bitnami/model-data/00611.jpg



docker run -d -v /data/nfs:/data/nfs --name nfs --net host --privileged cpuguy83/nfs-server /data/nfs




cdn.bootcss.com/async/2.0.1/async.min
'sprintf' : '//cdn.bootcss.com/sprintf/1.0.3/sprintf.min',
'require/css'  : '//cdn.bootcss.com/require-css/0.1.10/css.min',
'require/text' : '//cdn.bootcss.com/require-text/2.0.12/text.min',
'require/json' : '//cdn.bootcss.com/requirejs-plugins/1.0.3/json.min',
'jquery': '//cdn.bootcss.com/jquery/1.12.4/jquery.min',
'jquery-cookie': '//cdn.bootcss.com/jquery-cookie/1.4.1/jquery.cookie.min',
'jquery.twbsPagination': '//cdn.bootcss.com/twbs-pagination/1.3.1/jquery.twbsPagination.min',
'jquery-confirm': '//cdn.bootcss.com/jquery-confirm/3.2.3/jquery-confirm.min',
'echarts2' : '//cdn.bootcss.com/echarts/2.2.7/echarts-all',
'echarts3' : '//cdn.bootcss.com/echarts/3.2.2/echarts.min',
'echarts3map' : '//echarts.baidu.com/asset/map/js/china',
'angular'           : '//cdn.bootcss.com/angular.js/1.5.7/angular',
'angular-cookies'   : '//cdn.bootcss.com/angular.js/1.5.7/angular-cookies.min',
'angular-messages'  : '//cdn.bootcss.com/angular-messages/1.5.7/angular-messages',
'angular-ui-router' : '//cdn.bootcss.com/angular-ui-router/1.0.3/angular-ui-router.min',
'angularAMD'        : '//cdn.jsdelivr.net/angular.amd/0.2/angularAMD.min',
'bootstrap'     : '//cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min',
'bootstrap-css' : '//cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min',
'bootstrap-table' : '//cdn.bootcss.com/bootstrap-table/1.11.1/bootstrap-table.min',
'bootstrap-table-reorder-columns' : '//cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/bootstrap-table-reorder-columns.min',
'bootstrap-table-locale' : '//cdn.bootcss.com/bootstrap-table/1.11.1/locale/bootstrap-table-zh-CN.min',
'bootstrap-table-filter-control' : '//cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/bootstrap-table-filter-control.min',

'bootstrap-fileinput'     : '//cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/fileinput.min',
'bootstrap-fileinput-zh'  : '//cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/fileinput_locale_zh.min',
'bootstrap-fileinput-css' : '//cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/fileinput.min',
'font-awesome' : '//cdn.bootcss.com/font-awesome/4.6.3/css/font-awesome.min',
'ztree'     : '//cdn.bootcss.com/zTree.v3/3.5.26/js/jquery.ztree.all.min',
'ztree-css' : '//cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/zTreeStyle.min',
'daterangepicker' :'//cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min',
'daterangepicker-css' : '//cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min',
'moment' : '//cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/moment.min',


mkdir -p /data/cdn/cdn.bootcss.com/async/2.0.1/ && cd /data/cdn/cdn.bootcss.com/async/2.0.1/ && curl -O http://cdn.bootcss.com/async/2.0.1/async.min
mkdir -p /data/cdn/cdn.bootcss.com/async/2.0.1/ && cd /data/cdn/cdn.bootcss.com/async/2.0.1/ && curl -O http://cdn.bootcss.com/async/2.0.1/async.min.js
mkdir -p /data/cdn/cdn.bootcss.com/async/2.0.1/ && cd /data/cdn/cdn.bootcss.com/async/2.0.1/ && curl -O http://cdn.bootcss.com/async/2.0.1/async.min.css
mkdir -p /data/cdn/cdn.bootcss.com/async/2.0.1/ && cd /data/cdn/cdn.bootcss.com/async/2.0.1/ && curl -O http://cdn.bootcss.com/async/2.0.1/async.min.less
mkdir -p /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && cd /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && curl -O http://cdn.bootcss.com/sprintf/1.0.3/sprintf.min
mkdir -p /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && cd /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && curl -O http://cdn.bootcss.com/sprintf/1.0.3/sprintf.min.js
mkdir -p /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && cd /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && curl -O http://cdn.bootcss.com/sprintf/1.0.3/sprintf.min.css
mkdir -p /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && cd /data/cdn/cdn.bootcss.com/sprintf/1.0.3/ && curl -O http://cdn.bootcss.com/sprintf/1.0.3/sprintf.min.less
mkdir -p /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && cd /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && curl -O http://cdn.bootcss.com/require-css/0.1.10/css.min
mkdir -p /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && cd /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && curl -O http://cdn.bootcss.com/require-css/0.1.10/css.min.js
mkdir -p /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && cd /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && curl -O http://cdn.bootcss.com/require-css/0.1.10/css.min.css
mkdir -p /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && cd /data/cdn/cdn.bootcss.com/require-css/0.1.10/ && curl -O http://cdn.bootcss.com/require-css/0.1.10/css.min.less
mkdir -p /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && cd /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && curl -O http://cdn.bootcss.com/require-text/2.0.12/text.min
mkdir -p /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && cd /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && curl -O http://cdn.bootcss.com/require-text/2.0.12/text.min.js
mkdir -p /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && cd /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && curl -O http://cdn.bootcss.com/require-text/2.0.12/text.min.css
mkdir -p /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && cd /data/cdn/cdn.bootcss.com/require-text/2.0.12/ && curl -O http://cdn.bootcss.com/require-text/2.0.12/text.min.less
mkdir -p /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && cd /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && curl -O http://cdn.bootcss.com/requirejs-plugins/1.0.3/json.min
mkdir -p /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && cd /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && curl -O http://cdn.bootcss.com/requirejs-plugins/1.0.3/json.min.js
mkdir -p /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && cd /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && curl -O http://cdn.bootcss.com/requirejs-plugins/1.0.3/json.min.css
mkdir -p /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && cd /data/cdn/cdn.bootcss.com/requirejs-plugins/1.0.3/ && curl -O http://cdn.bootcss.com/requirejs-plugins/1.0.3/json.min.less
mkdir -p /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && cd /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && curl -O http://cdn.bootcss.com/jquery/1.12.4/jquery.min
mkdir -p /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && cd /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && curl -O http://cdn.bootcss.com/jquery/1.12.4/jquery.min.js
mkdir -p /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && cd /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && curl -O http://cdn.bootcss.com/jquery/1.12.4/jquery.min.css
mkdir -p /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && cd /data/cdn/cdn.bootcss.com/jquery/1.12.4/ && curl -O http://cdn.bootcss.com/jquery/1.12.4/jquery.min.less
mkdir -p /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && cd /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && curl -O http://cdn.bootcss.com/jquery-cookie/1.4.1/jquery.cookie.min
mkdir -p /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && cd /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && curl -O http://cdn.bootcss.com/jquery-cookie/1.4.1/jquery.cookie.min.js
mkdir -p /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && cd /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && curl -O http://cdn.bootcss.com/jquery-cookie/1.4.1/jquery.cookie.min.css
mkdir -p /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && cd /data/cdn/cdn.bootcss.com/jquery-cookie/1.4.1/ && curl -O http://cdn.bootcss.com/jquery-cookie/1.4.1/jquery.cookie.min.less
mkdir -p /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && cd /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && curl -O http://cdn.bootcss.com/twbs-pagination/1.3.1/jquery.twbsPagination.min
mkdir -p /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && cd /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && curl -O http://cdn.bootcss.com/twbs-pagination/1.3.1/jquery.twbsPagination.min.js
mkdir -p /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && cd /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && curl -O http://cdn.bootcss.com/twbs-pagination/1.3.1/jquery.twbsPagination.min.css
mkdir -p /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && cd /data/cdn/cdn.bootcss.com/twbs-pagination/1.3.1/ && curl -O http://cdn.bootcss.com/twbs-pagination/1.3.1/jquery.twbsPagination.min.less
mkdir -p /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && cd /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && curl -O http://cdn.bootcss.com/jquery-confirm/3.2.3/jquery-confirm.min
mkdir -p /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && cd /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && curl -O http://cdn.bootcss.com/jquery-confirm/3.2.3/jquery-confirm.min.js
mkdir -p /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && cd /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && curl -O http://cdn.bootcss.com/jquery-confirm/3.2.3/jquery-confirm.min.css
mkdir -p /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && cd /data/cdn/cdn.bootcss.com/jquery-confirm/3.2.3/ && curl -O http://cdn.bootcss.com/jquery-confirm/3.2.3/jquery-confirm.min.less
mkdir -p /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && cd /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && curl -O http://cdn.bootcss.com/echarts/2.2.7/echarts-all
mkdir -p /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && cd /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && curl -O http://cdn.bootcss.com/echarts/2.2.7/echarts-all.js
mkdir -p /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && cd /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && curl -O http://cdn.bootcss.com/echarts/2.2.7/echarts-all.css
mkdir -p /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && cd /data/cdn/cdn.bootcss.com/echarts/2.2.7/ && curl -O http://cdn.bootcss.com/echarts/2.2.7/echarts-all.less
mkdir -p /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && cd /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && curl -O http://cdn.bootcss.com/echarts/3.2.2/echarts.min
mkdir -p /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && cd /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && curl -O http://cdn.bootcss.com/echarts/3.2.2/echarts.min.js
mkdir -p /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && cd /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && curl -O http://cdn.bootcss.com/echarts/3.2.2/echarts.min.css
mkdir -p /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && cd /data/cdn/cdn.bootcss.com/echarts/3.2.2/ && curl -O http://cdn.bootcss.com/echarts/3.2.2/echarts.min.less
mkdir -p /data/cdn/echarts.baidu.com/asset/map/js/ && cd /data/cdn/echarts.baidu.com/asset/map/js/ && curl -O http://echarts.baidu.com/asset/map/js/china
mkdir -p /data/cdn/echarts.baidu.com/asset/map/js/ && cd /data/cdn/echarts.baidu.com/asset/map/js/ && curl -O http://echarts.baidu.com/asset/map/js/china.js
mkdir -p /data/cdn/echarts.baidu.com/asset/map/js/ && cd /data/cdn/echarts.baidu.com/asset/map/js/ && curl -O http://echarts.baidu.com/asset/map/js/china.css
mkdir -p /data/cdn/echarts.baidu.com/asset/map/js/ && cd /data/cdn/echarts.baidu.com/asset/map/js/ && curl -O http://echarts.baidu.com/asset/map/js/china.less
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular.js
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular.css
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular.less
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular-cookies.min
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular-cookies.min.js
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular-cookies.min.css
mkdir -p /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular.js/1.5.7/ && curl -O http://cdn.bootcss.com/angular.js/1.5.7/angular-cookies.min.less
mkdir -p /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && curl -O http://cdn.bootcss.com/angular-messages/1.5.7/angular-messages
mkdir -p /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && curl -O http://cdn.bootcss.com/angular-messages/1.5.7/angular-messages.js
mkdir -p /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && curl -O http://cdn.bootcss.com/angular-messages/1.5.7/angular-messages.css
mkdir -p /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && cd /data/cdn/cdn.bootcss.com/angular-messages/1.5.7/ && curl -O http://cdn.bootcss.com/angular-messages/1.5.7/angular-messages.less
mkdir -p /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && cd /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && curl -O http://cdn.bootcss.com/angular-ui-router/1.0.3/angular-ui-router.min
mkdir -p /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && cd /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && curl -O http://cdn.bootcss.com/angular-ui-router/1.0.3/angular-ui-router.min.js
mkdir -p /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && cd /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && curl -O http://cdn.bootcss.com/angular-ui-router/1.0.3/angular-ui-router.min.css
mkdir -p /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && cd /data/cdn/cdn.bootcss.com/angular-ui-router/1.0.3/ && curl -O http://cdn.bootcss.com/angular-ui-router/1.0.3/angular-ui-router.min.less
mkdir -p /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && cd /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && curl -O http://cdn.jsdelivr.net/angular.amd/0.2/angularAMD.min
mkdir -p /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && cd /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && curl -O http://cdn.jsdelivr.net/angular.amd/0.2/angularAMD.min.js
mkdir -p /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && cd /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && curl -O http://cdn.jsdelivr.net/angular.amd/0.2/angularAMD.min.css
mkdir -p /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && cd /data/cdn/cdn.jsdelivr.net/angular.amd/0.2/ && curl -O http://cdn.jsdelivr.net/angular.amd/0.2/angularAMD.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/js/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/js/bootstrap.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/css/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/css/bootstrap.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/bootstrap-table.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/bootstrap-table.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/bootstrap-table.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/bootstrap-table.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/bootstrap-table-reorder-columns.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/bootstrap-table-reorder-columns.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/bootstrap-table-reorder-columns.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/reorder-columns/bootstrap-table-reorder-columns.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/locale/bootstrap-table-zh-CN.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/locale/bootstrap-table-zh-CN.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/locale/bootstrap-table-zh-CN.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/locale/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/locale/bootstrap-table-zh-CN.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/bootstrap-table-filter-control.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/bootstrap-table-filter-control.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/bootstrap-table-filter-control.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && cd /data/cdn/cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/ && curl -O http://cdn.bootcss.com/bootstrap-table/1.11.1/extensions/filter-control/bootstrap-table-filter-control.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/fileinput.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/fileinput.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/fileinput.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/js/fileinput.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/fileinput_locale_zh.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/fileinput_locale_zh.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/fileinput_locale_zh.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.3.1/js/fileinput_locale_zh.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/fileinput.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/fileinput.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/fileinput.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && cd /data/cdn/cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/ && curl -O http://cdn.bootcss.com/bootstrap-fileinput/4.4.1/css/fileinput.min.less
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/css/font-awesome.min
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/css/font-awesome.min.js
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/css/font-awesome.min.css
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/css/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/css/font-awesome.min.less
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/js/jquery.ztree.all.min
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/js/jquery.ztree.all.min.js
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/js/jquery.ztree.all.min.css
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/js/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/js/jquery.ztree.all.min.less
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/zTreeStyle.min
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/zTreeStyle.min.js
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/zTreeStyle.min.css
mkdir -p /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && cd /data/cdn/cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/ && curl -O http://cdn.bootcss.com/zTree.v3/3.5.26/css/zTreeStyle/zTreeStyle.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/daterangepicker.min.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/moment.min
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/moment.min.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/moment.min.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && cd /data/cdn/cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/ && curl -O http://cdn.bootcss.com/bootstrap-daterangepicker/2.1.25/moment.min.less
mkdir -p /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && cd /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && curl -O http://cdn.bootcss.com/require.js/2.3.3/require.min
mkdir -p /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && cd /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && curl -O http://cdn.bootcss.com/require.js/2.3.3/require.min.js
mkdir -p /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && cd /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && curl -O http://cdn.bootcss.com/require.js/2.3.3/require.min.css
mkdir -p /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && cd /data/cdn/cdn.bootcss.com/require.js/2.3.3/ && curl -O http://cdn.bootcss.com/require.js/2.3.3/require.min.less
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff2
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff2.js
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff2.css
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff2.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff2
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff2.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff2.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff2.less
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff.js
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff.css
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.woff.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.woff.less
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.ttf
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.ttf.js
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.ttf.css
mkdir -p /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && cd /data/cdn/cdn.bootcss.com/font-awesome/4.6.3/fonts/ && curl -O http://cdn.bootcss.com/font-awesome/4.6.3/fonts/fontawesome-webfont.ttf.less
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.ttf
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.ttf.js
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.ttf.css
mkdir -p /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && cd /data/cdn/cdn.bootcss.com/bootstrap/3.3.5/fonts/ && curl -O http://cdn.bootcss.com/bootstrap/3.3.5/fonts/glyphicons-halflings-regular.ttf.less


博客
学院
下载
更多

写博客
发布Chat

文件系统vs对象存储——选型和趋势
转载 2016年04月22日 13:50:18 标签：文件系统 1131
摘要：对象存储和我们经常接触到的硬盘和文件系统等存储形态不同，它提供Key-Value（简称K/V）方式的RESTful数据读写接口，并且常以网络服务的形式提供数据的访问。但经过多年的发展，我们现在通常认为AWS S3或者Swift才是对象存储。
作者：李明宇    来源：-    2015-08-11
关键词：对象存储    Ceph    Swift    OpenStack    
 
如果我们在服务端存储文件，例如一个O2O应用中的图片或者企业级云盘里的文档，以前我们可能会毫不犹豫地把它们放到文件系统里，比如说NAS或者一个分布式文件系统里，但是，随着技术的发展，我们有了一个新的选择——对象存储，今天我们来讨论一下，对象存储相对于文件系统有什么特点？什么时候我们应该选择对象存储？文件系统将来的发展方向是什么？

一、对象存储的概念

对象存储和我们经常接触到的硬盘和文件系统等存储形态不同，它提供Key-Value（简称K/V）方式的RESTful数据读写接口，并且常以网络服务的形式提供数据的访问。

在早些年，特别是2006年以前，人们提到对象存储，往往指的是以类似标准化组织SNIA定义的OSD（object storage device）和MDS（Metadata Server）为基本组成部分的分布式存储，通常是分布式文件系统。我们经常听到的分布式存储Ceph的底层RADOS（Reliable Autonomous Distributed Object Store），即属于这类对象存储。



（图片部分内容引用自Ceph官网和SwiftStack官网）

而2006年以后，人们说到对象存储，往往指的是以AWS的S3为代表的，通过HTTP接口提供访问的存储服务或者存储系统。类似的系统还有Rackspace于2009年开始研发并于2010年开源的OpenStack Swift（Rackspace的对象存储服务开始于2008年，但是Swift项目的开发是从2009年开始的，Rackspace用Swift项目对其云存储系统进行了彻底重构）。这里的“对象”（Object）和我们平时说的文件类似，如果我们把一个文件传到对象存储系统里面存起来，就叫做一个对象。



（图片部分内容引用自Ceph官网和SwiftStack）

从另一个角度来说，2006年以前常说的对象存储，指的是一种存储系统的架构；而2006年以后，人们说到对象存储常指的是一种存储形态，我们这里讨论的对象存储也正是后者。

目前，对象存储已经得到了广泛的应用。具有代表性的大规模实现主要在各个公有云服务商，比如AWS的S3、Rackspace的CloudFiles，国内的七牛云存储、阿里云的开放存储服务OSS也属于对象存储，最近，青云也发布了对象存储服务。

对象存储也有一些著名的开源实现，如OpenStack Swift，开源的统一存储系统Ceph也可以通过Ceph Object Gateway提供对象存储服务，也称作RADOS Gateway，缩写为RADOSGW。

二、对象存储与文件系统的比较

与文件系统相比，以AWS S3和Swift为代表的对象存储有两个显著的特征——REST风格的接口和扁平的数据组织结构。

1.对象存储的接口

对于大多数文件系统来说，尤其是POSIX兼容的文件系统，提供open、close、read、write和lseek等接口。

而对象存储的接口是REST风格的，通常是基于HTTP协议的RESTful Web API，通过HTTP请求中的PUT和GET等操作进行文件的上传即写入和下载即读取，通过DELETE操作删除文件。



（图片内容来自SwiftStack）

对象存储和文件系统在接口上的本质区别是对象存储不支持和fread和fwrite类似的随机位置读写操作，即一个文件PUT到对象存储里以后，如果要读取，只能GET整个文件，如果要修改一个对象，只能重新PUT一个新的到对象存储里，覆盖之前的对象或者形成一个新的版本。

如果结合平时使用云盘的经验，就不难理解这个特点了，用户会上传文件到云盘或者从云盘下载文件。如果要修改一个文件，会把文件下载下来，修改以后重新上传，替换之前的版本。实际上几乎所有的互联网应用，都是用这种存储方式读写数据的，比如微信，在朋友圈里发照片是上传图像、收取别人发的照片是下载图像，也可以从朋友圈中删除以前发送的内容；微博也是如此，通过微博API我们可以了解到，微博客户端的每一张图片都是通过REST风格的HTTP请求从服务端获取的，而我们要发微博的话，也是通过HTTP请求将数据包括图片传上去的。在没有对象存储以前，开发者需要自己为客户端提供HTTP的数据读写接口，并通过程序代码转换为对文件系统的读写操作。

能够放弃随机读写接口而采用REST接口的一个重要原因是计算机系统本身的演进呼唤存储系统的变革，目前的计算机的内存大小已经和当初设计POSIX文件系统接口时大不一样了。文件系统诞生于1960年代，当时的内存是以KB为单位的，内存资源非常宝贵，同时外存的数据读写速率也非常低，所以把文件中的一小部分数据加载进内存进行操作显得非常有必要。而如今，计算机的内存是以GB为单位的，往往在几十、几百GB量级，而常常需要存取的文件——如图片、文档等，则是在MB级别，GB以上的文件数量非常少（多为长视频、归档文件、虚拟机镜像等，这一类数据我们会在本系列的后面几篇中进行讨论），外存和网络的吞吐率较之1960年代，也有了数千倍的提升，把一个文件完全加载到内存中进行处理和可视化的已经开销微不足道了，而带来的计算效率和用户体验的提升却是显著的。

2. 扁平的数据组织结构

对比文件系统，对象存储的第二个特点是没有嵌套的文件夹，而是采用扁平的数据组织结构，往往是两层或者三层，例如AWS S3和华为的UDS，每个用户可以把它的存储空间划分为“容器”（Bucket），然后往每个容器里放对象，对象不能直接放到租户的根存储空间里，必须放到某个容器下面，而不能嵌套，也就是说，容器下面不能再放一层容器，只能放对象。OpenStack Swift也类似

这就是所谓“扁平数据组织结构”，因为它和文件夹可以一级一级嵌套不同，层次关系是固定的，而且只有两到三级，是扁平的。每一级的每个元素，例如S3中的某个容器或者某个对象，在系统中都有唯一的标识，用户通过这个标识来访问容器或者对象，所以，对象存储提供的是一种K/V的访问方式。



（图片内容来自华为）

采用扁平的数据组织结构抛弃了嵌套的文件夹，避免维护庞大的目录树。随着大数据和互联网的发展，如今的存储系统中，动辄数百万、千万甚至上亿个文件/对象，单位时间内的访问次数和并发访问量也达到了前所未有的量级，在这种情况下，目录树会给存储系统带来很大的开销和诸多问题，成为系统的瓶颈。反观目录结构的初衷——数据管理，如今作用非常有限，我们已经很难通过目录的划分对文件进行归类和管理了，因为一个文件最终只能放到一个文件夹下，作为目录树的叶子节点存在，而文件的属性是多维度的。目前各类应用中广泛采用元数据检索的方式进行数据的管理，通过对元数据的匹配得到一个Index或者Key，再根据这个Index或者Key找到并读取数据，所以，对象存储的扁平数据组织形式和K/V访问方式更能满足数据管理的需求。

不难看出，对象存储有着鲜明的互联网和大数据时代的特点，随着“互联网+”的推进，互联网技术正在渗透到各行各业，数据量也在成指数倍数增长，对象存储将发挥越来越大的作用。

三、文件系统和对象存储系统的优劣和发展趋势分析

上述分析了对象存储的特点并与文件系统做了比较，接下来就不得不回答一个问题：文件系统是不是没有生命力了？答案当然是否定的。对象存储打破了文件系统一统天下的局面，给我们带来了更多的选择，并不意味着我们就要否定文件系统。

而对于一些场景，比如虚拟机活动镜像的存储，或者说虚拟机硬盘文件的存储，还有大数据处理等场景，对象存储就显得捉襟见肘了。而文件系统在这些领域有突出的表现，比如Nutanix的NDFS（Nutanix Distributed Filesystem）和VMware的VMFS（VMware Filesystem）在虚拟机镜像存储方面表现很出色，Google文件系统GFS及其开源实现HDFS被广泛用于支撑基于MapReduce模型的大数据处理支持得很好，而且能够很好地支持百GB级、TB级甚至更大文件的存储。

由此看来文件系统将来的发展趋势更多的是专用文件系统，而不再是以前一套Filesystem一统天下的做法，更有一些部分要让位于对象存储或者其他存储形态。

从另一个角度来看，现代对象存储系统的“甜区”在哪里：1. 互联网和类似互联网的应用场景，这不仅仅是因为REST风格的HTTP的接口，而且还因为大多数对象存储系统在设计上能够非常方便地进行横向扩展以适应大量用户高并发访问的场景；2. 海量十KB级到GB级对象/文件的存储，小于10KB的数据更适用于使用K/V数据库，而大于10GB的文件最好将其分割为多个对象并行写入对象存储系统中，多数对象存储系统都有单个对象大小上限的限制。所以，如果应用具有上述两种特点，对象存储是首选。

也有人在对象存储上做出进一步的开发或者改进，使其能够很好地支持归档备份、MapReduce大数据处理等场景，甚至将对象存储的接口转为文件系统接口；反之，OpenStack Swift等对象存储系统也支持使用GlusterFS等通用文件系统作为存储后端。人们为什么会在这些对象存储和文件系统相互转换的技术上进行人力和资金的投入？这些做法的意义何在？应该在什么时候使用这些技术？我们将在本系列的后续章节中给出答案。

本系列还将以OpenStack Swift为例来剖析对象存储的设计与实现，并且讨论对象存储在实际应用中所遇到的问题以及在Swift中是如何解决的，进而讨论对象存储的发展对底层硬件带来的挑战和机遇。另外，由于对象存储和传统存储形态的差别，性能评估已经不能以IOPS和读写速率等传统指标来衡量，应当如何对对象存储进行评估？我们也将在后续章节中进行探讨。


OpenStack Swift 开源项目提供了弹性可伸缩、高可用的分布式对象存储服务，适合存储大规模非结构化数据。本文将深入介绍 Swift 的基本设计原理、对称式的系统架构和 RESTful API。
6 评论
张 华, Advisory Software Engineer, IBM
2013 年 10 月 24 日
expand
内容

在 IBM Bluemix 云平台上开发并部署您的下一个应用。
开始您的试用
OpenStack Swift 原理、架构与 API 介绍
回页首
背景与概览
Swift 最初是由 Rackspace 公司开发的高可用分布式对象存储服务，并于 2010 年贡献给 OpenStack 开源社区作为其最初的核心子项目之一，为其 Nova 子项目提供虚机镜像存储服务。Swift 构筑在比较便宜的标准硬件存储基础设施之上，无需采用 RAID（磁盘冗余阵列），通过在软件层面引入一致性散列技术和数据冗余性，牺牲一定程度的数据一致性来达到高可用性和可伸缩性，支持多租户模式、容器和对象读写操作，适合解决互联网的应用场景下非结构化数据存储问题。
此项目是基于 Python 开发的，采用 Apache 2.0 许可协议，可用来开发商用系统。
回页首
基本原理
一致性散列（Consistent Hashing)
面对海量级别的对象，需要存放在成千上万台服务器和硬盘设备上，首先要解决寻址问题，即如何将对象分布到这些设备地址上。Swift 是基于一致性散列技术，通过计算可将对象均匀分布到虚拟空间的虚拟节点上，在增加或删除节点时可大大减少需移动的数据量；虚拟空间大小通常采用 2 的 n 次幂，便于进行高效的移位操作；然后通过独特的数据结构 Ring（环）再将虚拟节点映射到实际的物理存储设备上，完成寻址过程。
图 1. 一致性散列
一致性散列
如图 1 中所示，以逆时针方向递增的散列空间有 4 个字节长共 32 位，整数范围是[0~232-1]；将散列结果右移 m 位，可产生 232-m个虚拟节点，例如 m=29 时可产生 8 个虚拟节点。在实际部署的时候需要经过仔细计算得到合适的虚拟节点数，以达到存储空间和工作负载之间的平衡。
数据一致性模型（Consistency Model）
按照 Eric Brewer 的 CAP（Consistency，Availability，Partition Tolerance）理论，无法同时满足 3 个方面，Swift 放弃严格一致性（满足 ACID 事务级别），而采用最终一致性模型（Eventual Consistency），来达到高可用性和无限水平扩展能力。为了实现这一目标，Swift 采用 Quorum 仲裁协议(Quorum 有法定投票人数的含义)：
（1）定义：N：数据的副本总数；W：写操作被确认接受的副本数量；R：读操作的副本数量
（2）强一致性：R+W>N，以保证对副本的读写操作会产生交集，从而保证可以读取到最新版本；如果 W=N，R=1，则需要全部更新，适合大量读少量写操作场景下的强一致性；如果 R=N，W=1，则只更新一个副本，通过读取全部副本来得到最新版本，适合大量写少量读场景下的强一致性。
（3）弱一致性：R+W<=N，如果读写操作的副本集合不产生交集，就可能会读到脏数据；适合对一致性要求比较低的场景。
Swift 针对的是读写都比较频繁的场景，所以采用了比较折中的策略，即写操作需要满足至少一半以上成功 W >N/2，再保证读操作与写操作的副本集合至少产生一个交集，即 R+W>N。Swift 默认配置是 N=3，W=2>N/2，R=1 或 2，即每个对象会存在 3 个副本，这些副本会尽量被存储在不同区域的节点上；W=2 表示至少需要更新 2 个副本才算写成功；当 R=1 时意味着某一个读操作成功便立刻返回，此种情况下可能会读取到旧版本（弱一致性模型）；当 R=2 时，需要通过在读操作请求头中增加 x-newest=true 参数来同时读取 2 个副本的元数据信息，然后比较时间戳来确定哪个是最新版本（强一致性模型）；如果数据出现了不一致，后台服务进程会在一定时间窗口内通过检测和复制协议来完成数据同步，从而保证达到最终一致性。如图 2 所示：
图 2. Quorum 协议示例
Quorum 协议示例
环的数据结构
环是为了将虚拟节点（分区）映射到一组物理存储设备上，并提供一定的冗余度而设计的，其数据结构由以下信息组成：
存储设备列表、设备信息包括唯一标识号（id）、区域号（zone）、权重（weight）、IP 地址（ip）、端口（port）、设备名称（device）、元数据（meta）。
分区到设备映射关系（replica2part2dev_id 数组)
计算分区号的位移(part_shift 整数，即图 1 中的 m)
以查找一个对象的计算过程为例：
图 3. 环的数据机构
环的数据机构
使用对象的层次结构 account/container/object 作为键，使用 MD5 散列算法得到一个散列值，对该散列值的前 4 个字节进行右移操作得到分区索引号，移动位数由上面的 part_shift 设置指定；按照分区索引号在分区到设备映射表（replica2part2dev_id）里查找该对象所在分区的对应的所有设备编号，这些设备会被尽量选择部署在不同区域（Zone）内，区域只是个抽象概念，它可以是某台机器，某个机架，甚至某个建筑内的机群，以提供最高级别的冗余性，建议至少部署 5 个区域；权重参数是个相对值，可以来根据磁盘的大小来调节，权重越大表示可分配的空间越多，可部署更多的分区。
Swift 为账户，容器和对象分别定义了的环，查找账户和容器的是同样的过程。
数据模型
Swift 采用层次数据模型，共设三层逻辑结构：Account/Container/Object（即账户/容器/对象)，每层节点数均没有限制，可以任意扩展。这里的账户和个人账户不是一个概念，可理解为租户，用来做顶层的隔离机制，可以被多个个人账户所共同使用；容器代表封装一组对象，类似文件夹或目录；叶子节点代表对象，由元数据和内容两部分组成，如图 4 所示：
图 4. Swift 数据模型
Swift 数据模型
点击查看大图
回页首
系统架构
Swift 采用完全对称、面向资源的分布式系统架构设计，所有组件都可扩展，避免因单点失效而扩散并影响整个系统运转；通信方式采用非阻塞式 I/O 模式，提高了系统吞吐和响应能力。
图 5. Swift 系统架构
Swift 系统架构
点击查看大图
Swift 组件包括：
代理服务（Proxy Server）：对外提供对象服务 API，会根据环的信息来查找服务地址并转发用户请求至相应的账户、容器或者对象服务；由于采用无状态的 REST 请求协议，可以进行横向扩展来均衡负载。
认证服务（Authentication Server）：验证访问用户的身份信息，并获得一个对象访问令牌（Token），在一定的时间内会一直有效；验证访问令牌的有效性并缓存下来直至过期时间。
缓存服务（Cache Server）：缓存的内容包括对象服务令牌，账户和容器的存在信息，但不会缓存对象本身的数据；缓存服务可采用 Memcached 集群，Swift 会使用一致性散列算法来分配缓存地址。
账户服务（Account Server）：提供账户元数据和统计信息，并维护所含容器列表的服务，每个账户的信息被存储在一个 SQLite 数据库中。
容器服务（Container Server）：提供容器元数据和统计信息，并维护所含对象列表的服务，每个容器的信息也存储在一个 SQLite 数据库中。
对象服务（Object Server）：提供对象元数据和内容服务，每个对象的内容会以文件的形式存储在文件系统中，元数据会作为文件属性来存储，建议采用支持扩展属性的 XFS 文件系统。
复制服务（Replicator）：会检测本地分区副本和远程副本是否一致，具体是通过对比散列文件和高级水印来完成，发现不一致时会采用推式（Push）更新远程副本，例如对象复制服务会使用远程文件拷贝工具 rsync 来同步；另外一个任务是确保被标记删除的对象从文件系统中移除。
更新服务（Updater）：当对象由于高负载的原因而无法立即更新时，任务将会被序列化到在本地文件系统中进行排队，以便服务恢复后进行异步更新；例如成功创建对象后容器服务器没有及时更新对象列表，这个时候容器的更新操作就会进入排队中，更新服务会在系统恢复正常后扫描队列并进行相应的更新处理。
审计服务（Auditor）：检查对象，容器和账户的完整性，如果发现比特级的错误，文件将被隔离，并复制其他的副本以覆盖本地损坏的副本；其他类型的错误会被记录到日志中。
账户清理服务（Account Reaper）：移除被标记为删除的账户，删除其所包含的所有容器和对象。
回页首
API
Swift 通过 Proxy Server 向外提供基于 HTTP 的 REST 服务接口，对账户、容器和对象进行 CRUD 等操作。在访问 Swift 服务之前，需要先通过认证服务获取访问令牌，然后在发送的请求中加入头部信息 X-Auth-Token。下面是请求返回账户中的容器列表的示例：
GET /v1/<account> HTTP/1.1
Host: storage.swift.com
X-Auth-Token: eaaafd18-0fed-4b3a-81b4-663c99ec1cbb
响应头部信息中包含状态码 200，容器列表包含在响应体中：
HTTP/1.1 200 Ok
Date: Thu, 07 Jan 2013 18:57:07 GMT
Server: Apache
Content-Type: text/plain; charset=UTF-8
Content-Length: 32

images
movies
documents
backups
Swift 支持的所有操作可以总结为表 1：
表 1. Swift RESTful API 总结
资源类型	URL	GET	PUT	POST	DELETE	HEAD
账户	/account/	获取容器列表	-	-	-	获取账户元数据
容器	/account/container	获取对象列表	创建容器	更新容器元数据	删除容器	获取容器元数据
对象	/account/container/object	获取对象内容和元数据	创建、更新或拷贝对象	更新对象元数据	删除对象	获取对象元数据
详细的 API 规范可以参考开发者指南。应用开发可采用 Swift 项目本身已经包含的 Python 的绑定实现；如果使用其它编程语言，可以参考 Rackspace 兼容 Swift 的 Cloud Files API，支持 Java，.Net，Ruby，PHP 等语言绑定。
回页首
结束语
OpenStack Swift 作为稳定和高可用的开源对象存储被很多企业作为商业化部署，如新浪的 App Engine 已经上线并提供了基于 Swift 的对象存储服务，韩国电信的 Ucloud Storage 服务。有理由相信，因为其完全的开放性、广泛的用户群和社区贡献者，Swift 可能会成为云存储的开放标准，从而打破 Amazon S3 在市场上的垄断地位，推动云计算在朝着更加开放和可互操作的方向前进。


