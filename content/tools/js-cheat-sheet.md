---
title: "JS Cheatsheet"
lastmod: 2019-10-24T15:23:17-04:00
draft: false
menu:
  main:
    identifier: "js-cheatsheet"
    parent: "Tools"
    weight: 10
---

Jquery and Vanilla JS equivalents:

| Task                       | jQuery                                               | "Vanilla" JS                                                                          |
|----------------------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Get all matching elements  | `$('selector')`                                      | `document.querySelectorAll('selector')`                                               |
| Get first matching element | `$('selector').first()`                              | `document.querySelector('selector')`                                                  |
| Change CSS prop            | `$('selector').css('property-name', 'value')`        | `document.querySelector('selector').style.property-name = 'value'`                    |
|                            |                                                      | `const matches = document.querySelectorAll('selector')`                               |
|                            |                                                      | `for (const m of matches) {m.style.property-name='value'`                             |
| Change Text Value          | `$('selector').text('new text here')`                | `document.querySelector('selector').textContent = 'new text here'`                    |
|                            |                                                      | `const matches = document.querySelectorAll('selector')`                               |
|                            |                                                      | `for (const m of matches) {m.textContent ='new text here'`                            |
| Set inner HTML             | `$('selector').html('<tag>valid HTML here</tag>')`   | `document.querySelector('selector').innerHTML = '<tag>valid HTML here</tag>'`         |
|                            |                                                      | `const matches = document.querySelectorAll('selector')`                               |
|                            |                                                      | `for (const m of matches) {m.textContent ='<tag>valid HTML here</tag>'`               |
| Append to an element       | `$('selector').append('<tag>valid HTML here</tag>')` | `document.querySelector('selector').innerHTML += '<tag>valid HTML here</tag>'` risky! |
| Remove a node              | `$('selector').remove()`                             | `let el = document.querySelector('selector'); el.parentNode.removeChild(el);`         |
