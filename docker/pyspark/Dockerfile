FROM jupyter/notebook

MAINTAINER bigboards <hello@bigboards.io>

RUN curl -s http://d3kbcqa49mib13.cloudfront.net/spark-1.3.0-bin-hadoop2.4.tgz | tar -xz -C /opt
RUN cd /opt && ln -s ./spark-1.3.0-bin-hadoop2.4 spark

RUN mkdir -p ~/.ipython/kernels/pyspark
ADD ./kernel.json ~/.ipython/kernels/pyspark/kernel.json

USER root

EXPOSE 80

WORKDIR /data

CMD ["/bin/bash"]
