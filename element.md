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

<div style="border: 1px solid #ddd; padding: 20px; border-radius: 8px; background: #f9f9f9; font-family: Arial, sans-serif;">
  <h3 style="color: #333; margin-top: 0; margin-bottom: 15px;">🧬 Анатомия HTML-элемента (все в одной строке)</h3>

  <div style="background: white; padding: 15px; border-radius: 5px; font-family: 'Courier New', monospace; border-left: 4px solid #4CAF50;">
    <span style="color: #d14;">&lt;button</span> 
    <span style="color: #099;">class</span>=<span style="color: #c00;">"order-btn special-btn"</span>
    <span style="color: #099;"> data-id</span>=<span style="color: #c00;">"promo-2"</span><span style="color: #d14;">&gt;</span>
    <span style="color: #333;">Заказать</span>
    <span style="color: #d14;">&lt;/button&gt;</span>
  </div>

  <div style="margin-top: 15px; padding: 10px; background: #e8f4f8; border-radius: 5px;">
    <div style="display: flex; align-items: center; margin-bottom: 8px;">
      <div style="width: 120px; font-weight: bold;">Имя тега:</div>
      <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">button</div>
    </div>

    <div style="display: flex; align-items: center; margin-bottom: 8px;">
      <div style="width: 120px; font-weight: bold;">Атрибуты:</div>
      <div style="flex: 1;">
        <div style="display: inline-block; margin-right: 15px;">
          <div style="font-size: 0.9em; color: #666;">имя</div>
          <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">class</div>
        </div>
        <div style="display: inline-block;">
          <div style="font-size: 0.9em; color: #666;">значение</div>
          <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">"order-btn special-btn"</div>
        </div>
      </div>
    </div>
    
    <div style="display: flex; align-items: center; margin-bottom: 8px;">
      <div style="width: 120px; font-weight: bold;">Атрибуты:</div>
      <div style="flex: 1;">
        <div style="display: inline-block; margin-right: 15px;">
          <div style="font-size: 0.9em; color: #666;">имя</div>
          <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">data-id</div>
        </div>
        <div style="display: inline-block;">
          <div style="font-size: 0.9em; color: #666;">значение</div>
          <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">"promo-2"</div>
        </div>
      </div>
    </div>
    
    <div style="display: flex; align-items: center;">
      <div style="width: 120px; font-weight: bold;">Текст кнопки:</div>
      <div style="background: white; padding: 3px 8px; border-radius: 3px; border: 1px solid #ccc;">Заказать</div>
    </div>
  </div>

  <div style="margin-top: 15px; font-size: 0.9em; color: #666; padding: 8px; background: #fff3cd; border-radius: 5px; border-left: 4px solid #ffc107;">
    💡 <strong>Структура:</strong> &lt;<em>имя_тега</em> <em>атрибут="значение"</em> <em>атрибут="значение"</em>&gt;<em>текст</em>&lt;/<em>имя_тега</em>&gt;
  </div>
</div>