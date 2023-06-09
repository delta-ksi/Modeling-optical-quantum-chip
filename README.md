### __English language__
# Modeling tomography of optical quantum chip

### __Русский язык__
# Моделирование томографии квантового оптического чипа
## _Конструкция программы_
Программа состоит из двух основных _python_ модулей:
- __tomography.py__, который выполняет моделирование томографии оптического чипа;
- __testing.py__, который тестирует предсказанный скриптом tomography.py чип на большой тестовой выборке.

Также есть _bash_ скрипт __launch.sh__ который позволяет управлять этими двумя _python_ скриптами. Сам скрипт в первую очередь создаёт папку _/data_, в которой храниться вся информация о томографии и тестирование. У скрипта есть опции для оптимального управление численным экспериментом:
- __-tom__ | __--tomography__ - запуск только скрипта __tomography.py__. Результатом работы программы будет битовый _.dat_ файл в котором будут храниться вся информация о томографии, файл сохраняется в папке _/data_.
- __-tes__ | __--testing__ - запуск только скрипта __testing.py__. Программа будет работать с последним _.dat_ файлом в директории _/data_. Результатом выполнения программы будет дозапись _.dat_ файла результатами тестирования предсказанного чипа.