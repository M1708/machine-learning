FROM jupyter/scipy-notebook

RUN pip install joblib

RUN mkdir model
ENV MODEL_DIR=/home/meenu/model
ENV MODEL_FILE=clf.joblib
ENV METADATA_FILE=metadata.json

COPY train.py ./train.py
COPY inference.py ./inference.py

RUN python3 train.py
