# Домашнее задание к занятию 1 «Введение в Ansible» - Вмнцентини С.Г.

## Подготовка к выполнению

1. Установите Ansible версии 2.10 или выше.
2. Создайте свой публичный репозиторий на GitHub с произвольным именем.
3. Скачайте [Playbook](./playbook/) из репозитория с домашним заданием и перенесите его в свой репозиторий.

## Основная часть

1. Попробуйте запустить playbook на окружении из `test.yml`, зафиксируйте значение, которое имеет факт `some_fact` для указанного хоста при выполнении playbook.
><img width="237" height="90" alt="image" src="https://github.com/user-attachments/assets/3585e8e5-d635-491b-b935-544deee4ba07" />

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на `all default fact`.
><img width="507" height="94" alt="image" src="https://github.com/user-attachments/assets/1fb0d7bb-c2d3-4d88-a405-573e7b3c33e3" />

3. Воспользуйтесь подготовленным (используется `docker`) или создайте собственное окружение для проведения дальнейших испытаний.
><img width="849" height="73" alt="image" src="https://github.com/user-attachments/assets/2211c2ee-4eb5-4034-a4d0-c7ba9db88f0c" />

4. Проведите запуск playbook на окружении из `prod.yml`. Зафиксируйте полученные значения `some_fact` для каждого из `managed host`.
><img width="237" height="143" alt="image" src="https://github.com/user-attachments/assets/6723760f-4fc4-42fc-b99c-20eb4ef3e465" />

5. Добавьте факты в `group_vars` каждой из групп хостов так, чтобы для `some_fact` получились значения: для `deb` — `deb default fact`, для `el` — `el default fact`.
><img width="454" height="106" alt="image" src="https://github.com/user-attachments/assets/4b126b16-6304-498f-90bb-16d9597878b1" />
<img width="510" height="108" alt="image" src="https://github.com/user-attachments/assets/8f825c81-2fa4-40a7-bbbc-c668797ca5f2" />

6.  Повторите запуск playbook на окружении `prod.yml`. Убедитесь, что выдаются корректные значения для всех хостов.
><img width="281" height="150" alt="image" src="https://github.com/user-attachments/assets/785f0163-e6ad-4680-bd33-e608e485f45f" />

7. При помощи `ansible-vault` зашифруйте факты в `group_vars/deb` и `group_vars/el` с паролем `netology`.
><img width="897" height="149" alt="image" src="https://github.com/user-attachments/assets/6e7eb55f-a26a-4153-8961-408a01fff7c2" />

8. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь в работоспособности.
><img width="1179" height="499" alt="image" src="https://github.com/user-attachments/assets/b257df9a-f21b-406d-9357-9c31e968d764" />

9. Посмотрите при помощи `ansible-doc` список плагинов для подключения. Выберите подходящий для работы на `control node`.
><img width="776" height="517" alt="image" src="https://github.com/user-attachments/assets/7cd6e4f7-ebc5-4896-b745-61c1ddcfa4c7" />

10. В `prod.yml` добавьте новую группу хостов с именем  `local`, в ней разместите localhost с необходимым типом подключения.
><img width="409" height="294" alt="image" src="https://github.com/user-attachments/assets/95deb7cd-5eb3-4a6f-8606-e3f9ba10b689" />

11. Запустите playbook на окружении `prod.yml`. При запуске `ansible` должен запросить у вас пароль. Убедитесь, что факты `some_fact` для каждого из хостов определены из верных `group_vars`.
><img width="388" height="202" alt="image" src="https://github.com/user-attachments/assets/6173e2b1-c54a-44b2-9d03-79812143d74b" />

12. Заполните `README.md` ответами на вопросы. Сделайте `git push` в ветку `master`. В ответе отправьте ссылку на ваш открытый репозиторий с изменённым `playbook` и заполненным `README.md`.
> 
13. Предоставьте скриншоты результатов запуска команд.
