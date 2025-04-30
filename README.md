# Домашнее задание к занятию 17.3 «Использование Ansible» - Падеев Василий


## Подготовка к выполнению

1. Подготовьте в Yandex Cloud три хоста: для `clickhouse`, для `vector` и для `lighthouse`.  
2. Репозиторий LightHouse находится [по ссылке](https://github.com/VKCOM/lighthouse).

## Основная часть

1. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.

Доработан playbook [Site.yml](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/playbook/site.yml), дополнительно устанавливаются сервисы Nginx, git, nodejs, npm.

2. При создании tasks рекомендую использовать модули: `get_url`, `template`, `yum`, `apt`.  
3. Tasks должны: скачать статику LightHouse, установить Nginx или любой другой веб-сервер, настроить его конфиг для открытия LightHouse, запустить веб-сервер.

![answer1](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/1.png)  
![answer2](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/2.png)  
![answer3](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/3.png)  
![answer4](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/4.png)  

4. Подготовьте свой inventory-файл `prod.yml`.  
5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть.  

![answer5](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/5.png)  
![answer6](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/6.png)  

6. Попробуйте запустить playbook на этом окружении с флагом `--check`.

![answer7](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/7%20--check1.png)  
![answer8](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/8%20--check2.png)  

7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.  

![answer1](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/9%20--diff1.png)  
![answer1](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/10--diff2.png)  

8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.

![answer1](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/11--diff3.png)  
![answer1](https://github.com/Vasiliy-Ser/using_ansible_17.3/blob/3eb9c933ada3e9f1f4a27ebb587e7aa4534ac91d/png/12--diff4.png)  

9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.  
10. Готовый playbook выложите в свой репозиторий, поставьте тег `08-ansible-03-yandex` на фиксирующий коммит, в ответ предоставьте ссылку на него.

---
