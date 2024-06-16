# Лабораторная работа: Tree классификатор



## Описание
Данная лабораторная работа посвящена исследованию классификатора "деревья решенийй" на различных наборах данных с использованием R.

## Содержание
1. [Задание 1](#задание-1)
2. [Задание 2](#задание-2)
3. [Задание 3](#задание-3)
5. [Задание 4](#задание-4)
6.  [Задание 5](#задание-5)
7.   [Задание 6](#задание-6)
8.  [Решение](#решение)

## Задание 1 

Загрузите набор данных Glass из пакета “mlbench”. Набор данных (признаки, классы) был 
изучен в работе «Метод ближайших соседей». Постройте дерево классификации для модели, 
задаваемой следующей формулой: **Type ~ .**, дайте интерпретацию полученным результатам. При 
рисовании дерева используйте параметр cex=0.7 для уменьшения размера текста на рисунке, 
например, text(bc.tr,cex=0.7) или draw.tree(bc.tr,cex=0.7). Является ли построенное дерево 
избыточным? Выполните все операции оптимизации дерева.

## Задание 2

Загрузите набор данных spam7 из пакета DAAG. Постройте дерево классификации для 
модели, задаваемой следующей формулой: **yesno ~.**, дайте интерпретацию полученным 
результатам. Запустите процедуру “**cost-complexity prunning**” с выбором параметра **k** по 
умолчанию, **method = ’misclass’**, выведите полученную последовательность деревьев. Какое из 
полученных деревьев, на Ваш взгляд, является оптимальным? Объясните свой выбор.

## Задание 3

Загрузите набор данных nsw74psid1 из пакета DAAG. Постройте регрессионное дерево для 
модели, задаваемой следующей формулой: **re78 ~.**. Постройте регрессионную модель и SVM-
регрессию для данной формулы. Сравните качество построенных моделей, выберите 
оптимальную модель и объясните свой выбор.

## Задание 4

Загрузите набор данных Lenses Data Set из файла Lenses.txt: 

3 класса (последний столбец): 
1 : пациенту следует носить жесткие контактные линзы
2 : пациенту следует носить мягкие контактные линзы
3 : пациенту не следует носить контактные линзы.

Признаки (категориальные):
1. возраст пациента:
   (1) молодой
   (2) предстарческая дальнозоркость
   (3) старческая дальнозоркость 
2. состояние зрения:
   (1) близорукий
   (2) дальнозоркий 
4. астигматизм:
   (1) нет
   (2) да 
7. состояние слезы:
   (1) сокращенная
   (2) нормальная
   
Постройте дерево решений. Какие линзы надо носить при предстарческой дальнозоркости, 
близорукости, при наличии астигматизма и сокращенной слезы?

## Задание 5

Постройте классификатор для обучающего множества Glass, данные которого характеризуются 10 признаками:
1. Id number: 1 to 214
2. RI: показатель преломления
3. Na: сода (процент содержания в соответствующем оксиде)
4. Mg
5. Al
6. Si
7. K
8. Ca
9. Ba
10. Fe

Классы характеризуют тип стекла:
- (1) окна зданий, плавильная обработка
- (2) окна зданий, не плавильная обработка
- (3) автомобильные окна, плавильная обработка
- (4) автомобильные окна, не плавильная обработка (нет в базе)
- (5) контейнеры
- (6) посуда
- (7) фары

Посмотрите заголовки признаков и классов. Перед построением классификатора необходимо также удалить первый признак Id number, который не несет никакой информационной нагрузки. Это выполняется командой:
```r
glass <- glass[,-1]
```
Постройте графики зависимости ошибки классификации от значения k и от типа ядра. 
Исследуйте, как тип метрики расстояния (параметр distance) влияет на точность классификации.
Определите, к какому типу стекла относится экземпляр с характеристиками:
- RI = 1.516 
- Na = 11.7 
- Mg = 1.01
-  Al = 1.19
-  Si = 72.59 
- K = 0.43 
- Ca = 11.44 
- Ba = 0.02 
- Fe = 0.1

Определите, какой из признаков оказывает наименьшее влияние на определение класса путем 
последовательного исключения каждого признака.


## Задание 6
Разработать классификатор на основе дерева решений для данных Титаник (Titanic dataset) - https://www.kaggle.com/c/titanic

## Решение

- **Деревья_решений.pdf**: Документ, содержащий подробное описание и пошаговые комментарии к решению задач.

## Автор
Шаронов Артем
