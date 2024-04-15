FROM pytorch/pytorch:1.13.1-cuda11.6-cudnn8-runtime

WORKDIR /workspace/
COPY requirements.txt .
RUN apt update
RUN apt install -y gcc
RUN pip install -r requirements.txt
RUN pip install torchaudio --index-url https://download.pytorch.org/whl/cu116
RUN pip install pandas==2.2.2
COPY . .