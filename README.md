# Операционные системы и виртуализация (Linux) (семинары). Урок 8. Скрипты Bash

## Задание

### 1. Написать скрипт очистки директорий. На вход принимает путь к директории. Если директория существует, то удаляет в ней все файлы с расширениями .bak, .tmp, .backup. Если директории нет, то выводит ошибку.

## Выполнение

[Перейти к скрипту](https://github.com/Dmitri54/Linux_HW/blob/main/delDir.sh)

Создаем и открываем файл следующими командами:

cat > delDir

Далее прописываем текст, указанный ниже:

#!/bin/bash

read -p "Введите путь к дирректории: " DELDIR

if [ -e $DELDIR ]
    then
        echo 'Указанная дирректория найдена'
        cd $DELDIR
        echo 'Произвожу удаление'
        rm -v *.bak *.tmp *.backup
        echo 'Удаление завершено успешно'
    else
        echo 'Указанная дирректория не найдена! Выполнение остановлено'
        exit 2
fi

Сохраняем и запускаем в Bash:

bash delDir

