To set up and run a Django project with a PostgreSQL database, follow these steps:

1. Install Python: Make sure Python is installed on your system. You can download it from the official Python website and follow the installation instructions for your operating system.

2. Extract code if downloded or use git cloen for the reprository

3. cd into the folder

4. Install requirements: Open a terminal or command prompt and run the following command to install requirements using pip (Python package manager):

   ```
   pip install -r requirements.txt
   ```

5. Install PostgreSQL: Download and install PostgreSQL from the official website, following the installation instructions for your operating system.

6. Set up the database: Create a new PostgreSQL database for your Django project. You can use a graphical tool like pgAdmin or run the following command in a terminal or command prompt:

   ```
   createdb your_database_name
   ```

7. Configure the Django project:
   - Create a new Django project by running the following command in the terminal or command prompt:

     ```
     django-admin startproject your_project_name
     ```

   - Open the project's settings.py file (located in the project's root directory) and update the database configuration:

     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.postgresql',
             'NAME': 'your_database_name',
             'USER': 'your_username',
             'PASSWORD': 'your_password',
             'HOST': 'localhost',
             'PORT': '',
         }
     }
     ```

     Replace `'your_database_name'`, `'your_username'`, and `'your_password'` with your actual database details.

8. Run database migrations: In the terminal or command prompt, navigate to the project's root directory (the one containing `manage.py`). Run the following command to apply the initial database migrations:

   ```
   python manage.py makemigration
   python manage.py migrate
   ```

9. Start the development server: Run the following command to start the Django development server:

   ```
   python manage.py runserver
   ```

   This will start the server, and you can access your Django project by visiting `http://localhost:8000` in your web browser.


That's it! Django project is set up and running with a PostgreSQL database. 