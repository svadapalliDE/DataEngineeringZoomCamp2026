FROM python:3.9.16-slim


RUN pip install pandas pyarrow

WORKDIR /code

COPY pipeline.py .

ENTRYPOINT ["python", "pipeline.py"]