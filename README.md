
### Note:
It works only on 3.6 not in 3.8


# Flask-SocketIO integration with Celery
This repository contains an example code which shows the integration between Flask, Socket.IO and Celery. The application is made in Flask where a counting task, representing a lengthy task, is performed by the celery worker. To update the client with the status of the task, Flask-SocketIO (by Miguel Grinberg) is used in the application to communicate with the celery task and report to the client. 

## Quick Setup
```
pip install -r requirements.txt
rabbitmq-server (run in a separate terminal - terminal 1)
celery worker -A app.celery --loglevel=info (run in a separate terminal - terminal 2)
python app.py (run in a separate terminal - terminal 3)
```

### Server
```
http://localhost:5000/
```



### Original Source:
[Flask-SocketIO-Celery](https://github.com/poonesh/Flask-SocketIO-Celery-example)


### Issues:
[socketio monkey patch issues](https://stackoverflow.com/questions/44104683/flask-socket-io-giving-redis-error-but-i-am-using-rabbitmq)
