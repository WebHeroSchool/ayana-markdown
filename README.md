## 1. Избегайте глобальных переменных :blush:
- ##### Используйте замыкания
 
:thumbsdown: Плохой пример:  
```
  let a = 9; 
  function func() {
  return a
  }
```
:thumbsup: Хороший пример:
```  
  function func() {
    let a = 5; 
  function func1() { 
     let b = 8; 
     } }
```
---
## 2. Всегда объявлять локальные переменные :blush:
- ##### Используйте ключевые слова let и const
:thumbsdown: Плохой пример:  
```
function func() {
  a = 9;
}
```
:thumbsup: Хороший пример:
```  
function func(){
let a = 10; 
}
```
---
## 3. Используйте === Сравнение :blush: 
- ##### Оператор == cравнение всегда преобразуется перед сравнением
- ##### Оператор === сравнивает значения и тип

:thumbsdown: Плохой пример:  
```
0 == '';
```
:thumbsup: Хороший пример:
```  
let 0 ==='';
```
---
## 4. Избегайте использовать eval() :blush: 
- ##### В 99% случаев можно избежать использования eval()

:thumbsdown: Плохой пример:  
```
console.log(eval('2 + 2'));
```
:thumbsup: Хороший пример:
```  
console.log(2 + 2);
```
---
## 5. Объявляйте переменные снаружи от цикла For :blush: 
- ##### При выполнении длинных циклов «for» не создавайте дополнительной нагрузки на движок. 

:thumbsdown: Плохой пример:  
```
for(var i = 0; i < someArray.length; i++) {
    var container = document.getElementById('container');
    container.innerHtml += 'my number: ' + i;
    console.log(i);
 }
```
:thumbsup: Хороший пример:
```  
var container = document.getElementById('container');
 for(var i = 0, len = someArray.length; i < len;  i++) {
    container.innerHtml += 'my number: ' + i;
    console.log(i);
 }
```
---
## 6. Комментируйте свой код :blush: 
- ##### Поначалу может показаться, что в этом нет необходимости, но поверьте мне, вам следует комментировать ваш код насколько это возможно. Что произойдет, когда вы вернетесь к вашему проекту через несколько месяцев, – только то, что вы поймете: не так-то просто вспомнить ход собственной мысли. Или что если одному из ваших коллег необходимо будет внести изменения в ваш код? Всегда, всегда комментируйте важные части вашего кода.

:thumbsup: Хороший пример:
```  
// Cycle through array and echo out each name. 
 for(var i = 0, len = array.length; i < len; i++) {
    console.log(array[i]);
 }
```
---
## 7. Не передавайте строку в "SetInterval" или "SetTimeOut" :blush: 
- ##### Код в первом примере не только неэффективен, но и ведет себя таким же образом, как и вела бы себя функция "eval". Никогда не передавайте строку в "SetInterval" или "SetTimeOut". Вместо этого передавайте имя функции.

:thumbsdown: Плохой пример:  
```
setInterval(
 "document.getElementById('container').innerHTML += 'My new number: ' + i", 3000
 );
```
:thumbsup: Хороший пример:
```  
setInterval(someFunction, 3000);
```
---
## 8.  Всегда, всегда используйте точки с запятой (;) :blush: 
- ##### Технически в большинстве браузеров опускание «;» сойдет вам с рук.
- ##### Тем не менее, это очень плохая практика, в результате использования которой потенциально могут возникнуть гораздо более крупные и тяжелые для обнаружения проблемы.
:thumbsdown: Плохой пример:  
```
let someItem = 'some string'
 function doSomething() {
   return 'something'
 }
```
:thumbsup: Хороший пример:
```  
let someItem = 'some string';
 function doSomething() {
   return 'something';
 }
```
---
## 9. Уберите атрибут "language" :blush: 
- ##### Много лет тому назад вполне можно было встретить атрибут "language" внутри тегов script.
Однако, уже давно с тех пор этот атрибут считается устаревшим, так что забудьте о нем.

:thumbsdown: Плохой пример:  
```
<script type="text/javascript" language="javascript">
 ...
 </script>
```
:thumbsup: Хороший пример:
```  
<script type="text/javascript">
 ...
 </script>
```
---
## 10. Используйте {} вместо New Object() :blush: 
- ##### Имеется множество способов создания объектов в JavaScript. Вероятно, более традиционным способом является использование конструктора «new».
- ##### Однако, этот способ зарекомендовал себя как «плохую практику» без должных на то оснований. Вместо этого я вам рекомендую использовать более надежный способ создания объектов – при помощи литерала (* литеральная (символьная) константа).

:thumbsdown: Плохой пример:  
```
let o = new Object();
 o.name = 'Jeffrey';
 o.lastName = 'Way';
 o.someFunction = function() {
    console.log(this.name);
 }
```
:thumbsup: Хороший пример:
```  
let o = {
    name: 'Jeffrey',
    lastName = 'Way',
    someFunction : function() {
       console.log(this.name);
    }
 };
```
---
