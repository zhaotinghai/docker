FROM python:3.6

MAINTAINER zhaotinghai <zhaotinghai@sina.cn>

RUN pip install --no-cache-dir --upgrade pip && \
pip --no-cache-dir install jupyter notebook jupyter_contrib_nbextensions pymongo apscheduler pystan fbprophet tensorflow==1.13.1 && \
python --version && \
pip list
