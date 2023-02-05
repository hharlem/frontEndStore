## BEM
Block, Element, Modifier

Bloque, Elemento, Modificador

Es una metodologia para crear codigo reutilizable y ordenado.
Se utilizan ciertas convenciones para nombrar a los elementos.

Reglas de BEM

- **Bloques:** Son un contenedor, si una sección por si sola es significativa y no requiere otras secciones para su apariencia (CSS) deberá ir en un bloque.
Ej. -> 
```html
<div class="cliente"> </div>
```
Este cliente no depende de otros elementos. Por si solo podemos seleccionarlo y darle estilos a ese bloque.
```css
.cliente {   }
```

- **Elementos:** Parte de un bloque, depende del bloque y no es por si solo significativo; tienen la caracteristica de que utilizan el nombre del bloque y despues un doble guion bajo.
Ej. ->
```html
<p class="cliente__nombre"> </p>

<style>
.cliente__nombre{...}
</style> 
```

- **Modificadores:** ¿Un bloque o un elemento tendrá una variante? Se utiliza un modificador que es una "bandera" que avisa que ese elemento tendrá un diseño diferente.
Ej. ->
```html
<p class="cliente__nombre--ceo"> </p>

<style>
.cliente__nombre--ceo{...}
</style> 
```

- Tambien se puede saltar el elemento y solamente incluir bloque--modificador
```html
<p class="grafico--camisas"> </p>

<style>
.grafico--camisas{...}
</style> 
```

## Buscar que es minmax en css grid
/* Grid */
```css
.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 2rem;
}```