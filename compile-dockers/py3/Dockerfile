FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
	software-properties-common \
	python-software-properties

RUN apt-get update && apt-get install -y \
	python3.5

RUN apt-get update && apt-get install -y \
	python3-pip

RUN pip3 install numpy

RUN groupadd -r compiler --gid=2016 && useradd -M -s /bin/bash -R / compiler -u 2016 -g compiler

COPY compile_code /compile_code
COPY utils /utils

CMD python3.5 compile_code/compile.py
