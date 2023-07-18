# Динамический веб Развертывание веб приложения
### Вариант стенда:
- nginx + php-fpm (laravel/wordpress) + python (flask/django) + js(react/angular);

#### Для выполнения используем [методичку](https://github.com/SalnikovAnton/VPN/blob/main/dynamicweb.pdf "методичка"):   
Создаем файл и согласно структуре проекта
```
anton@anton-VirtualBox:~/dynamicweb$ tree
locales-launch: Data of ru_RU locale not found, generating, please wait...
.
├── dynamicweb.pdf
├── project
│   ├── docker-compose.yml
│   ├── nginx-conf
│   │   └── nginx.conf
│   ├── node
│   │   └── test.js
│   └── python
│       ├── Dockerfile
│       ├── manage.py
│       ├── mysite
│       │   ├── asgi.py
│       │   ├── __init__.py
│       │   ├── settings.py
│       │   ├── urls.py
│       │   └── wsgi.py
│       └── requirements.txt
├── provision_log
├── prov.yml
└── Vagrantfile
```
Конфигурирование выполнено, разворачиваем стенд 
```
anton@anton-VirtualBox:~/dynamicweb$ vagrant up
Bringing machine 'DynamicWeb' up with 'virtualbox' provider...
==> DynamicWeb: Importing base box 'bento/ubuntu-20.04'...
==> DynamicWeb: Matching MAC address for NAT networking...
==> DynamicWeb: Setting the name of the VM: dynamicweb_DynamicWeb_1689623879649_21564
==> DynamicWeb: Clearing any previously set network interfaces...
==> DynamicWeb: Preparing network interfaces based on configuration...

***

TASK [Copy project] ************************************************************
changed: [DynamicWeb]

TASK [reset ssh connection] ****************************************************

TASK [Run container] ***********************************************************
changed: [DynamicWeb]

PLAY RECAP *********************************************************************
DynamicWeb                 : ok=10   changed=8    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```
И выполним проверку
* http://localhost:8081/
![Image alt](https://github.com/SalnikovAnton/dynamicweb/blob/main/skrin/localhost_8081.png)     
* http://localhost:8082/
![Image alt](https://github.com/SalnikovAnton/dynamicweb/blob/main/skrin/localhost_8082.png)     
* http://localhost:8083/
![Image alt](https://github.com/SalnikovAnton/dynamicweb/blob/main/skrin/localhost_8083.png)     
