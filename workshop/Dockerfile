from gcr.io/tensorflow/tensorflow:1.4.1-devel-py3

RUN pip3 --no-cache-dir install \
	keras \
	jupyterlab \
	annoy==1.9.5 \
    xgboost==0.7.post3
	
RUN apt-get update && \
	apt-get install less emacs -y
	
# IPython
EXPOSE 8888
# get good shell in jupyter lab
ENV SHELL=/bin/bash

WORKDIR /home/
ADD . /home/

# Cleanup
RUN rm -rf /tmp/pip && \
rm -rf /root/.cache && \
apt-get clean && \
rm -rf /var/lib/apt/lists/*

CMD jupyter lab --allow-root