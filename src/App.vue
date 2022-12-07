<template>

  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <header>
      <section>
        <article>
          <searchStr class="search" />
        </article>
        <article class="filterImg">
          <svg width="100" height="100" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink">
            <rect width="100" height="100" fill="url(#pattern0)" />
            <defs>
              <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                <use xlink:href="#image0_103_41" transform="scale(0.00195312)" />
              </pattern>
              <image id="image0_103_41" width="512" height="512"
                xlink:href="data:image/png;base64,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" />
            </defs>
          </svg>

        </article>
      </section>

    </header>
    <main>
    </main>
    <footer>
      <section>
        <article class="calendImg">
          <svg width="48" height="48" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink">
            <rect width="100" height="100" fill="url(#pattern0)" />
            <defs>
              <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                <use xlink:href="#image0_97_5" transform="scale(0.02)" />
              </pattern>
              <image id="image0_97_5" width="48" height="48"
                xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAABmJLR0QA/wD/AP+gvaeTAAADVUlEQVRoge2ZT2hcVRTGf9+bSYSaleSlMYoaWxfa7goRum+LCCYqBTdVwdKNirRJixRJbpOFVYOKUAqlUurWgqQgQnXpH6S4TCsUQakEzes2WSSZ+7mYSUzGyZ+pIe8lzG/13nnnu5xv7txzHjPQokWLFtsJrbgLbu90HJN0DPNwTjWtxxT4i0zJCEFzi8Hy8oyUOAo6g7e+uiboAb2bEp3B2cXgCiNYxwAUdXB6TD9tdOV0JBogO5dovdz/q+sKPmj7B6zXWGYkqcvrAWjGxFYzHfRj7bJnebzeyLalZaRotIwUjRVtb7EdbheWt+0dsyPlRsGtGGyboVvOjtmRlpGi0TJSNHaMkdZALBqtgVg0WkaKRsMzkhsn3JZ2MyDFAUsHgEepfth/Yf8sJ9emEybwf5trYYx0BQ/Y/gjYa0Tdb2u9oF7Lr6TwWyN9Ib5aaaict/0VsNdi0tLJUtT+ZEYdyYw6SlH7bZ0S3MLsWRIGL9VfmIEomLM0mE1ykS9VaZh01KV0H2+CxzFtyO9noXS2pv+XvIwI5iQ9/3fQd43qqZ8zXcM+5MRfY9os9d8Lup7fQAwup/hXzB5Lg9N1JtZielTfpsM+jfyp8Dgn/E1uZySFgaoJJrNJLjarzxIuIG5jnurq5oX8Drvjy9ULXV71TKxF0ILRZQCS+GJ+RqRnASLcuN8lSjWtrQM57kj1j6RklruNHj8U/Mx6S1Rm+QMA8Uiec2RutQdp8Osl+yaA4NZGFsvNiOBPgPIDPLYY2z3kB9ORylXsK8Au5KuaUd9qa5R28Xjtcqph+73fedKMbjFxQRwGJgFiB89hvQrMYr2VnUuurLVGJXJEAts363fk+2YK3wwS+ThHXQLIgq5JHitF9WWjWtMEwWXJxwGkZKKpwbepBLen9m3gSaR3sqDPmpF3Dvuk5I8Rd7Ip7cvvsAfNJdap6o3Hu4Z9aKPSruDDSvwBxkZDXNJ8fjuyVFRl3NYgYp6o01nCBYIWGiYHlzsjb9dMrP7SmA9W50j8UGgIqu02Sp+X4EaE3wESeKISOaLEb2CexpjE5zOS9wiKNV0x2D3s/pj4E0zvmonijtHQvaDrK8NFIrg9jfSj+BKoD+gGIuKu7V+kZCKbYoJLmq+X/gOsrGMYTHorjgAAAABJRU5ErkJggg==" />
            </defs>
          </svg>

        </article>
        <article class="optionsImg">
          <svg width="100" height="100" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink">
            <rect width="100" height="100" fill="url(#pattern0)" />
            <defs>
              <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                <use xlink:href="#image0_54_12" transform="scale(0.02)" />
              </pattern>
              <image id="image0_54_12" width="50" height="50"
                xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAAABmJLR0QA/wD/AP+gvaeTAAAEh0lEQVRoge3aS6iVVRQH8M+rXTPNRIp8EBkVhCSaJSWaUoOMil5qD4goqAiVaFAJTe3hoCCchIOwQQ/oMatoYhGVCpmRpvlII6VRRKjX0lJ/Dfb6Ovt83nPvOddzzm1w/3A537f2f6+91n6svff6blGMYAQjGBJwBzaiz/DjqGTL7a068cIwGz4Q1rQyEnAcz2DqUEa0ncBUPBs20czI4LMgP9MFG1sCngvbNjZDPhrkKV2wrSVgSth2pBkyaEOj9+OvbG7/gXlt0NuvfT1nq3gAPFgUxbnZ+6SiKO7uVGOddGRu/F5VFMWyeJ7dwfbq0ezUwky8jCv6KbuwnMvowZXxfqiBrqV4HdPaZV9TRMzGb0H9E6sxOitfEmVfxHtPFkQuzHgX4/1sHe3F9K44gqszJ37KjNiM6/EU9oXstaze5pDtwJN4BL+H7DB+jOfduKgbjrwRlG/Ri9twyJnYiVlZvVszY3N8jEuk6Vgehx7thiM34bS0y84M2QVYjxN4Dw0XNebhIxzEw5l8VTT9KyZ13JHgrA/aJvVrY/RA9QbQN0NtDd11tvY1TcTE6FF4ukW7+9P3aeh6tx32tUTEfUE9I6RKa2cVtsS875MW+0r0VriXh56TuHg4HHk+qBsq8mn4TmNsk+0XUmj+PsqWdM0RjMW1+EVa9JdXyraVI4VlOD/+7sGeKPs2Hxk8EPLPpRA+riOO4E68Le0B/2S9u6XCKyPPIUzuR/dktVC9MpOPV1vsoo3vsQFL2+nIsayRk9iFdzC3wtsSnGVFA2B5cDZX5LfgTWyvdNaJdjpS4rpBhr3s1fMH4EwMTsM7BcZJU6yhLdU6rZ5+JxVF0dCRoiiauceMaoIzriiKhp3RFBr0whH1+BkfYnGFV06tewfQvzQ4myryRfgAByptHR7MvlYcWYR1+Ep9emh/hbcy5Hs0Xux7g7Mik4/C/kxvX7S1Dova5kilfLR0F9ke1Buysl714Xe5tCYmxkiUTmzFOVm9+SHfHrobHnXa5kjGezyoH1Xk06R9ohG2qqSYpEMkPNEu+1px5KagHkNPpaxXmmabpEh2FF9jRT4Swe1RC+83d9URaQf/IajNZf4G1ldmNnfj3EG4bXWkbHgnxmbyMS0YPyZ7HittsvDi2drXFBFz8Le0w88P2Xl4VbpYfVLKG9SfL90KT+AVscGG/JS0q8/phiNrg7IPE7BY7Y6eYz8WZPUWqA+xJfZK4X18pmdtNxyZoXapOiCdgEmHvAV4TC00v5XVeytkO6SIt1Dt+H46c/IgZnTckeBcKu3upGm2Vv2xfG6U7cpkZeLhmkw2RkollVn2Q/rJk3XMkeDNwEuyTElW1iutgVPS9JsQzydUbojBnxW6LmuXfc0TB9dTbooLcWM8b22D3n7tazpcDgHbipT//bIi6wg6mcR+ryiKvuy9ryiK9zvYXj3UjuzD/smtCkwP2w5Xy/obkW/i96HOmjUklDYNvtZwe3h9XPpmN2iqv9OQTtSrI+rR7GdqrPH/RWuHVGlkNqpP0wwXhvYPAyMYwQj+w7/zogR4Ax7DWgAAAABJRU5ErkJggg==" />
            </defs>
          </svg>

        </article>
      </section>
    </footer>
  </body>
</template>

<script>
import blueBlock from '@/components/blueBlock.vue'
import searchStr from '@/components/search'
import svgfilgImage from '@/assets/images/SVG/filter.svg'
import svgfilgImage2 from '@/assets/images/SVG/calend.svg'
import pngfilgImage from '@/assets/images/PNG/options.png'
export default {
  name: 'App',
  components: {
    searchStr,
    blueBlock,
    svgfilgImage,
    svgfilgImage2
  }
}
</script>

<style scoped>
body {
  background: #343434;
  margin: 0;
}

/* * {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
} */

header,
footer {
  margin: 0;
  position: absolute;
  width: 100%;
  background: #232323;
}

header {
  height: 100px;
  padding: 0 8px;
}

footer {
  height: 100px;
  bottom: 0;
}

main {
  flex-grow: 1;
}


.search {
  position: fixed;
  margin-top: 1vh;
}

.filterImg {
  position: absolute;
  top: 35%;
  left: 88%;
}

.calendImg {
  position: absolute;
  left: 8%;
  bottom: 35%;
}

.optionsImg {
  position: absolute;
  left: 88%;
  bottom: 35%;
}



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
