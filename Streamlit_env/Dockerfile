FROM python:3
USER root

EXPOSE 8501

COPY requirements.txt .
RUN python -m pip install --upgrade pip
RUN pip3 install -r requirements.txt
RUN python -m pip install jupyterlab

WORKDIR /src
COPY /src /src

CMD streamlit run app.py
