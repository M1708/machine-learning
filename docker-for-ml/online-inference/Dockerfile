FROM jupyter/scipy-notebook

COPY requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

RUN mkdir model
ENV MODEL_DIR=/home/meenu/model
ENV MODEL_FILE=clf.joblib
ENV METADATA_FILE=metadata.json

COPY train.py ./train.py
COPY api.py ./api.py

RUN python3 train.py
