Лабораторная работа № 2. Группа Б03-602

Основные Python-файлы (все имена переменных и функций на английском):
light/scripts/capture.py  — съёмка и проверка пересвета
light/scripts/spectra.py  — получение интенсивности из PNG
light/scripts/process.py  — калибровка и обработка всех листов
light/scripts/albedo.py   — альбедо нового изображения относительно белого

В light/scripts сохранены файлы lightMeasure.py, lightFunctions.py,
lightProcessing.py по названиям из задания. albedo_foto.py оставлен
для запуска старой командой. На уровне light также есть точки входа
lightMeasure.py и lightProcessing.py.

Установка зависимостей:
python3 -m pip install -r requirements.txt

Команды из папки light:
python3 lightMeasure.py white-tungsten 50000
python3 lightProcessing.py data .
python3 scripts/albedo.py 'data/blue(100000).png' 'data/white1(100000).png' data/kalibrovka.json

Результаты общей обработки: plots/*.png, data/signal.csv,
data/reflectance_curves.csv, data/kalibrovka.json.
Расчёт отдельного листа: rezultat_albedo/*.png и *.csv.

Для нового спектра нужен белый эталон, снятый той же установкой
с одинаковыми настройками камеры. Обычная фотография предмета
не позволяет рассчитать спектральное альбедо. Без калибровки
горизонтальная ось показывает строки изображения вместо длины волны.

Имена входных PNG и полей JSON сохранены для совместимости с данными
и предыдущими результатами. Подписи графиков оставлены на русском.
