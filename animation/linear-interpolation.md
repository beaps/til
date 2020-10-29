# Linear Interpolation

La `interpolación lineal` te permite obtener un valor entre dos valores conocidos (_start_ y _end_) dado un valor (_v_) que es la cantidad a interpolar y que normalmente está entre 0 y 1 (donde 0 es _start_ y 1 es _end_).

En el campo de los gráficos por ordenador (_computer graphics_) se le suele llamar **lerp**.

### Fórmula
```javascript
/**
 * @param {number} start - The first value
 * @param {number} end - The second value
 * @param {number} v - The amount to interpolate
 * @return {number} The interpolated value
 */
function linearInterpolation(start, end, v) {
  return (1 - v) * start + v * end;
}
```

### Ejemplos
```javascript
linearInterpolation(10, 20, 0) // 10
linearInterpolation(10, 20, 1) // 20
linearInterpolation(10, 20, 0.5) // 15
linearInterpolation(10, 20, 0.2) // 12
linearInterpolation(100, 300, 0.5) // 200
linearInterpolation(-10, 10, 0.5) // 0
linearInterpolation(0, 0.5, 0.5) // 0.25
```

Si no se pone un valor (_v_) entre 0 y 1 te da un valor fuera del rango de valores conocidos (_start_, _end_):
```javascript
linearInterpolation(0, 100, 2) // 200
linearInterpolation(0, 100, -1) // -100
```

### Demos
➡️ [Mover el ratón sin interpolación lineal](https://codepen.io/beaps/pen/XWmxZej)

➡️ [Mover el ratón con interpolación lineal](https://codepen.io/beaps/pen/rNOqJEw)

➡️ [Cambiar de color](https://codepen.io/beaps/pen/GRpPXWJ)

➡️ [Del punto A al punto B](https://codepen.io/beaps/pen/YzydgOR)

#### Referencias
- <https://mattdesl.svbtle.com/linear-interpolation>
- <https://en.wikipedia.org/wiki/Linear_interpolation>
- <https://www.trysmudford.com/blog/linear-interpolation-functions/>
- <https://www.trysmudford.com/blog/linear-interpolation/>
- <https://gist.github.com/Anthodpnt/f4ad9127a3c5479d1c0e8ff5ed79078e>
- <https://p5js.org/reference/#/p5/lerp>
- <https://codepen.io/rachsmith/post/animation-tip-lerp>
