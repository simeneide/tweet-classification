from gcr.io/tensorflow/tensorflow:1.4.1-devel-py3

RUN pip3 --no-cache-dir install \
	keras \
	jupyterlab \
	annoy==1.9.5 \
	jsonlines==1.2.0 \
	seaborn==0.8.1

RUN apt-get update && \
	apt-get install less emacs -y

# IPython
EXPOSE 8888
# get good shell in jupyter lab
ENV SHELL=/bin/bash

WORKDIR /home/
ADD . /home/

CMD jupyter lab --allow-root
