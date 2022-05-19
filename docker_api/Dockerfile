#FROM ubuntu:20.04
FROM python
WORKDIR ./image_source
COPY . .
RUN apt-get update
#RUN apt-get install python3-pip
#RUN apt-get install python3-venv
#RUN python3 -m venv env
#RUN source env/bin/activate
RUN pip install -r requirements.txt
RUN python3 manage.py migrate
EXPOSE 8000
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]             