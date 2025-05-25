
# Документация проекта
## Авторы
Петров Вадим

Чайкин Илья

Чжан Цзияо(Иван)

Пан Цзясюй(Константин)

Руководитель: Куклин Егор Вадимович

## Описание опставленной задачи
Мы команда, которая занимается совмещением аппаратуры и программного обеспечения. Главная задача нашей команды — сделать работу устройств надежной, стабильной и совместимой с программами, устраняя возникающие неполадки и проблемы.

## Ссылка на репозиторий (2024 год)
[HS Line 316](https://github.com/anvax/HS_line316?tab=readme-ov-file#%D0%B0%D0%B2%D1%82%D0%BE%D1%80%D1%8B)

## Используемое ПО
Siemens TIA Portal V16 / SIMATIC STEP 7 incl. Safety and WinCC V16  

UaExpert

## Архитектура
ПЛК взаимодействут друг с другом благодаря стандарту Profinet 

![изображение](https://github.com/n0th1ngs89/HS_Line_316_I-O/assets/146949002/05848d01-be59-402f-ab1c-b9a10d6a265b)

## Основные задачи нашей команды:
* Находим и исправляем проблемы в оборудовании.
* Проверяем устройства на стабильность и качество работы.
* Выполняем совместную работу с командой разработчиков для повышения надежности линии.
* Ищем идеи, как дополнительно усовершенствовать линию.

## Выполненные задачи:
Задачи по обслуживании линии:
* Тестирование установки в  ручном режиме.
* Осуществили проверку тэгов.
* Снятие с установки экрана
  
[<img src="https://github.com/user-attachments/assets/1af6d73b-b7f7-416d-a668-f68a07459118" width="400">](src)

* Доработка захвата фишек.
* Занимались устранением проблем связанных  с коробкой с шайбой, которая не попадала в желоба.
  
[<img src="https://github.com/user-attachments/assets/54b70992-08bc-40f2-b56a-f753c63754ba" width="400">](src)

* Поиск замены ПЛК s7-1200 на модули ввода-вывода. 
* Решиние проблем с частью механизма открытия и закрытя коробки.

Помимо обслуживания линии, мы также занимались и другими задачами: 
* Формированием идей того, как обеспечить надежность упаковки коробки на линии
* Решение задачи по сбору модуля RFID и его установке на линию. 

[<img src="https://github.com/user-attachments/assets/491d7efc-19e8-4b87-91e2-54fa183a3fff" width="400">](src)

* Составлением списка компонентов на покупку.
  
## Список компонентов на закупку
Модули ввода-вывода:
* Для Handling and Packing station PLC –  ICP DAS U-7561M
* Для Sorting station PLC – ICP DAS U-7567M
* Для Proccesing station PLC – ICP DAS U-7560M.
* DIN-рейки для их потенциального монатажа

Пневматика:
* Электромагнитные пневматические клапаны 
* Фитинги и трубки
* Промышленные пневматические провода

Остальное:
* Замены коробки для испытаний модель siemens
* Кабель Elitronic LIYY 21×0.34 ZL 68081 для замены:
  
[<img src="https://github.com/user-attachments/assets/95cd8a85-98d6-4d4b-8718-fff85e085a2d" width="400">](src)

## Что  мы оставляем студентам следующего курса!
* Возможность замены контроллеры ПЛК на модули ввода-вывода и установка их на линии.
* Возможность замены OPC UA сервера.
* Может понадобиться составить новый список деталей для закупки.
* Решение возникших проблем со станцией упаковки и конвейером.


## Возникшие сложности, которые не были исправлены:

1. Станция упаковки перестала работать:

![image](https://github.com/user-attachments/assets/fa8d52de-d188-4816-a5e2-82cd28327f81)

2. Конвейер стал плохо работать: с разной скоростью или останавливается. Возможные причины: неисправности редуктора или подшипников.

![image](https://github.com/user-attachments/assets/2dc79251-760e-4314-9679-96f86111fe8b)

## Таблица входных и выходных тэгов

### Proccesing station PLC
<table>
  <tr>
    <td>Тэги</td>
    <td>Описание</td>
    <td>Адрес</td>
  </tr>
  <tr>
    <th colspan="3">Входы</th>
  </tr>
  
  <tr>
    <td>processing_input_1_workpiece_detected</td>
    <td>шайба на определении цвета</td>
    <td>I0.1</td>
  </tr>
<tr>
    <td>processing_input_2_workpiece_silver</td>
    <td>датчик для серебристой шайбы</td>
    <td>I0.2</td>
  </tr>
  <tr>
    <td>processing_input_5_carousel_init</td>
    <td>поворот карусели на 45 градусов</td>
    <td>I0.5</td>
  </tr>
  <tr>
    <td>processing_input_6_hole_detected</td>
    <td>дырка сверху шайбы</td>
    <td>I0.6</td>
  </tr>
  
  <tr>
    <td>processing_input_7_workpiece_not_black</td>
    <td>датчик для красной и серебристой шайбы</td>
    <td>I0.7</td>
  </tr>
  <tr>
    <th colspan="3">Выходы</th>
  </tr>
  <tr>
    <td>processing_output_0_drill</td>
    <td>включить дрель</td>
    <td>Q0.0</td>
  </tr>
<tr>
    <td>processing_output_1_rotate_carousel</td>
    <td>включить вращение карусели</td>
    <td>Q0.1</td>
  </tr>
  <tr>
    <td>processing_output_2_drill_down</td>
    <td>опустить дрель</td>
    <td>Q0.2</td>
  </tr>
  <tr>
    <td>processing_output_3_drill_up</td>
    <td>поднять дрель</td>
    <td>Q0.3</td>
  </tr>
  
  <tr>
    <td>processing_output_4_fix_workpiece</td>
    <td>зафиксировать шайбу</td>
    <td>Q0.4</td>
  </tr>
<tr>
    <td>processing_output_5_detect_hole/td>
    <td>опустить определитель дырки</td>
    <td>Q0.5</td>
  </tr>
</table>

### Handling and Packing station PLC

<table>
  <tr>
    <td>Тэги</td>
    <td>Описание</td>
    <td>Адрес</td>
  </tr>
  <tr>
    <th colspan="3">Входы</th>
  </tr>
  
  <tr>
    <td>handling_input_0_workpiece_pushed</td>
    <td>шайба выдвинута</td>
    <td>I0.0</td>
  </tr>
<tr>
    <td>handling_input_1_grippe_at_right</td>
    <td>гриппер в крайнем правом положении</td>
    <td>I0.1</td>
  </tr>
  <tr>
    <td>handling_input_2_gripper_at_start </td>
    <td>гриппер в начальном положении</td>
    <td>I0.2</td>
  </tr>
  <tr>
    <td>handling_input_3_gripper_down_pack_lvl</td>
    <td>гриппер над упаковщиком</td>
    <td>I0.3</td>
  </tr>
  
  <tr>
    <td>packing_input_7_pack_turned_on</td>
    <td>упаковщик включен</td>
    <td>I0.7</td>
  </tr>
  <tr>
    <th colspan="3">Выходы</th>
  </tr>
  <tr>
    <td>handling_output_0_to_green</td>
    <td>зеленый цвет светофора</td>
    <td>Q0.0</td>
  </tr>
  <tr>
    <td>handling_output_1_to_yellow</td>
    <td>желтый цвет светофора</td>
    <td>Q0.1</td>
  </tr>
<tr>
    <td>handling_output_2_to_red</td>
    <td>красный цвет светофора</td>
    <td>Q0.2</td>
  </tr>
  <tr>
    <td>handling_output_3_gripper_to_right</td>
    <td>движение гриппера вправо</td>
    <td>Q0.3</td>
  </tr>
  <tr>
    <td>handling_output_4_gripper_to_left</td>
    <td>движение гриппера влево</td>
    <td>Q0.4</td>
  </tr>
  
  <tr>
    <td>handling_output_5_gripper_to_down</td>
    <td>переключатель движения гриппера вниз</td>
    <td>Q0.5</td>
  </tr>
<tr>
    <td>handling_output_6_gripper_to_open</td>
    <td>переключатель открытия клешни гриппера</td>
    <td>Q0.6</td>
  </tr>
  <tr>
    <td>handling_output_7_gripper_push_workpiece</td>
    <td>вытолкнуть шайбу</td>
    <td>Q0.6</td>
  </tr>
<tr>
    <td>packing_output_4_push_box</td>
    <td>вытолкнуть коробку</td>
    <td>Q0.4</td>
  </tr>
  <tr>
    <td>packing_output_5_fix_box_upper_side</td>
    <td>зафиксировать верхнюю часть коробки</td>
    <td>Q0.5</td>
  </tr>
  <tr>
    <td>packing_output_6_fix_box_tongue/td>
    <td>зафиксировать язычок коробки</td>
    <td>Q0.6</td>
  </tr>
  
  <tr>
    <td>packing_output_7_pack_box</td>
    <td>упаковать коробку</td>
    <td>Q0.7</td>
  </tr>
</table>

### Sorting station PLC
<table >
  <tr>
    <td>Тэги</td>
    <td>Описание</td>
    <td>Адрес</td>
  </tr>
  <tr>
    <th colspan="3">Входы</th>
  </tr>
  
  <tr>
    <td>sorting_input_3_box_on_conveyor</td>
    <td>коробка на конвейере</td>
    <td>I0.3</td>
  </tr>
<tr>
    <td>sorting_input_4_box_is_down</td>
    <td>коробка упала в желоб со своим цветом</td>
    <td>I0.4</td>
  </tr>
  <tr>
    <th colspan="3">Выходы</th>
  </tr>
  <tr>
    <td>sorting_output_0_move_conveyor_right </td>
    <td>включить движение конвейера вправо</td>
    <td>Q0.0</td>
  </tr>
<tr>
    <td>sorting_output_1_move_conveyor_left</td>
    <td>включить движение конвейера влево</td>
    <td>Q0.1</td>
  </tr>
  <tr>
    <td>sorting_output_2_push_silver_workpiece</td>
    <td>толкатель для серебристой шайбы</td>
    <td>Q0.2</td>
  </tr>
  <tr>
    <td>sorting_output_3_push_red_workpiece</td>
    <td>толкатель для красной шайбы</td>
    <td>Q0.3</td>
  </tr>
</table>
