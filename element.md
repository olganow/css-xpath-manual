[< Главная страница](README.md) 

# 📋 XPath и CSS-селекторы - общая информация

## Содержание

1. [Общая информация](#1-общая-информация)
2. [Строение HTML элемента](#2-строение-html-элемента)


## 1. Что такое CSS Selectors и XPath?

CSS Selectors и XPath— это разные способы для нахождения элементов в HTML документе: это конкретная строка-запрос. В случае CSS — селектор включает в себя набор уникальных атрибутов элемента, а в случае XPath — это гибкий способ адресации в XML документе, а также путь по DOM’у к элементу на HTML странице

Локатор — это общее понятие, описывающее способ нахождения элемента на странице, он может включать методы для работы с элементами, в то время как селектор лишь указывает на объект.

CSS (англ. Cascading Style Sheets, «каскадные таблицы стилей») изначально создавался как язык стилей, с помощью которого применяют оформление к веб-странице, но его селекторы также используются для выбора элементов по:
•	Тегу (div, p)
•	Классу (.class)
•	Идентификатору (#id)
•	Атрибутам ([type="text"])
•	Иерархии вниз (пробел, >, +, ~)

XPath (XML Path Language) — язык запросов для навигации и поиска информации в XML-документах (и HTML как частным случаем). Он позволяет искать элементы:
•	Тегу (div, p)
•	Классу ([@class])
•	Атрибутам ([@type="text"])
•	Сложным условиям
•	Перемещаться по дереву документа (вверх, вбок, вниз)
•	Использовать функции (поиск по тексту, позиции, условиям)

Особенность XPath - это оси. Оси (axes) в XPath - это одна из самых мощных особенностей, которая делает его гораздо более гибким, чем CSS-селекторы.
Оси - это направления навигации по дереву документа (DOM) относительно выбранного контекстного узла (текущего элемента). Проще говоря, это способы "смотреть" в разные стороны от элемента: к родителям, детям, соседям и т.д.
В то время как CSS-селекторы могут двигаться в основном вниз (от родителя к ребёнку), XPath позволяет двигаться в любом направлении.

CSS - лаконичный и быстрый, идеален для простых селекторов
XPath - мощный и гибкий, незаменим для сложной навигации и поиска


## 2. Строение HTML элемента
Элемент состоит из имени, то есть самого HTML-тега. Например, div, span, input, button и другие. Внутри него перечислены атрибуты, которые отвечают за все возможные свойства элемента. Например, цвет, размер, действие, которое будет происходить по клику на элемент.
HTML-тега.


<div style="border: 1px solid #ddd; padding: 20px; border-radius: 8px; background: #f9f9f9;">
  <h3 style="color: #333; margin-top: 0;">🧬 Разбор HTML-элемента</h3>
  
  <div style="background: white; padding: 15px; border-radius: 5px; font-family: monospace;">
    &lt;<span style="color: #d14;">button</span> 
    <span style="color: #099;" title="имя атрибута">class</span>="<span style="color: #c00;" title="значение атрибута">order-btn special-btn</span>"
    <span style="color: #099;" title="имя атрибута">data-id</span>="<span style="color: #c00;" title="значение атрибута">promo-2</span>"&gt;
    <br>
    &nbsp;&nbsp;<span style="color: #333;" title="текст кнопки">Заказать</span>
    <br>
    &lt;/<span style="color: #d14;">button</span>&gt;
  </div>
  
  <table style="width: 100%; margin-top: 15px; border-collapse: collapse;">
    <tr style="background: #e8f4f8;">
      <th style="padding: 8px; text-align: left;">Компонент</th>
      <th style="padding: 8px; text-align: left;">Значение</th>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Имя тега</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>button</code></td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Атрибут 1 (имя)</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>class</code></td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Атрибут 1 (значение)</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>"order-btn special-btn"</code></td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Атрибут 2 (имя)</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>data-id</code></td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Атрибут 2 (значение)</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>"promo-2"</code></td>
    </tr>
    <tr>
      <td style="padding: 8px; border: 1px solid #eee;">Текст кнопки</td>
      <td style="padding: 8px; border: 1px solid #eee;"><code>"Заказать"</code></td>
    </tr>
  </table>
</div>
