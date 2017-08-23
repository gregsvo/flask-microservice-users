FROM python:3.6.1

# set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add requirements (to leverage Docker cache)
ADD ./requirements.pip /usr/src/app/requirements.pip

# install requirements
RUN pip install -r requirements.pip

# add app
ADD . /usr/src/app

# run server
CMD python manage.py runserver -h 0.0.0.0
