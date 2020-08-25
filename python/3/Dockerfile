FROM python:3.7.8
ENV PYTHONUNBUFFERED 1

LABEL Name="Python" \
      Version="3"

RUN apt-get update && apt-get install --no-install-recommends -y \
  libxmlsec1-dev \
  pdftk \
  postgresql-client \
  python-dev \
  tree \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
RUN pip install --no-cache-dir -U \
  pip \
  pre-commit \
  setuptools \
  virtualenv \
  wheel
