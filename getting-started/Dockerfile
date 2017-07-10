FROM python:2.7-slim
WORKDIR /app
ADD . /app
RUN pip install -r requirements.txt
EXPOSE 8080
ENV NAME Wellington
CMD ["python", "app.py"]