# Лабораторная работа №20:

## Основная информация

**ФИО:** Боровой Роман Николаевич, Соколов Вовчик Санекович, Андоюха Евгеха Медведович
**Группа:** ИСП-233  
**Дата:** 31.03.2026

---

## Описание (что изучили)

В ходе лабораторной работы были изучены основы работы с DOM и событиями в JavaScript:

- Научились работать с DOM-деревом;
- Освоили поиск HTML-элементов из JavaScript;
- Научились изменять содержимое страницы;
- Освоили обработку событий пользователя;
- Создали простой TODO-лист.

---

## Структура проекта

---lab20/

- dynamicElements.html
- dynamicElements.js
- index.html
- main.js
- README.md
- style.css

|      Концепция       |                C# (WinForms)                |                   JavaScript (DOM)                   |
| :------------------: | :-----------------------------------------: | :--------------------------------------------------: |
|    Найти элемент     | Button myButton = this.Controls["myButton"] | const myButton = document.getElementById("myButton") |
|    Изменить текст    |         label1.Text = "Новый текст"         |          label.textContent = "Новый текст"           |
| Добавить обработчик  |        button1.Click += HandleClick         |    button.addEventListener("click", handleClick)     |
|   Создать элемент    |          Button btn = new Button()          |     const btn = document.createElement("button")     |
| Добавить в контейнер |          panel1.Controls.Add(btn)           |                panel.appendChild(btn)                |
|    Скрыть элемент    |           button1.Visible = false           |            button.style.display = "none"             |

## Events в JS = События в C#

C# (WinForms):

```csharp
private void Button1_Click(object sender, EventArgs e)
{
    label1.Text = "Нажато!";
}
```

JavaScript (DOM):

```JavaScript
button.addEventListener("click", (e) => {
    label.textContent = "Нажато!";
});
```

## Валидация формы

C# (WinForms):

```csharp
private void SubmitButton_Click(object sender, EventArgs e)
{
    if (string.IsNullOrEmpty(nameTextBox.Text))
    {
        MassageBox.Show("Введите имя!");
        return;
    }
}
```

JavaScript (DOM):

```JavaScript
form.addEventListener("submit", (e) => {
    e.preventDefault();

    if (!nameInput.valve.trum()) {
        alert("Введите имя!");
        return;
    }
});
```

---

## Главные отличия:

|   Аспект    |    C# (WinForms)    |   JavaScript DOM    |
| :---------: | :-----------------: | :-----------------: |
| Компиляция  |         Да          | Нет (интерпретация) |
|  Типизация  |       Строгая       |    Динамическая     |
|   Ошибки    | Во время компиляции | Во время выполнения |
| UI-дизайнер |  Есть (визуальный)  |  Нет (только код)   |
|  Платформа  |       Windows       |    Любой браузер    |

**Преимущества DOM перед WinForms:**
* Кроссплатформенность (работает везде)
* Не нужна установка приложения
* Легко обновлять (обновил файлы — всё работает)
* Современные UI (CSS, анимации)

**Преимущества WinForms перед DOM:**
* Визуальный дизайнер (drag & drop)
* Ошибки на этапе компиляции
* Интеграция с Windows API
* Более понятная структура

**Вывод: DOM и WinForms решают схожие задачи, но разными подходами.**