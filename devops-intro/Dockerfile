
FROM python:3.9


RUN pip install "poetry==1.0.0"


WORKDIR /code


COPY pyproject.toml poetry.lock /code/


RUN poetry config virtualenvs.create false \
    && poetry install


COPY ./app /code/app


CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "80"]
