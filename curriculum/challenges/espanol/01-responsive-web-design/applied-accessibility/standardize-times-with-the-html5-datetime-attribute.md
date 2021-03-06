---
id: 587d778c367417b2b2512aa9
title: Estandariza horas con el atributo HTML5 datetime
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMgtz'
forumTopicId: 301025
dashedName: standardize-times-with-the-html5-datetime-attribute
---

# --description--

Continuando con el tema de fechas, HTML5 también introdujo el elemento `time` junto con un atributo `datetime` para estandarizar las horas. Este es un elemento inline que puede ajustar una fecha u hora en una página. Un formato válido de esa fecha se mantiene mediante el atributo `datetime`. Este es el valor al que acceden los dispositivos de asistencia. Ayuda a evitar confusiones al indicar una versión estandarizada de una hora, incluso si está escrito de manera informal o coloquial en el texto.

Aquí hay un ejemplo:

`<p>Master Camper Cat officiated the cage match between Goro and Scorpion <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.</p>`

# --instructions--

¡Ya tenemos los resultados de la encuesta de Mortal Kombat de Camper Cat! Envuelva una etiqueta `time` alrededor del texto `Thursday, September 15<sup>th<sup>` y agregue un atributo `datetime` establecido en `2016-09-15`.

# --hints--

Tu código debe tener un elemento `p` que incluya el texto `Thank you to everyone for responding to Master Camper Cat's survey.` e incluye un elemento `time`.

```js
assert(timeElement.length);
```

Las etiquetas `time` añadidas deben envolver el texto `Thursday, September 15<sup>th</sup>`.

```js
assert(
  timeElement.length &&
    $(timeElement).html().trim() === 'Thursday, September 15<sup>th</sup>'
);
```

Tu etiqueta `time` agregada debe tener un atributo `datetime` que no esté vacío.

```js
assert(datetimeAttr && datetimeAttr.length);
```

Tu atributo `datetime` agregado debe establecerse en un valor de `2016-09-15`.

```js
assert(datetimeAttr === '2016-09-15');
```

# --seed--

## --after-user-code--

```html
<script>
const pElement = $("article > p")
  .filter((_, elem) => $(elem).text().includes("Thank you to everyone for responding to Master Camper Cat's survey."));
const timeElement = pElement[0] ? $(pElement[0]).find("time") : null;
const datetimeAttr = $(timeElement).attr("datetime");
</script>
```

## --seed-contents--

```html
<body>
  <header>
    <h1>Tournaments</h1>
  </header>
  <article>
    <h2>Mortal Kombat Tournament Survey Results</h2>

    <!-- Only change code below this line -->

    <p>Thank you to everyone for responding to Master Camper Cat's survey. The best day to host the vaunted Mortal Kombat tournament is Thursday, September 15<sup>th</sup>. May the best ninja win!</p>

    <!-- Only change code above this line -->

    <section>
      <h3>Comments:</h3>
      <article>
        <p>Posted by: Sub-Zero on <time datetime="2016-08-13T20:01Z">August 13<sup>th</sup></time></p>
        <p>Johnny Cage better be there, I'll finish him!</p>
      </article>
      <article>
        <p>Posted by: Doge on <time datetime="2016-08-15T08:12Z">August 15<sup>th</sup></time></p>
        <p>Wow, much combat, so mortal.</p>
      </article>
      <article>
        <p>Posted by: The Grim Reaper on <time datetime="2016-08-16T00:00Z">August 16<sup>th</sup></time></p>
        <p>Looks like I'll be busy that day.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Tournaments</h1>
  </header>
  <article>
    <h2>Mortal Kombat Tournament Survey Results</h2>

    <p>Thank you to everyone for responding to Master Camper Cat's survey. The best day to host the vaunted Mortal Kombat tournament is <time datetime="2016-09-15">Thursday, September 15<sup>th</sup></time>. May the best ninja win!</p>

    <section>
      <h3>Comments:</h3>
      <article>
        <p>Posted by: Sub-Zero on <time datetime="2016-08-13T20:01Z">August 13<sup>th</sup></time></p>
        <p>Johnny Cage better be there, I'll finish him!</p>
      </article>
      <article>
        <p>Posted by: Doge on <time datetime="2016-08-15T08:12Z">August 15<sup>th</sup></time></p>
        <p>Wow, much combat, so mortal.</p>
      </article>
      <article>
        <p>Posted by: The Grim Reaper on <time datetime="2016-08-16T00:00Z">August 16<sup>th</sup></time></p>
        <p>Looks like I'll be busy that day.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
