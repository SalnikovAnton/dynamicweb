# Динамический веб Развертывание веб приложения
### 1) :   
-   
-  
### 2) 

#### 1) Для выполнения первого пункта необходимо:   
* написать [Vagrantfile](https://github.com/SalnikovAnton/VPN/blob/main/Vagrantfile "Vagrantfile"), который будет поднимать 2 виртуальные машины server и client,
* пишем роли в [serverplaybook](https://github.com/SalnikovAnton/VPN/blob/main/serverplaybook.yml "serverplaybook.yml") для сервера и [clientplaybook](https://github.com/SalnikovAnton/VPN/blob/main/clientplaybook.yml "clientplaybook.yml") для клиентской машины,
* создаем [server.conf](https://github.com/SalnikovAnton/VPN/blob/main/server/server.conf "server.conf"), [openvpn@.service](https://github.com/SalnikovAnton/VPN/blob/main/server/openvpn@.service "openvpn@.service") для сервера и [server.conf](https://github.com/SalnikovAnton/VPN/blob/main/client/server.conf "server.conf"), [openvpn@.service](https://github.com/SalnikovAnton/VPN/blob/main/server/openvpn@.service "openvpn@.service") для клиента.
   
```

```
