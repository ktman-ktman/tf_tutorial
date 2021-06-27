FROM nvidia/cuda:11.3.1-cudnn8-devel-ubuntu20.04

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    curl \
    fish \
    git \
    htop \
    neovim \
    python3-dev \
    tmux \
    # for python
    #build-essential \
    #libbz2-dev \
    #libdb-dev \
    #libreadline-dev \
    #libffi-dev \
    #libgdbm-dev \
    #liblzma-dev \
    #libncursesw5-dev \
    #libsqlite3-dev \
    #libssl-dev \
    #zlib1g-dev \
    #uuid-dev \
    #tk-dev \
 && apt-get -y clean \
 && rm -rf /var/lib/apt/lists/*

# install poetry
ENV POETRY_HOME="/opt/poetry" \
    POETRY_VIRTUALENVS_IN_PROJECT=true \
    POETRY_NO_INTERACTION=1 

RUN curl -sSL https://raw.githubusercontent.com/sdispater/poetry/master/get-poetry.py | python3

RUN chmod 755 ${POETRY_HOME}/bin/poetry

# install python
#RUN git clone git://github.com/pyenv/pyenv.git \
# && pyenv/plugins/python-build/bin/python-build 3.8.10 /opt/python

CMD ["/usr/bin/fish"]
