# Виявляння грошей України - Yolov8 - Виявлення об'єктів

Модель detect_money_uk для бібліотеки [yolov8](https://github.com/ultralytics/ultralytics)

> Read this in other language: [Український](README.md), [English](README.en.md), [Русский](README.ru.md)

## Вимоги
* python3
* yolov8

## Встановлення
```sh
pip3 install -r requirements.txt
```

## Навчання
```sh
yolo task=detect \
mode=train \
model=yolov8s.pt \
data=data/data.yaml \
epochs=500 \
imgsz=640
```

## Виявлення
```sh
yolo task=detect \
mode=predict \
model=model/model.pt \
conf=0.25 \
source='examples/coins.jpg'
```

## Перевірка моделі
```sh
python3 detect.py
```

## Перетворення сегментів на полігони (Після LabelStudio)
```sh
python3 data_seg/segpoly.py
```

## Мітки
| Мітка               | Опис                |
| :-------------      | :-------------      |
| bn_1                | 1 гривень           |
| bn_10               | 10 гривень          |
| bn_100              | 100 гривень         |
| bn_1000             | 1000 гривень        |
| bn_2                | 2 гривень           |
| bn_20               | 20 гривень          |
| bn_200              | 200 гривень         |
| bn_5                | 5 гривень           |
| bn_50               | 50 гривень          |
| bn_500              | 500 гривень         |
| coin_1              | 1 копійок           |
| coin_10             | 10 копійок          |
| coin_10_bn          | 10 копійок гривень  |
| coin_1_bn           | 1 копійок гривень   |
| coin_2              | 2 копійок           |
| coin_25             | 25 coin             |
| coin_2_bn           | 2 копійок гривень   |
| coin_5              | 5 копійок           |
| coin_50             | 50 копійок          |
| coin_5_bn           | 5 копійок гривень   |

## Google Colab
```txt
yolov8.ipynb
```

# Подяка
* [Yolov8](https://github.com/ultralytics/ultralytics)
* [LabelStudio](https://github.com/HumanSignal/label-studio)

## Приклади
![example1](https://github.com/martinjack/detect_money_uk/blob/master/examples/coins.jpg?raw=true)

![example2](https://github.com/martinjack/detect_money_uk/blob/master/examples/example1.jpg?raw=true)

![example3](https://github.com/martinjack/detect_money_uk/blob/master/examples/example2.jpg?raw=true)

![example4](https://github.com/martinjack/detect_money_uk/blob/master/examples/example3.png?raw=true)

![example5](https://github.com/martinjack/detect_money_uk/blob/master/examples/example4.png?raw=true)