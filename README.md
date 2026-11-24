# Экономика информатизации — решения экзаменационных задач

**Студент:** Солдатов Сергей Юрьевич, группа ПИ4-1

## О репозитории

Репозиторий содержит решения экзаменационных задач по курсу «Экономика информатизации».
Каждое решение оформлено как аналитическая записка в Jupyter Notebook: экономическая постановка,
исходные данные, математическая модель, расчет на Python, визуализация, интерпретация, выводы и рекомендации.

## Структура репозитория

- `notebooks/` — Jupyter Notebook с решениями задач
- `data/` — исходные данные для задач (в задачах 1–5 данные заданы в условии и записаны прямо в ноутбуках)
- `reports/` — экспортированные отчеты (HTML и PDF), графики (`figures/`) и итоговые показатели (`*_summary.json`)

## Установка и запуск

```bash
git clone https://github.com/Ranot27/economy-of-informatization-exam.git
cd economy-of-informatization-exam
python -m venv venv
source venv/bin/activate        # Linux/macOS
# venv\Scripts\activate         # Windows
pip install -r requirements.txt
jupyter lab
```

Ноутбуки запускаются из папки `notebooks/` командой «Run All Cells». Все исходные данные задачи лежат
в словаре `BASE` в начале ноутбука: достаточно изменить значение там, и расчет, таблицы и графики пересчитаются.

Экспорт отчета в HTML:

```bash
jupyter nbconvert --to html --output-dir reports notebooks/01_crm_efficiency.ipynb
```

## Список задач

| № | Лекция | Задача | Ноутбук | Отчет | Статус | Ключ зачета |
|---|---|---|---|---|---|---|
| 1 | 1 | Оценка экономической эффективности внедрения облачной CRM | [01_crm_efficiency.ipynb](notebooks/01_crm_efficiency.ipynb) | [HTML](reports/01_crm_efficiency.html), [PDF](reports/01_crm_efficiency.pdf) | Зачтено | `bb42a37308fb80bf6730ebcdc3f2abcb64001471a4204638b0d84485667cbe33` |
| 2 | 3 | Расчет критической массы и ценности социальной сети | [02_network_critical_mass.ipynb](notebooks/02_network_critical_mass.ipynb) | [HTML](reports/02_network_critical_mass.html), [PDF](reports/02_network_critical_mass.pdf) | Зачтено | `5c7a900623a1afdeb0da48f660eaef02021bcfad78dbe88e6c60fdf2648490ea` |
| 3 | 4 | Выбор ценовой стратегии для AI-сервиса по созданию контента | [03_ai_pricing_strategy.ipynb](notebooks/03_ai_pricing_strategy.ipynb) | [HTML](reports/03_ai_pricing_strategy.html), [PDF](reports/03_ai_pricing_strategy.pdf) | Зачтено | `ffc324f4d6562c634d93fdda817af9f1f5109ef2d2d1db064ce30c212f9cf7e4` |
| 4 | 5 | Оптимизация рекламной нагрузки для платформы видеоконтента | [04_ad_load_optimization.ipynb](notebooks/04_ad_load_optimization.ipynb) | [HTML](reports/04_ad_load_optimization.html), [PDF](reports/04_ad_load_optimization.pdf) | Выполнено | — |
| 5 | 6 | Расчет стоимости разработки по COCOMO II | [05_cocomo_cost.ipynb](notebooks/05_cocomo_cost.ipynb) | [HTML](reports/05_cocomo_cost.html), [PDF](reports/05_cocomo_cost.pdf) | Выполнено | — |

## Ключевые результаты

| Задача | Результат |
|---|---|
| 1. CRM | NPV = 11,94 млн руб., ROI = 553% (442% по чистой прибыли), окупаемость на 5-м месяце |
| 2. Соцсеть | Критическая масса 133 367 пользователей, достигается на 112-м месяце; NPV за 36 мес. = −60,10 млн руб. |
| 3. Ценовая стратегия | Выбрана подписка: ARPU 300 руб., LTV 6 000 руб., LTV/CAC от 4,0 до 60; NPV за 3 года = −50,07 млн руб. (все четыре стратегии убыточны при заданной базе) |
| 4. Рекламная нагрузка | Оптимальная рекламная нагрузка — 10 показов в день на пользователя, прибыль 1 530 млн руб.; ответ не меняется при CPM 10–30 руб. и при изменении оттока на ±20% |
| 5. COCOMO II | Размер — 19,44 тыс. строк кода, трудоемкость — 133,36 чел.-мес., длительность — 13,86 мес.; стоимость — 36,67 млн руб. без НДС и 44,01 млн руб. с НДС |
