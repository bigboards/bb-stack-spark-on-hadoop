FROM bigboards/jupyterhub-__arch__

MAINTAINER bigboards <hello@bigboards.io>

USER bb

WORKDIR /srv/jupyterhub/

EXPOSE 8000

CMD ["jupyterhub", "-f", "/srv/jupyterhub/jupyterhub_config.py"]
