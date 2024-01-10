# simple-django-project
## Installation

### Prerequisites

#### 1. Install Python
Install ```python-3.7.2``` and ```python-pip```. Follow the steps from the below reference document based on your Operating System.
Reference: [https://docs.python-guide.org/starting/installation/](https://docs.python-guide.org/starting/installation/)

#### 2. Install MySQL
Install ```mysql-8.0.15```. Follow the steps form the below reference document based on your Operating System.
Reference: [https://dev.mysql.com/doc/refman/5.5/en/](https://dev.mysql.com/doc/refman/5.5/en/)
#### 3. Setup virtual environment
```bash
# Install virtual environment
sudo pip install virtualenv

# Make a directory
mkdir envs

# Create virtual environment
virtualenv ./envs/

# Activate virtual environment
source envs/bin/activate
```

#### 4. Clone git repository
```bash
git clone "https://github.com/madhujha9771/Xenonstackwebsite"
```

#### 5. Install requirements
```bash
cd simple-django-project/
pip install -r requirements.txt
```

#### 6. Load sample data into MySQL
```bash
# open mysql bash
mysql -u <mysql-user> -p

# Give the absolute path of the file
mysql> source ~/simple-django-project/world.sql
mysql> exit;

```
#### 7. Edit project settings
```bash
# open settings file
vim panorbit/settings.py

# Edit Database configurations with your MySQL configurations.
# Search for DATABASES section.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'world',
        'USER': '<mysql-user>',
        'PASSWORD': '<mysql-password>',
        'HOST': '<mysql-host>',
        'PORT': '<mysql-port>',
    }
}

# Edit email configurations.
# Search for email configurations
EMAIL_USE_TLS = True
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_HOST_USER = '<your-email>'
EMAIL_HOST_PASSWORD = '<your-email-password>'
EMAIL_PORT = 587

# save the file
```
#### 8. Run the server
```bash
# Make migrations
python manage.py makemigrations
python manage.py migrate

# For search feature we need to index certain tables to the haystack. For that run below command.
python manage.py rebuild_index

# Run the server
python manage.py runserver 

# your server is up on port 8000
```
Try opening [http://127.0.0.1:8000/] in the browser.
Now you are good to go.

### 9. URLs
#### Login: 
![image](https://github.com/madhujha9771/Xenonstackwebsite/assets/86901904/f510c987-1d93-48d2-b047-d4d0d714bdcc)
#### Logout
![image](https://github.com/madhujha9771/Xenonstackwebsite/assets/86901904/a8397e9e-eee0-4a85-a0b7-176ea866b750)
#### Contact us page:
![image](https://github.com/madhujha9771/Xenonstackwebsite/assets/86901904/7b84325d-1d2e-4192-a3ae-3beafc2481bf)
### Pawword wrong:
![image](https://github.com/madhujha9771/Xenonstackwebsite/assets/86901904/28cf6bb9-f57b-4059-a3af-af5c8d22201f)

### Django database  users data 
![image](https://github.com/madhujha9771/Xenonstackwebsite/assets/86901904/095de9c1-8175-4110-8fea-b1153202765a)



### Link for project

https://freshers-guide.netlify.app/








