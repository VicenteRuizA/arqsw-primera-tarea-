FROM python:3.9

WORKDIR /code

RUN mkdir -p /code/logs

COPY ./requirements.txt /code/requirements.txt
RUN pip install --no-cache-dir --upgrade -r /code/requirements.txt
COPY ./app /code/app

EXPOSE 8070
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8070"]
