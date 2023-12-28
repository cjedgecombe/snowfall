# designate official python base image
FROM python:3.12.0

# designate working directory within docker virtual environment
WORKDIR /usr/src/app

# prevents python from writing byte code files to disk (keeps environment cleaner)
ENV PYTHONDONTWRITEBYTECODE 1
# allows the viewing of django logs in real time vs. buffered
ENV PYTHONUNBUFFERED 1

# update pip and install dependencies
RUN pip install --upgrage pip
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# copy project to working directory
COPY . .