FROM python:3.7.4
 
#ARG project_directory
#WORKDIR $project_directory

RUN mkdir -p /var/www/sample/src
#WORKDIR /var/www
 
#WORKDIR /var/www
WORKDIR /var/www/sample

COPY ./uwsgi/requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

#WORKDIR /var/www
#WORKDIR /var/www/sample
COPY ./uwsgi/uwsgi.ini ./

WORKDIR /var/www/sample/src
#COPY ./uwsgi/app.py ./

CMD ["uwsgi","--ini","/var/www/sample/uwsgi.ini"]
