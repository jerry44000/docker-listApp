FROM python:2.7-slim-buster
MAINTAINER SHAI
ADD student_age.py /
RUN apt-get update && apt-get install -y --no-install-recommends \
    gcc \
    python-dev \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    && pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0 \
    && pip install python-ldap==3.3.0 \
    && rm -rf /var/lib/apt/lists/*
VOLUME ["/data"]
EXPOSE 5000
CMD ["python", "./student_age.py"]

