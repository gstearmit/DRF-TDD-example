## DRF-TDD-Example

An example Django REST framework project for test driven development.

### Test Case Scenarios
* Test to verify registration with invalid password.
* Test to verify registration with already exists username.
* Test to verify registration with valid datas.
* Tested API authentication endpoint validations.
* Tested authenticated user authorization. 
* Create a todo with API.
* Update a todo with API.
* Update a todo with API.
* Delete a todo with API.
* Get todo list for a user.

### API Endpoints

#### Users

* **/api/users/** (User registration endpoint)
* **/api/users/login/** (User login endpoint)
* **/api/users/logout/** (User logout endpoint)


#### Todos

* **/api/todos/** (Todo create and list endpoint)
* **/api/todos/{todo-id}/** (Todo retrieve, update and destroy endpoint)

### Install 
    python -m venv  todoapp
    source todoapp/bin/activate
    pip install -r requirements.txt

### Usage
    
    $ cd todoapp/
    python manage.py test

    ------------------------------------
    
    nosetests --with-coverage --cover-package=users,todos --verbosity=1
    
    Creating test database for alias 'default'...
    ..................
    Name                               Stmts   Miss  Cover
    ------------------------------------------------------
    todos/__init__.py                      0      0   100%
    todos/admin.py                         6      6     0%
    todos/migrations/0001_initial.py       8      0   100%
    todos/migrations/__init__.py           0      0   100%
    todos/models.py                       15     15     0%
    todos/permissions.py                   4      0   100%
    todos/serializers.py                  12      0   100%
    todos/urls.py                          4      0   100%
    todos/views.py                        15      0   100%
    users/__init__.py                      0      0   100%
    users/admin.py                         1      1     0%
    users/migrations/__init__.py           0      0   100%
    users/models.py                        2      2     0%
    users/serializers.py                  37      1    97%
    users/urls.py                          4      0   100%
    users/views.py                        48      0   100%
    ------------------------------------------------------
    TOTAL                                156     25    84%
    ----------------------------------------------------------------------
    Ran 18 tests in 4.105s
    
    OK
    Destroying test database for alias 'default'...
    
### ————— Khi có Model mới cần update vào db ——————
    $ python manage.py makemigrations 
    $ python manage.py migrate
    
    
### Chay Admin
    $ python manage.py runserver  
    or 
    $ python manage.py runserver 127.0.0.1:7000 
    http://127.0.0.1:8000/admin/