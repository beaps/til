# Normalization

La `normalización` convierte un número (_value_) de un rango (_min_, _max_) en un valor entre 0 y 1.

Los valores fuera del rango no están sujetos a 0 y 1.

### Fórmula

```javascript
/**
 * @param {number} min - The minimun value of the range
 * @param {number} max - The maximun value of the range
 * @param {number} value - The value to be normalized
 * @returns {number} The normalized value.
 */
function normalize(min, max, value) {
  return (value - min) / (max - min);
}
```

### Ejemplos

```javascript
normalize(10,30,10); // 0
normalize(10,30,30); // 1
normalize(10,30,20); // 0.5
normalize(10,30,15); // 0.25
normalize(10,30,9); // -0.05
normalize(10,30,31); // 1.05
normalize(10,30,-10); // -1
normalize(10,30,40); // 1.5
normalize(10,30,50); // 2
normalize(10,50,40); // 0.75
normalize(10,50,90); // 2
normalize(-10,10,0); // 0.5
```

### Normalización vs Interpolación lineal
```javascript
normalize(5,15,10); // 0.5
linearInterpolation(5,15,0.5); // 10
normalize(5,15,15); // 1
linearInterpolation(5,15,1); // 15
normalize(5,15,5); // 0
linearInterpolation(5,15,0); // 5
```

#### Referencias
- <https://gist.github.com/Anthodpnt/aafeb0dc669fb9137dd0550b6f5d8630>
- <https://p5js.org/reference/#/p5/norm>
- <https://developers.google.com/machine-learning/data-prep/transform/normalization>
- <https://developers.google.com/machine-learning/glossary#normalization>
- <https://www.educba.com/normalization-formula/>
