# LR6
Лабораторная работа №6


---

Отчёт по Лабораторной работе №6 

Тема: Система контроля версий   

Цель: Изучение базовых возможностей системы управления версиями, работа с Git API, локальным и удалённым репозиторием.

 1. Создан аккаунт на [GitHub](https://github.com/).

 2. Сделана копия (Fork) репозитория с исходного репозитория по адресу: (https://github.com/Kurtyanik/LR6).

 3. Установлен Git с официального сайта: (https://git-scm.com/).
  
 4. Настроен Git, добавлено имя пользователя и email:
  ```bash
  git config --global user.name "В3441 Кащенко Дарья Васильевна"
  git config --global user.email "dashulja09082005@gmail.com"
  ```
![screen](screen/1.jpg)

 5. Личный удалённый репозиторий был клонирован на компьютер:
  ```bash
  git clone https://github.com/KashchenkoDV/LR6
  ```
![screen](screen/2.jpg)


 6. Новый файл был добавлен через интерфейс GitHub, изменения подтянуты в локальный репозиторий: 
  ```bash
  git pull
  ```
![screen](screen/3.jpg)

 7. Получена история операций для каждой из веток:
  ```bash
  git log --oneline
  ```
![screen](screen/4.jpg)


 8. Последние изменения просмотрены с помощью команды:
  ```bash
  git log -p 
  ```
![screen](screen/5.jpg)

 9. Ветка с изменениями была слита в ветку `master`:
  ```bash
  git checkout -b new_branch
  git add .
  git commit -m "Внесено изменение №1"
  git checkout master
  git merge new_branch
  ```
![screen](screen/6.jpg)
![screen](screen/7.jpg)



 10. Побочная ветка удалена после успешного слияния:
  ```bash
  git branch -d new_branch
  ```


 11. Сделаны несколько изменений и зафиксированы с комментариями:
  ```bash
  git add .
  git commit -m "Внесено изменение №2"
  ```
![screen](screen/8.jpg)

 12. Выбран нужный коммит, выполнен откат:
  ```bash
  git log --oneline
  git revert af86fc1
  ```
![screen](screen/9.jpg)
![screen](screen/10.jpg)

 13. Создана отдельная ветка для оформления отчёта:
  ```bash
  git checkout -b report
  ```
![screen](screen/11.jpg)

 14. Отчёт оформлен в файле `README.md` с использованием markdown синтаксиса, cкриншоты консоли и сторонних программ добавлены в отдельную папку `screen`.

 15. Получена история операций с сокращённым хэшем, датой, именем автора и комментарием:
  ```bash
  git log --pretty=format:"%h - %ad - %an - %s" --date=short
  ```
![screen](screen/12.jpg)

 16. Локальные изменения отправлены в удалённый репозиторий на GitHub:
  ```bash
  git push origin report
  ```

Вывод:

В процессе данной лабораторной работы я освоила базовые команды и операции в Git, включая commit, merge, checkout, pull, push, а также управление ветками и разрешение конфликтов. Получила опыт синхронизации локального и удаленного репозиториев на GitHub и создания отчетов при помощи Markdown.
