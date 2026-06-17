# ng-hub-ui-dropdown

**Español** | [English](./README.md)

[![NPM Version](https://img.shields.io/npm/v/ng-hub-ui-dropdown.svg)](https://www.npmjs.com/package/ng-hub-ui-dropdown)
[![License](https://img.shields.io/npm/l/ng-hub-ui-dropdown.svg)](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/blob/main/LICENSE)
[![Status](https://img.shields.io/badge/Status-Pre--release-orange.svg)](https://github.com/carlos-morcillo/ng-hub-ui-dropdown)

> Componentes de dropdown modernos y accesibles para Angular, parte del ecosistema ng-hub-ui.

> ⚠️ **Pre-release (v0.0.1).** Este paquete es un esqueleto inicial. La API pública **aún no es estable** y solo incluye un componente de marcador de posición mientras se diseñan las directivas del dropdown. No lo uses en producción. Las secciones marcadas como _planificado_ describen la hoja de ruta prevista, no funcionalidad ya disponible.

## Documentación y ejemplos en vivo

Este paquete forma parte de [Hub UI](https://hubui.dev/), una colección de bibliotecas de componentes Angular para aplicaciones standalone.

- Documentación: https://hubui.dev/dropdown/
- Ejemplos en vivo: https://hubui.dev/dropdown/examples/
- Hub UI: https://hubui.dev/

## 🧩 Familia de bibliotecas `ng-hub-ui`

Esta biblioteca forma parte del ecosistema **ng-hub-ui**:

- [**ng-hub-ui-accordion**](https://www.npmjs.com/package/ng-hub-ui-accordion) (obsoleta — usa ng-hub-ui-panels)
- [**ng-hub-ui-action-sheet**](https://www.npmjs.com/package/ng-hub-ui-action-sheet)
- [**ng-hub-ui-avatar**](https://www.npmjs.com/package/ng-hub-ui-avatar)
- [**ng-hub-ui-board**](https://www.npmjs.com/package/ng-hub-ui-board)
- [**ng-hub-ui-breadcrumbs**](https://www.npmjs.com/package/ng-hub-ui-breadcrumbs)
- [**ng-hub-ui-calendar**](https://www.npmjs.com/package/ng-hub-ui-calendar)
- [**ng-hub-ui-dropdown**](https://www.npmjs.com/package/ng-hub-ui-dropdown) ← Estás aquí
- [**ng-hub-ui-ds**](https://www.npmjs.com/package/ng-hub-ui-ds)
- [**ng-hub-ui-forms**](https://www.npmjs.com/package/ng-hub-ui-forms)
- [**ng-hub-ui-history**](https://www.npmjs.com/package/ng-hub-ui-history)
- [**ng-hub-ui-milestones**](https://www.npmjs.com/package/ng-hub-ui-milestones)
- [**ng-hub-ui-modal**](https://www.npmjs.com/package/ng-hub-ui-modal)
- [**ng-hub-ui-nav**](https://www.npmjs.com/package/ng-hub-ui-nav)
- [**ng-hub-ui-paginable**](https://www.npmjs.com/package/ng-hub-ui-paginable)
- [**ng-hub-ui-panels**](https://www.npmjs.com/package/ng-hub-ui-panels)
- [**ng-hub-ui-portal**](https://www.npmjs.com/package/ng-hub-ui-portal)
- [**ng-hub-ui-skeleton**](https://www.npmjs.com/package/ng-hub-ui-skeleton)
- [**ng-hub-ui-sortable**](https://www.npmjs.com/package/ng-hub-ui-sortable)
- [**ng-hub-ui-stepper**](https://www.npmjs.com/package/ng-hub-ui-stepper)
- [**ng-hub-ui-utils**](https://www.npmjs.com/package/ng-hub-ui-utils)

---

## 📦 Descripción

`ng-hub-ui-dropdown` busca ofrecer componentes de dropdown modernos y accesibles para Angular con una API flexible y un buen encaje con proyectos basados en Bootstrap y con el ecosistema ng-hub-ui. Se concibe como una versión mejorada, desacoplada y optimizada para tree-shaking del clásico dropdown de Bootstrap / ng-bootstrap, de modo que los proyectos existentes puedan migrar con cambios mínimos en sus plantillas ganando nuevas capacidades.

## 🚦 Estado

Esta biblioteca está en **pre-release**. La superficie publicada actualmente es un esqueleto:

| Elemento | Estado |
| --- | --- |
| Componente marcador `Dropdown` (selector `lib-dropdown`) | ✅ Implementado (solo marcador) |
| Directivas `hubDropdown` / `hubDropdownToggle` / `hubDropdownMenu` | 🚧 Planificado |
| Directivas `hubDropdownItem`, `hubDropdownAnchor` | 🚧 Planificado |
| Configuración de posición, disparador, overflow y animación | 🚧 Planificado |
| Paridad de migración con ng-bootstrap | 🚧 Planificado |

### Funcionalidades planificadas

- **Fork mejorado de ng-bootstrap** — desacoplado de la biblioteca completa para mayor flexibilidad y bundles más pequeños.
- **Compatibilidad con Bootstrap** — funciona con clases y estilos de Bootstrap de serie.
- **Comportamiento configurable** — posición, disparador (`click` / `hover` / `focus` / `manual`), cierre al hacer clic fuera, offset, boundary, posicionamiento automático, prevención de overflow, flip y ocultar al hacer scroll.
- **Animaciones** — `fade`, `slide`, `scale` o `none`.
- **Accesibilidad** — soporte WCAG 2.1 AA, navegación por teclado y marcado compatible con lectores de pantalla.
- **TypeScript estricto** — tipado preciso para items, badges y atajos de teclado.
- **Tree-shaking optimizado** — importa solo lo que usas.

## 🚀 Instalación

```bash
npm install ng-hub-ui-dropdown
```

> Al tratarse de una pre-release, fija la versión exacta (`ng-hub-ui-dropdown@0.0.1`) y cuenta con cambios incompatibles entre versiones.

## ⚙️ Uso

El único componente disponible actualmente es un marcador de posición usado para validar la compilación del paquete:

```typescript
import { Component } from '@angular/core';
import { Dropdown } from 'ng-hub-ui-dropdown';

@Component({
	selector: 'app-example',
	standalone: true,
	imports: [Dropdown],
	template: `<lib-dropdown></lib-dropdown>`
})
export class ExampleComponent {}
```

Esto solo renderiza un elemento marcador. La API basada en directivas que se muestra abajo está **planificada** y todavía no está disponible:

```html
<!-- API PLANIFICADA — aún no implementada -->
<div class="dropdown" hubDropdown>
	<button class="btn btn-primary dropdown-toggle" hubDropdownToggle type="button">Opciones</button>
	<div class="dropdown-menu" *hubDropdownMenu>
		<a class="dropdown-item" href="#">Acción 1</a>
		<a class="dropdown-item" href="#">Acción 2</a>
		<div class="dropdown-divider"></div>
		<a class="dropdown-item text-danger" href="#">Eliminar</a>
	</div>
</div>
```

## 🪄 Referencia de API

### Componente `Dropdown` (implementado)

| Elemento | Valor | Notas |
| --- | --- | --- |
| Selector | `lib-dropdown` | Selector marcador; cambiará antes de la versión estable. |
| Inputs | _ninguno_ | Todavía sin inputs configurables. |
| Outputs | _ninguno_ | Todavía sin outputs. |
| Contenido | Plantilla marcador estática | Renderiza `dropdown works!`. |

> La **API planificada** (directivas, inputs, interfaces de item/configuración, opciones de posición y animación) se documentará aquí a medida que aterrice. Sigue el progreso en el [changelog](./CHANGELOG.md).

## 🤝 Contribución

Las contribuciones son bienvenidas. Como la API aún se está diseñando, abre una incidencia para discutir la dirección antes de enviar cambios grandes.

1. Haz fork del repositorio
2. Crea una rama de feature: `git checkout -b feature/dropdown-enhancement`
3. Confirma tus cambios: `git commit -m 'feat: enhance dropdown'`
4. Sube la rama: `git push origin feature/dropdown-enhancement`
5. Abre un Pull Request

```bash
git clone https://github.com/carlos-morcillo/ng-hub-ui.git
cd ng-hub-ui
npm install
ng build dropdown
ng test dropdown
```

## ☕ Soporte

- [Reportar un bug](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/issues)
- [Solicitar una funcionalidad](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/issues/new)
- [Repositorio](https://github.com/carlos-morcillo/ng-hub-ui-dropdown)

Si ng-hub-ui te ha resultado útil, considera apoyar su desarrollo:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-support-yellow.svg?style=flat-square&logo=buy-me-a-coffee)](https://buymeacoffee.com/carlosmorcillo)

## 📄 Licencia

Este proyecto está bajo la licencia MIT.

MIT © [Carlos Morcillo Fernández](https://www.carlosmorcillo.com)
