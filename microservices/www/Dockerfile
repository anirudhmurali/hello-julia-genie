FROM julia:0.6

RUN apt-get update \
    && apt-get install -y \
    build-essential \
    vim \
    tmux \
    unzip \
    cmake \
    && apt-get clean

ADD deps.jl deps.jl

RUN julia deps.jl

COPY app /app

WORKDIR /app

CMD ["bin/server"]
