
FROM python
WORKDIR /app
COPY ./image_source /app
RUN apt-get update
RUN pip install -r requirements.txt
RUN python3 manage.py migrate
EXPOSE 8000
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]             