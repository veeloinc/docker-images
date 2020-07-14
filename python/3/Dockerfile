FROM python:3.8
ENV PYTHONUNBUFFERED 1

LABEL Name="Python" \
      Version="3"

RUN apt-get update && apt-get install --no-install-recommends -y \
  libxmlsec1-dev \
  pdftk \
  postgresql-client \
  python-dev \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
RUN pip install --no-cache-dir -U \
  pip \
  pre-commit \
  setuptools \
  virtualenv \
  wheel
RUN virtualenv -p $(which python2) ${HOME}/.venv/python2
RUN /bin/bash -c "source ${HOME}/.venv/python2/bin/activate; \
  pip install --no-cache-dir -U pip-tools"
