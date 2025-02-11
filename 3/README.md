Домашнее задание к уроку Автоматизация администрирования Ansible-1 №3 - Первые шаги с Ansible

 Playbook webserv: 
 
 Устанавливает nginx
 
 Таск Configure NGINX из файла nginx.conf.j2 переносит настройки в nginx.conf
 
 Таск New site подменят файл index.html на сервере
 
 
 handlers перезагружают и перезапускает nginx
 
 Результат работы Playbook в ansible-playbook.png
 
 Результат проверки работы веб сервера в curl.png  
