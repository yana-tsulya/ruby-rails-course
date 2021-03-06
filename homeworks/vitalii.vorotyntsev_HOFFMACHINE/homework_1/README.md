Описание предметной области **рыболовного инвентаря**.

Ассортимент рыболовного инвентаря очень широкий, большинство акссесуаров разных типов, наборов свойств и качеств, которые сильно зависят друг от друга при использовании.

Наша текущая цель иметь возможность сбора рыболовной снасти (удочки), для конкретного вида ловли.

Выделим несколько ключевых сущностей из которых можно собрать снасть для любого вида ловли:

 - Удилища `rods` - могут быть разных типов, кастингов, конструкций и материалов; 
 - Катушки `reels` - могут быть разных типов и фрикционов, отличатся количеством подшипников и размером шпули;
 - Оснастка `tackle` - набор готовых смонтированных снастей для разного вида ловли:
    - поплавочная;
    - спиннинговая;
    - фидерная;
    - карповая;
    - зимняя.

Предварительно у нас должен быть создан абстрактный класс `FishingRod` на основе которого можно собрать удочку для разного вида ловли и который включает в себя методы для выбора типа удилища, установки катушки и монтаж нужной оснастки.

Предполагается что для каждого вида ловли нам нужен будет свой интерфейс что бы не нарушать некоторые условия этого вида ловли при сборе новой удочки. Создадим интерфейс `Feeder` в котором по умолчанию будет задан тип удилища (фидерные) с возможностью задания дополнительных требований (длинны, кастинга, материала и так далее), а так же методы для монтажа оснастки в которые могут входить разные аксессуары (шнуры или лески, поводки, грузики, вертлюжки, крючки, кормушки и так далее).

Соберем удочку для фидерной рыбалки от фирмы **Salmo**. Нам нужно будет создать класс `SalmoSupreeme` который будет наследован из абстрактного класса `FishingRod` и будет описан по интерфейсу `Feeder`. 

Начинаем сборку:

 - Выберем фирменное композитное удилище, штекерной конструкции с длинной в 3.3 м. и кастингом 90 г.
 - Устанавливаем на удилище фирменную безынерционную катушку с бейтраннером, передним фрикционом и с размером шпули в 3000.
 - Монтируем оснастку:
    - нам понадобится шнур длиннов 2.1 м. и разрывной нагрузкой до 4.2 кг. c диамметром в 0.14 мм.;
    - с помощью застежек закрепим поводок на котором установим несколько офсетных крючков, а так же кормушку с грузиками;
    - установим сигнализатор поклёвки.

Данная удочка должна получиться комфортной для использования, её вес не должен превышать 350 г., у неё средних размеров катушка с хорошим тонким шнуром, который способен выдерживает большу разрывную нагрузку, что позволить ловить крупную рыбу.