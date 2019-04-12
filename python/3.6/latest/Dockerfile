FROM zhaotinghai/python:3.6-base

# MAINTAINER zhaotinghai <zhaotinghai@sina.cn>

# RUN pip --no-cache-dir install jupyter notebook jupyter_contrib_nbextensions pymongo apscheduler pystan fbprophet tensorflow==1.13.1 \

RUN pip --no-cache-dir install keras scipy statsmodels sklearn seaborn && \

jupyter notebook --generate-config && \

jupyter contrib nbextension install --user && \

python --version && pip list
