# Обнаружение денег Украина - Yolov8 - Detect objects

Модель detect_money_uk для библиотеки [yolov8](https://github.com/ultralytics/ultralytics)

> Read this in other language: [Український](README.md), [English](README.en.md), [Русский](README.ru.md)

## Требования
* python3
* yolov8

## Установка
```sh
pip3 install -r requirements.txt
```

## Обучение
```sh
yolo task=detect \
mode=train \
model=yolov8s.pt \
data=data/data.yaml \
epochs=500 \
imgsz=640
```

## Обнаружение
```sh
yolo task=detect \
mode=predict \
model=model/model.pt \
conf=0.25 \
source='examples/coins.jpg'
```

## Проверка модели
```sh
python3 detect.py
```

## Преобразование сегментов в полигоны (После LabelStudio)
```sh
python3 data_seg/segpoly.py
```

## Метки
| Метка               | Описание            |
| :-------------      | :-------------      |
| bn_1                | 1 гривен            |
| bn_10               | 10 гривен           |
| bn_100              | 100 гривен          |
| bn_1000             | 1000 гривен         |
| bn_2                | 2 гривен            |
| bn_20               | 20 гривен           |
| bn_200              | 200 гривен          |
| bn_5                | 5 гривен            |
| bn_50               | 50 гривен           |
| bn_500              | 500 гривен          |
| coin_1              | 1 копеек            |
| coin_10             | 10 копеек           |
| coin_10_bn          | 10 копеек гривен    |
| coin_1_bn           | 1 копеек гривен     |
| coin_2              | 2 копеек            |
| coin_25             | 25 копеек           |
| coin_2_bn           | 2 копеек гривен     |
| coin_5              | 5 копеек            |
| coin_50             | 50 копеек           |
| coin_5_bn           | 5 копеек гривен     |

## Google Colab
```txt
yolov8.ipynb
```

# Спасибо
* [Yolov8](https://github.com/ultralytics/ultralytics)
* [LabelStudio](https://github.com/HumanSignal/label-studio)

## Примеры
![example1](https://github.com/martinjack/detect_money_uk/blob/master/examples/coins.jpg?raw=true)

![example2](https://github.com/martinjack/detect_money_uk/blob/master/examples/example1.jpg?raw=true)

![example3](https://github.com/martinjack/detect_money_uk/blob/master/examples/example2.jpg?raw=true)

![example4](https://github.com/martinjack/detect_money_uk/blob/master/examples/example3.png?raw=true)

![example5](https://github.com/martinjack/detect_money_uk/blob/master/examples/example4.png?raw=true)