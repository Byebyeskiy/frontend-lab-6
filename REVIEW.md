# Challenge 8 — CSS Debugging

| Проблема | Причина | CSS-властивість | Виправлення |
|---|---|---|---|
| Horizontal overflow | Фіксована ширина сторінки 1200px | width | Адаптивна ширина та Grid з minmax(0,1fr) |
| Heading overflow | Заборона переносу і 64px | white-space, font-size | Прибрати nowrap, clamp(), overflow-wrap |
| Card overflow | Картки по 350px в одному flex-рядку | width, display | auto-fit Grid, minmax(min(100%,220px),1fr) |
| Sidebar too wide | Фіксовані 300px при вузькому viewport | grid-template-columns | Адаптивна сітка і один стовпець на mobile |

# Challenge 9 — AI review

Початковий приклад CSS з умови збережений у `initial-ai.css`. Порівняння з `style.css`:
| Рекомендація | Прийнята? | Перевірка | Обґрунтування |
|---|---|---|---|
| Замінити фіксовану ширину page | Так | MDN CSS grid layout | Уникнення overflow |
| Використати auto-fit + minmax | Так | MDN repeat() | Автоматична кількість колонок |
| Прибрати nowrap з h1 | Так | MDN white-space | Заголовок переноситься |
| Застосувати container query для картки | Так | MDN CSS container queries | Незалежність від viewport |

Посилання для перевірки: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout ; https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_size_and_style_queries ; https://developer.mozilla.org/en-US/docs/Web/CSS/clamp

Примітка: це огляд згенерованого коду; фактичні вимірювання в DevTools студент має виконати у браузері.
