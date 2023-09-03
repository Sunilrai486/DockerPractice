FROM continuumio/miniconda3

LABEL maintainer="Sunil Rai <sunilrai486@outlook.com>"
LABEL description="Dev environment for machine learning and data science team with access to shared data in network drive."

WORKDIR /data

RUN apt-get update && apt-get install -y build-essential

RUN conda install jupyter -y && conda install python==3.7.3 -y && conda install pandas==0.24.2 -y && conda install seaborn==0.9.0 -y && conda clean -y -all

EXPOSE 8888

VOLUME /data

CMD ["jupyter","notebook","--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
