FROM python:3


COPY requirements.txt requirements.txt
RUN python -m pip install --upgrade pip
RUN pip3 install -r requirements.txt
RUN python -m pip install jupyterlab

WORKDIR /src
COPY /src /src


# docker image build -t sample/test .
# docker container run -it -p 8000:8080 --name sample -v ${PWD}/src:/src sample/test
# docker exec  -it {container_name} bash