# Clamp

Ajustar/restringir un valor a un rango.

### Fórmula

```javascript
/**
 * @param {number} min - The minimum value.
 * @param {number} max - The maximum value.
 * @param {number} value - The value to clamp.
 * @returns {number} The clamped value.
 */
function clamp(min, max, value) {
  return Math.max(min, Math.min(max, value));
}
```

### Ejemplos
```javascript
clamp(70,90,82); // 82
clamp(70,90,75); // 75
clamp(70,90,30); // 70
clamp(70,90,95); // 90
```

### Combinar con Interpolación lineal y Normalización
```javascript
clamp(20,40,linearInterpolation(20,40,1)); // 40
clamp(20,40,linearInterpolation(20,40,0)); // 20
clamp(20,40,linearInterpolation(20,40,0.5)); // 30
clamp(20,40,linearInterpolation(20,40,3)); // 40
clamp(20,40,linearInterpolation(20,40,-5)); // 20

clamp(0,1,normalize(20,40,40)); // 1
clamp(0,1,normalize(20,40,20)); // 0
clamp(0,1,normalize(20,40,30)); // 0.5
clamp(0,1,normalize(20,40,80)); // 1
clamp(0,1,normalize(20,40,7)); // 0
```

#### Referencias
- <https://www.html5rocks.com/en/tutorials/speed/parallax/>
- <https://www.trysmudford.com/blog/linear-interpolation-functions/>
- <https://p5js.org/reference/#/p5/constrain>
