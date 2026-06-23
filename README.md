# ng-hub-ui-dropdown

[Español](./README.es.md) | **English**

[![NPM Version](https://img.shields.io/npm/v/ng-hub-ui-dropdown.svg)](https://www.npmjs.com/package/ng-hub-ui-dropdown)
[![License](https://img.shields.io/npm/l/ng-hub-ui-dropdown.svg)](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/blob/main/LICENSE)
[![Status](https://img.shields.io/badge/Status-Deprecated-red.svg)](https://github.com/carlos-morcillo/ng-hub-ui-dropdown)

> **Deprecated.** This library is superseded by [`ng-hub-ui-buttons`](https://www.npmjs.com/package/ng-hub-ui-buttons) which ships `HubDropdownDirective`, `HubDropdownPanelComponent` and all related helpers. No new features will be added here.

> Modern and accessible dropdown components for Angular, part of the ng-hub-ui ecosystem.

> ⚠️ **Pre-release (v0.0.1).** This package is an early scaffold. The public API is **not stable yet** and ships a single placeholder component while the dropdown directives are being designed. Do not use it in production. The sections marked _planned_ below describe the intended roadmap, not shipped functionality.

## Documentation and Live Examples

This package is part of [Hub UI](https://hubui.dev/), a collection of Angular component libraries for standalone apps.

- Docs: https://hubui.dev/dropdown/
- Live examples: https://hubui.dev/dropdown/examples/
- Hub UI: https://hubui.dev/

## 🧩 Library Family `ng-hub-ui`

This library is part of the **ng-hub-ui** ecosystem:

- [**ng-hub-ui-accordion**](https://www.npmjs.com/package/ng-hub-ui-accordion) (deprecated — use ng-hub-ui-panels)
- [**ng-hub-ui-action-sheet**](https://www.npmjs.com/package/ng-hub-ui-action-sheet)
- [**ng-hub-ui-avatar**](https://www.npmjs.com/package/ng-hub-ui-avatar)
- [**ng-hub-ui-board**](https://www.npmjs.com/package/ng-hub-ui-board)
- [**ng-hub-ui-breadcrumbs**](https://www.npmjs.com/package/ng-hub-ui-breadcrumbs)
- [**ng-hub-ui-calendar**](https://www.npmjs.com/package/ng-hub-ui-calendar)
- [**ng-hub-ui-dropdown**](https://www.npmjs.com/package/ng-hub-ui-dropdown) ← You are here
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

## 📦 Description

`ng-hub-ui-dropdown` aims to provide modern, accessible dropdown components for Angular with a flexible API and a familiar fit for Bootstrap-based projects and the ng-hub-ui ecosystem. It is conceived as an improved, decoupled and tree-shakeable take on the classic Bootstrap / ng-bootstrap dropdown, so existing projects can migrate with minimal template changes while gaining new capabilities.

## 🚦 Status

This library is in **pre-release**. The current published surface is a scaffold:

| Item | Status |
| --- | --- |
| `Dropdown` placeholder component (selector `lib-dropdown`) | ✅ Implemented (placeholder only) |
| `hubDropdown` / `hubDropdownToggle` / `hubDropdownMenu` directives | 🚧 Planned |
| `hubDropdownItem`, `hubDropdownAnchor` directives | 🚧 Planned |
| Placement, trigger, overflow and animation configuration | 🚧 Planned |
| ng-bootstrap migration parity | 🚧 Planned |

### Planned Features

- **Enhanced ng-bootstrap fork** — decoupled from the full library for greater flexibility and smaller bundles.
- **Bootstrap compatibility** — works with Bootstrap classes and styles out of the box.
- **Configurable behaviour** — placement, trigger (`click` / `hover` / `focus` / `manual`), close-on-outside-click, offset, boundary, auto-placement, overflow prevention, flip and hide-on-scroll.
- **Animations** — `fade`, `slide`, `scale` or `none`.
- **Accessibility** — WCAG 2.1 AA support, keyboard navigation and screen-reader friendly markup.
- **Strict TypeScript** — precise typing for items, badges and keyboard shortcuts.
- **Optimized tree-shaking** — import only what you use.

## 🚀 Installation

```bash
npm install ng-hub-ui-dropdown
```

> Because this is a pre-release, pin the exact version (`ng-hub-ui-dropdown@0.0.1`) and expect breaking changes between releases.

## ⚙️ Usage

The only component currently shipped is a placeholder used to validate the package build:

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

This renders a placeholder element only. The directive-based API shown below is **planned** and not yet available:

```html
<!-- PLANNED API — not implemented yet -->
<div class="dropdown" hubDropdown>
	<button class="btn btn-primary dropdown-toggle" hubDropdownToggle type="button">Options</button>
	<div class="dropdown-menu" *hubDropdownMenu>
		<a class="dropdown-item" href="#">Action 1</a>
		<a class="dropdown-item" href="#">Action 2</a>
		<div class="dropdown-divider"></div>
		<a class="dropdown-item text-danger" href="#">Delete</a>
	</div>
</div>
```

## 🪄 API Reference

### `Dropdown` component (implemented)

| Item | Value | Notes |
| --- | --- | --- |
| Selector | `lib-dropdown` | Placeholder selector; will change before the stable release. |
| Inputs | _none_ | No configurable inputs yet. |
| Outputs | _none_ | No outputs yet. |
| Content | Static placeholder template | Renders `dropdown works!`. |

> **Planned API** (directives, inputs, item/config interfaces, placement and animation options) will be documented here as it lands. Track progress in the [changelog](./CHANGELOG.md).

## 🤝 Contribution

Contributions are welcome. Since the API is still being designed, please open an issue to discuss direction before submitting large changes.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/dropdown-enhancement`
3. Commit your changes: `git commit -m 'feat: enhance dropdown'`
4. Push the branch: `git push origin feature/dropdown-enhancement`
5. Open a Pull Request

```bash
git clone https://github.com/carlos-morcillo/ng-hub-ui.git
cd ng-hub-ui
npm install
ng build dropdown
ng test dropdown
```

## ☕ Support

- [Report a bug](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/issues)
- [Request a feature](https://github.com/carlos-morcillo/ng-hub-ui-dropdown/issues/new)
- [Repository](https://github.com/carlos-morcillo/ng-hub-ui-dropdown)

If ng-hub-ui has been useful to you, consider supporting its development:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-support-yellow.svg?style=flat-square&logo=buy-me-a-coffee)](https://buymeacoffee.com/carlosmorcillo)

## 📄 License

This project is licensed under the MIT License.

MIT © [Carlos Morcillo Fernández](https://www.carlosmorcillo.com)
