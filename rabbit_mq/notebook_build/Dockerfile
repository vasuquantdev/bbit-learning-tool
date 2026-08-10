FROM jupyter/scipy-notebook:python-3.11
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
ENV PYTHONPATH=/app

ENTRYPOINT ["/bin/bash", "-c", "jupyter lab"]

