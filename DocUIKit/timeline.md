# Documentación del UI KIT

# Componente: Timeline

## Descripción general: Este componente está situado debajo de la barra de navegación y su principal función es indicarle al usuario en qué interfaz se encuentra.

- **Tipo de componente:**
  Este es el componente Timeline.
- **Atributos:**
  El componente está situado debajo de la barra de navegación, ofrece al usuario información sobre en qué interfaz se encuentra, también incluye el ícono de acuerdo a dicha interfaz según los íconos especificados en el menú principal.

## Guia de uso

| class     | descripción                                                                              | uso               |
| --------- | ---------------------------------------------------------------------------------------- | ----------------- |
| timeline  | corresponde al posicionamiento de nuestra timeline                                       | class="timeline"  |
| container | corresponde al contenedor que va a contener nuestro content                              | class="container" |
| right     | corresponde al texto que se muestra en el banner                                         | class="right"     |
| primero   | corresponde al cambio de color de " ", que se usa en el primer paso de nuestra timeline  | class="primero"   |
| segundo   | corresponde al cambio de color de " ", que se usa en el segundo paso de nuestra timeline | class="segundo"   |
| tercero   | corresponde al cambio de color de " ", que se usa en el tercer paso de nuestra timeline  | class="tercero"   |
| cuarto    | corresponde al cambio de color de " ", que se usa en el cuarto paso de nuestra timeline  | class="cuarto"    |

HTML (Con informacion de ejemplo)

```html
<div class="timeline">
  <div class="container right primero">
    <div class="content">
      <h2>Pendiente</h2>
      <p>26/08/2024 10:30 Hrs.</p>
      <p>Notificado ✓</p>
    </div>
  </div>
  <div class="container right tercero">
    <div class="content">
      <h2>Evaluado</h2>
      <p>27/08/2024 10:30 Hrs.</p>
      <p>Notificado ✓</p>
    </div>
  </div>
  <div class="container right segundo">
    <div class="content">
      <h2>Pagado</h2>
      <p>28/08/2024 10:00 Hrs.</p>
      <p>Notificado ✓</p>
    </div>
  </div>
  <div class="container right primero">
    <div class="content">
      <h2>Finalizado</h2>
      <p>30/08/2024 12:30 Hrs.</p>
      <p>Notificado ✓</p>
    </div>
  </div>
</div>
```

CSS

```css
.timeline {
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
}

.timeline::after {
  content: "";
  position: absolute;
  width: 3px;
  background-color: black;
  top: 0;
  bottom: 0;
  left: 3px;
  margin-left: -3px;
}

.container {
  padding: 10px 10px;
  position: relative;
  background-color: inherit;
  width: 20%;
}

.container::after {
  content: "";
  position: absolute;
  width: 15px;
  height: 15px;
  right: -17px;
  border: 4px solid black;
  top: 18px;
  border-radius: 50%;
  z-index: 1;
}

.primero::after {
  background-color: var(--secondary-color);
}

.segundo::after {
  background-color: var(--secondary-color-lighten);
}

.tercero::after {
  background-color: var(--primary-color-lighten);
}

.cuarto::after {
  background-color: var(--tertiary-color);
}

.right {
  left: 6px;
}

.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 20px;
  border: medium solid black;
  border-width: 10px 10px 10px 0;
  border-color: transparent black transparent transparent;
}

.right::after {
  left: -16px;
}

.content {
  padding: 10px 10px;
  border-radius: 6px;
}
```
