FROM bigboards/jupyterhub-__arch__

MAINTAINER bigboards <hello@bigboards.io>

RUN curl -s http://d3kbcqa49mib13.cloudfront.net/spark-1.3.0-bin-hadoop2.4.tgz | tar -xz -C /opt
RUN cd /opt && ln -s ./spark-1.3.0-bin-hadoop2.4 spark

USER bb

RUN mkdir /usr/local/share/jupyter/kernels/pyspark
ADD pyspark.kernel /usr/local/share/jupyter/kernels/pyspark/kernel.json

WORKDIR /srv/jupyterhub/

EXPOSE 8000

CMD ["jupyterhub", "-f", "/srv/jupyterhub/jupyterhub_config.py"]
