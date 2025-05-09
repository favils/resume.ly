FROM python:3.10-slim

# for latex
RUN apt-get update && \
    apt-get install -y texlive-latex-base texlive-latex-extra texlive-fonts-recommended latexmk && \
    apt-get clean

# wd
WORKDIR /app

# copey
COPY . .

# install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# set environment variables
ENV PYTHONUNBUFFERED=1

# start the app
CMD ["gunicorn", "--bind", "0.0.0.0:8080", "main:create_app()"]
