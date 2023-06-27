
# Django CRM

This project is Flask based API  to run this app locally take these steps





## Deployment

To deploy this project run Create environment

```bash
 virtualenv venv -p python3.11
```

activate venv
```
venv\Scripts\activate.bat
```
install packages
```
pip install -r requirements.txt
```
set database in setting.py

```
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.mysql",
        "NAME": "my_data",
        "USER": 'root',
        "PASSWORD": "your_password",
        "HOST": "localhost",
        "PORT":   "3306" ,
          }
}
```
do migrations to set schema
```
Python manage.py makemigrations
```
```
python manage.py migrate
```



## Docker Deployment
* NOTE: Docker Desktop is needed to run with docker 

create Docker Image
```bash
docker build -t django .
```
run the image 
```bash
docker run -p 5000:5000 flaskapp
```


