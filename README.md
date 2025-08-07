# install_holehe_termux
Ось **покрокова інструкція**, як правильно встановити 🕵️‍♂️ **`holehe`** у **Termux** на Android:

---

## ✅ КРОК 1: Оновлення системи

```bash
pkg update && pkg upgrade -y
```

---

## ✅ КРОК 2: Встановлення Python та pip

```bash
pkg install python -y
```

---

## ✅ КРОК 3: Встановлення `git` та `pipx` (рекомендовано)

```bash
pkg install git -y
pip install pipx
pipx ensurepath
```

🔁 Після цього закрий Termux і відкрий знову, щоб оновився `$PATH`.

---

## ✅ КРОК 4: Встановлення `holehe`

Використовуй `pipx` (безпечніше, ніж просто `pip install`):

```bash
pipx install holehe
```

---

## 🔍 Альтернатива без pipx (якщо не хочеш)

```bash
pip install holehe
```

Тоді запуск буде так:

```bash
python3 -m holehe ...
```

або

```bash
~/.local/bin/holehe ...
```

---

## ✅ КРОК 5: Перевірка встановлення

```bash
holehe --help
```

---

## ⚠️ Додатково: Установка `proot` (якщо хочеш запускати з `proot -0`)

```bash
pkg install proot -y
```

---

## 🛡️ Примітка з безпеки:

* `holehe` **не ламає акаунти** — він просто перевіряє, чи **існує акаунт** на публічних сайтах.
* Він **відправляє запити** до сайтів, тому не зловживай, щоб уникнути бану IP.

---

## 📌 Приклад запуску:

```bash
holehe -NP --only-used example@gmail.com
```

або з `proot`:

```bash
proot -0 holehe -NP --only-used example@gmail.com
```

---

🔧 Хочеш, можу зробити скрипт-автоматизатор встановлення `holehe` у Termux?
