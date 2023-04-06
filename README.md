# django-todo
A simple todo app built with django

### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
$ git clone https://github.com/Nehanilajkar/Django-ToDo-Deployment-on-docker-using-Jenkins.git
```

If working locally best practice is to create a virtual env.
```bash
python -m venv env
 .\env\Scripts\activate
```

 You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide
```bash
pip install django
cd .\Django-ToDo-Deployment-on-docker-using-Jenkins\
```

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver 
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

Now we can run the app on AWS server using public ip(ec2 VM):8001 , by giving '*' in allowed hosts , to allow all ip's in todoApp/settings.py.
```bash
$ python manage.py runserver 0.0.0.0:8001 
```

Cheers and Happy Coding :)
