# HTML-Seninar_16
Задание 1 (тайминг 20 минут)
1. При наведении на любую ссылку цвет текста должен стать красным
2. При нажатии на ссылку цвет текста должен стать зеленым в момент нажатия
3. Найти первый элемент списка и добавить нижнее подчеркивание ссылке
4. Найти последний элемент списка и добавить ссылке жирность font-weight: bold
5. У третьей ссылки нужно поменять цвет фона на оранжевый Сокращенный набор кода
 
1. При наведении на любую ссылку цвет текста должен стать красным
.menu__link:hover {
    color: red;
}

2. При нажатии на ссылку цвет текста должен стать зеленым в момент нажатия
.menu__link:active {
    color: green;
}

3. Найти первый элемент списка и убрать нижнее подчеркивание ссылке
.menu__list:first-child .menu__link {
    text-decoration: none;
}

4. Найти последний элемент списка и добавить ссылке жирность font-weight: bold
.menu__list:last-child .menu__link {
    font-weight: bold;
}

5. У третьей ссылки нужно поменять цвет фона на оранжевый 
.menu__list:nth-child(3) .menu__link {
    background-color: orange;
}


Задание 2 (тайминг 20 минут)
1. Дан код https://codepen.io/alexej-kadochnikow/pen/RwQrvov
2. Необходимо создать псевдоэлемент new
3. Разместить его в правом верхнем углу блока product чтобы он не смещал другие элементы
4. Размеры блока 35 на 35 px
5. цвет фона красный, а цвет текста белый
6. Необходимо создать псевдоэлемент sale
7. Разместить его в левом верхнем углу блока product чтобы он не смещал другие элементы
8. размеры блока 35 на 35 px
9. цвет фона оранжевый, а цвет текста белый

Исходный код:

 <div class="product">
   <div class="product__img"></div>
   <h2 class="product__name">Name product</h2>
   <p class="product__text">Lorem ipsum dolor sit amet consectetur adipisicing.</p>
 </div>

Доббавлянем дочерний класс product_new 

 <div class="product product_new">
   <div class="product__img"></div>
   <h2 class="product__name">Name product</h2>
   <p class="product__text">Lorem ipsum dolor sit amet consectetur adipisicing.</p>
 </div>

CSS:
Исходный код 

.product {
  width: 250px;
  padding: 24px;
  border: 1px solid #000;
}

.product__img {
  background-color: forestgreen;
  height: 150px;
}

.product::after {
  content: 'new';
}

.product::before {
  content: 'sale';
}

После решения задачи

.product {
  width: 250px;
  padding: 24px;
  border: 1px solid #000;
  position: relative: - добавили
}

.product__img {
  background-color: forestgreen;
  height: 150px;
}

.product_new::after {
    position: absolute;
    top: 8px;
    right: 8px;
    content: 'new';
    width: 36px;
    height: 36px;
    background-color: darkred;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .product_sale::before {
    position: absolute;
    top: 8px;
    left: 8px;
    content: 'sale';
    width: 36px;
    height: 36px;
    background-color: orange;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
  }

Задание 3 (тайминг 10 минут)

1. Скопировать любой код svg с сайта https://fontawesome.com/
--- заходим на сайт - поиск - vk - нажимаем на значек - нажимаем Copy Code Snippetвкладку svg - копируем код svg - вставляем после "icons">
Задаем значение ширины после svg -> svg width="30"

Создаем блок icons

2. Необходимо добавить эффект наведения на картинку и поменять значение цвета на 
purple при наведении и yellow при нажатии

Смотри код семинар 16

Задание 4 (тайминг 20 минут)
1. Дан код https://codepen.io/alexej-kadochnikow/pen/yLveZbg
2. Необходимо добавить
   
a. При наведении на первый блок, чтобы он смещался на 50px вправо

b. при наведении на второй блок, он должен становиться в 2 раза больше

c. При наведении на 3 блок, он должен повернуться по часовой стрелке на 60 градусов

d. Все наведения должны быть плавными и выполнять переход за 1 секунду

e. Можно менять параметры ширины и высоты при необходимости

.item {
    width: 150px;
    height: 86px;
    background-color: forestgreen;
    border: 1px solid #000;
    transition: transform 1s;
  }
  
  .item_1:hover {
    transform: translateX(50px);
  }

  .item_2:hover {
    transform: scale(2);
  }

  .item_3:hover {
    transform: rotate(60deg);
  }

Задание 5 (тайминг 20 минут)

1. Дан код https://codepen.io/alexej-kadochnikow/pen/MWQKLop
2. Есть 4 блока, вам необходимо сделать 8 угольник 
3. Для этого вам необходимо подобрать значение высоты
4. Задать значение фона для блоков
5. Подобрать верный угол поворота
.content2 {
    margin-top: 200px;
    margin-left: 200px;
    padding-bottom: 200px;
    position: relative;
  }  
  .iteml {
    position: absolute;
    width: 150px;
    height: 62px;
    border: 1px solid #000;
    background-color: forestgreen;
  }
  .iteml_1 {
    transform: rotate(45deg);
  }
  .iteml_2 {
    transform: rotate(90deg);
  }
  .iteml_3 {
    transform: rotate(135deg);
  }

Задание 6 (тайминг 10 минут)

1. Дан код https://codepen.io/alexej-kadochnikow/pen/GRQozvb
2. Необходимо добавить произвольную анимацию на кнопку для этого можно 
использовать генератор или придумать анимацию самостоятельно 
https://animista.net/play/basic/rotate-scale  , если необходимо быстро определиться 
https://animista.net/play/attention/wobble

Заходим на страницу произвольной анимации - выбираем анимацию (ATTENTION - BOUNCE)
Нажимаем верхний правый угол - Generate Code - нажимаем Copy KeyFrames - добавляем в верхней части css
В css button добавляем строку animation: bounce-top 0.9s both;
@-webkit-keyframes bounce-top {
    0% {
      -webkit-transform: translateY(-45px);
              transform: translateY(-45px);
      -webkit-animation-timing-function: ease-in;
              animation-timing-function: ease-in;
      opacity: 1;
    }
----------------------------------------------------------------------------- далее длинный код
  .button {
    animation: bounce-top 0.9s both;
    width: 150px;
    height: 50px;
    background-color: purple;
    color: white;
    text-align: center;
    line-height: 50px;
    font-family: sans-serif;
    font-size: 18px;
  }

