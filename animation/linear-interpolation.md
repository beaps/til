# Linear Interpolation

La `interpolación lineal` te permite obtener un valor entre dos valores conocidos (v1 y v2) dado un valor (v3) que normalmente está entre 0 y 1 (donde 0 es v1 y 1 es v2).

Fórmula:

```javascript
function linearInterpolation(v1, v2, v3) {
  return (1 - v3) * v1 + v3 * v2;
}
```

Ejemplos:
```javascript
linearInterpolation(10, 20, 0) // 10
linearInterpolation(10, 20, 1) // 20
linearInterpolation(10, 20, 0.5) // 15
linearInterpolation(10, 20, 0.2) // 12
linearInterpolation(100, 300, 0.5) // 200
linearInterpolation(-10, 10, 0.5) // 0
linearInterpolation(0, 0.5, 0.5) // 0.25
```

Si no se pone un valor (v3) entre 0 y 1 te da un valor fuera del rango de valores conocidos (v1, v2):
```javascript
linearInterpolation(0, 100, 2) // 200
linearInterpolation(0, 100, -1) // -100
```

Referencias:
- <https://mattdesl.svbtle.com/linear-interpolation>
- <https://en.wikipedia.org/wiki/Linear_interpolation>
- <https://www.trysmudford.com/blog/linear-interpolation-functions/>
- <https://www.trysmudford.com/blog/linear-interpolation/>
