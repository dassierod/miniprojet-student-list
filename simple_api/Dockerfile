FROM python:3.11-slim

LABEL maintainer="Rodrigue Dassie"
RUN apt-get update -y && apt-get install -y \
python3-dev \
libsasl2-dev \
libldap2-dev \
libssl-dev \
gcc \
build-essential
COPY requirements.txt /

RUN pip3 install -r /requirements.txt
COPY student_age.py /
VOLUME /data
EXPOSE 5000
CMD ["python3", "student_age.py"]