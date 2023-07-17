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
```
И выполним проверку








* написать [Vagrantfile](https://github.com/SalnikovAnton/VPN/blob/main/Vagrantfile "Vagrantfile"), который будет поднимать 2 виртуальные машины server и client,
* пишем роли в [serverplaybook](https://github.com/SalnikovAnton/VPN/blob/main/serverplaybook.yml "serverplaybook.yml") для сервера и [clientplaybook](https://github.com/SalnikovAnton/VPN/blob/main/clientplaybook.yml "clientplaybook.yml") для клиентской машины,
* создаем [server.conf](https://github.com/SalnikovAnton/VPN/blob/main/server/server.conf "server.conf"), [openvpn@.service](https://github.com/SalnikovAnton/VPN/blob/main/server/openvpn@.service "openvpn@.service") для сервера и [server.conf](https://github.com/SalnikovAnton/VPN/blob/main/client/server.conf "server.conf"), [openvpn@.service](https://github.com/SalnikovAnton/VPN/blob/main/server/openvpn@.service "openvpn@.service") для клиента.
   
```

```
