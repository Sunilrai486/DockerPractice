FROM python:3.7.3-slim
LABEL maintainer="Sunil Rai <sunilrai486@outlook.com>"
LABEL version="0.1"
LABEL description="Noteboook and data (.csv file) to provide a summary of the total medals won by participating countries in the 2008 Summer Olympics."

WORKDIR /data

COPY . /data

RUN apt-get update && apt-get install -y build-essential

RUN pip install --upgrade pip && pip install numpy pandas==0.24.2 seaborn jupyter

EXPOSE 8888

CMD ["jupyter","notebook","--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
