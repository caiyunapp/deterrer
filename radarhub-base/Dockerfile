FROM python:3.8.12-bullseye

LABEL name="radarhub-base"

WORKDIR /app

RUN apt update && \
    apt install -y wget proj-bin && \
    apt install -y libgl1 vim libhdf5-dev && \
    pip3 install --upgrade pip wheel setuptools && \
    pip3 install supervisor && \ 
    pip3 install torch==1.10.0+cpu torchvision==0.11.0+cpu -f https://download.pytorch.org/whl/torch_stable.html && \
    mkdir -p /var/log/supervisor && \
    apt-get clean
