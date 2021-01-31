FROM python:3.8.5
ENV PYTHONUNBUFFERED=1
WORKDIR /app/api
COPY requirements.txt ./
RUN pip install -r requirements.txt
RUN sed -i -E 's/MinProtocol[=\ ]+.*/MinProtocol = TLSv1.0/g' /etc/ssl/openssl.cnf
COPY . ./
EXPOSE 8000