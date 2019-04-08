# Flask Example
### demo on Flask&SQLAlchemy (MIPT 2019)


### Flask official tutorial:
http://flask.pocoo.org/docs/1.0/tutorial/


### Usage:
```
pip3 install flask
python3 db_create.py
python3 run.py --debug
```

Из терминала позадаём запросы к поднятому сервису:
```
curl "http://127.0.0.1:5000"
>"Hello World"

curl "http://127.0.0.1:5000/add_user?nickname=Irina"
> "OK"

curl http://127.0.0.1:5000/add_user?nickname=Pavel
> "OK"

curl "http://127.0.0.1:5000/add_post?nickname=Irina&text=HelloWorld"
> "OK"

curl "http://127.0.0.1:5000/add_post?nickname=Irina&text=HelloWorld2"
> "OK"

curl "http://127.0.0.1:5000/add_post?nickname=NoSuchUser&text=HelloWorld"
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>400 Bad Request</title>
<h1>Bad Request</h1>
<p>The browser (or proxy) sent a request that this server could not understand.</p>

```
curl http://127.0.0.1:5000/get_user_posts?nickname=Pavel
> []

curl http://127.0.0.1:5000/get_user_posts?nickname=Pavel
> [
    "HelloWorld", 
    "HelloWorld2"
  ]
```
